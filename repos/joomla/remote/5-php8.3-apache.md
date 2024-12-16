## `joomla:5-php8.3-apache`

```console
$ docker pull joomla@sha256:8d794363c5660e48c35ac478ee90f4e80af31623919ae090e29e7e3e408e50b6
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

### `joomla:5-php8.3-apache` - linux; amd64

```console
$ docker pull joomla@sha256:122125cc7bb1fab73fe6ab5c2a5ab3399e390bac4fbd3e9d140023accb0e06e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.0 MB (259035993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70b65b75a017db819d8170def06a4cf741858417638455710bbdc12e07407e5d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 21 Nov 2024 06:31:33 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Thu, 21 Nov 2024 06:31:33 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 21 Nov 2024 06:31:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 21 Nov 2024 06:31:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 21 Nov 2024 06:31:33 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 21 Nov 2024 06:31:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 21 Nov 2024 06:31:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 21 Nov 2024 06:31:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 21 Nov 2024 06:31:33 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 21 Nov 2024 06:31:33 GMT
ENV PHP_VERSION=8.3.14
# Thu, 21 Nov 2024 06:31:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.14.tar.xz.asc
# Thu, 21 Nov 2024 06:31:33 GMT
ENV PHP_SHA256=58b4cb9019bf70c0cbcdb814c7df79b9065059d14cf7dbf48d971f8e56ae9be7
# Thu, 21 Nov 2024 06:31:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 21 Nov 2024 06:31:33 GMT
STOPSIGNAL SIGWINCH
# Thu, 21 Nov 2024 06:31:33 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
WORKDIR /var/www/html
# Thu, 21 Nov 2024 06:31:33 GMT
EXPOSE map[80/tcp:{}]
# Thu, 21 Nov 2024 06:31:33 GMT
CMD ["apache2-foreground"]
# Sat, 14 Dec 2024 11:07:50 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Sat, 14 Dec 2024 11:07:50 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Sat, 14 Dec 2024 11:07:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libicu-dev 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libmagickwand-dev 		libpq-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	pecl install APCu-5.1.23; 	pecl install memcached-3.3.0; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
VOLUME [/var/www/html]
# Sat, 14 Dec 2024 11:07:50 GMT
ENV JOOMLA_VERSION=5.2.1
# Sat, 14 Dec 2024 11:07:50 GMT
ENV JOOMLA_SHA512=87b2e1d01cf13458c5f24cfa7e5a092e087961c823fde8db6a5e5090bbef7e64a5e33900b3354a18d4ce7fc57d5d0719745fac3ec5597d7d44d91753ebd98c6a
# Sat, 14 Dec 2024 11:07:50 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/5.2.1/Joomla_5.2.1-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
COPY makedb.php /makedb.php # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 14 Dec 2024 11:07:50 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:bc0965b23a04fe7f2d9fb20f597008fcf89891de1c705ffc1c80483a1f098e4f`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 28.2 MB (28231580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55bfcbcb87a3d9966105ed8c691833fe95c03ba2a98bca581af4c44e3b929288`  
		Last Modified: Tue, 03 Dec 2024 02:24:10 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26ab5765987daf7bdcf0521b8059e120f8461ac9864d9032456437ddde86e88d`  
		Last Modified: Tue, 03 Dec 2024 02:24:11 GMT  
		Size: 104.2 MB (104150759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0146e8c39c25b1d64de12968c70d7d6b423b14b83eaef8abcf520ec935436475`  
		Last Modified: Tue, 03 Dec 2024 02:24:10 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35d8b09a42f213562fc747f7536a83f4c1f13348566c65321655695fa9b45e0f`  
		Last Modified: Tue, 03 Dec 2024 02:24:10 GMT  
		Size: 20.1 MB (20123793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18808a3789aba6fc7906e30ee5d0a99f7c90b162e4ee5c8bf3084819937b7118`  
		Last Modified: Tue, 03 Dec 2024 02:24:11 GMT  
		Size: 431.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df3cf4f1e7cd7fcdff5139f31a34db2968b2b6ece0fec5bb66437d072d58ce7b`  
		Last Modified: Tue, 03 Dec 2024 02:24:11 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6de2d72e53da0f59feee908b6473e52c7e90ab43fea86fe5cb846ac00595251`  
		Last Modified: Tue, 03 Dec 2024 02:24:11 GMT  
		Size: 12.6 MB (12648294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe3f47537dad61d9d5c7dd467fb9a88d772732c11ff7aee6d938de28fa870c34`  
		Last Modified: Tue, 03 Dec 2024 02:24:11 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97c061cf0423e038dea8cbb6e8873408a25dcdb67c2ff8520274aacc0118a605`  
		Last Modified: Tue, 03 Dec 2024 02:24:12 GMT  
		Size: 11.7 MB (11650051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:608ccf994ab7fafa6820fcb77872b1cce1eb3b8156ea3113e7a022846bceaf32`  
		Last Modified: Tue, 03 Dec 2024 02:24:12 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4730ec79ae125ea2e552aac4f2f99cf5f3f68e856da0874b70180105df7880bc`  
		Last Modified: Tue, 03 Dec 2024 02:24:12 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:580630955636857b73b120f51a12944f94144eb835431f92e06f537825b0b6c2`  
		Last Modified: Tue, 03 Dec 2024 02:24:12 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9119cb89a6782a446715677aeea28efa3abf03fdf61421be5ff0dfe00dfe15ec`  
		Last Modified: Mon, 16 Dec 2024 18:30:37 GMT  
		Size: 27.2 MB (27160042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14e312d0054f37119dd3c839cf15ef42d8a277d4fd5e8d9be80006ea05714d77`  
		Last Modified: Mon, 16 Dec 2024 18:30:37 GMT  
		Size: 31.3 MB (31265442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6aed2f5059a66aa07b8f885c9948f9e0d87205fdd91cae801a1d8dc2c4c6399`  
		Last Modified: Mon, 16 Dec 2024 18:30:36 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ba28c1fd16c3dce43158ff174f81402bc2ce49e2738ca6f33ba2630750bc020`  
		Last Modified: Mon, 16 Dec 2024 18:30:36 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c591959c047646ad585d55df1c7733fd3d581bb48ca2260f0a0f9df2b478b98f`  
		Last Modified: Mon, 16 Dec 2024 18:30:37 GMT  
		Size: 19.2 KB (19158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc88e767c6e8db039b2b3f5501c6bc0e3e0d030bf1c9d7b05de6a22edf95b637`  
		Last Modified: Mon, 16 Dec 2024 18:30:37 GMT  
		Size: 23.8 MB (23775918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24d1e133ae93101b8d110dbc8d9f72600477937ec3c5f9447f61a36fb8487dff`  
		Last Modified: Mon, 16 Dec 2024 18:30:38 GMT  
		Size: 3.7 KB (3655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc11881d9c62580e3d4cbd308b7caaa83049bc5c9b7e2d8db2ac14d04fdd3a51`  
		Last Modified: Mon, 16 Dec 2024 18:30:38 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:5-php8.3-apache` - unknown; unknown

```console
$ docker pull joomla@sha256:c44c9d86e8f4d9a158a1934fe2e0fd2d2b73fd09095dd39324991d72788d8961
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.9 KB (58862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16d1b64a0f494a41e652130382f3a039ca73331abc8a53bda5102cac6d23d302`

```dockerfile
```

-	Layers:
	-	`sha256:1f8d517b4c5620d4f285d7225dc3ed1c9f6a816a8cf7fcd22a3e138b6ad12970`  
		Last Modified: Mon, 16 Dec 2024 18:30:36 GMT  
		Size: 58.9 KB (58862 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:5-php8.3-apache` - linux; arm variant v5

```console
$ docker pull joomla@sha256:1cf80b577dfe6baac0af14c846416c7bc0ad24943f954d9f9053ab2455ad0445
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.6 MB (228631891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f63de94723f2e47be7500519dba911eafb2eca931f595303a752e4ce42551ec0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 21 Nov 2024 06:31:33 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1733097600'
# Thu, 21 Nov 2024 06:31:33 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 21 Nov 2024 06:31:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 21 Nov 2024 06:31:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 21 Nov 2024 06:31:33 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 21 Nov 2024 06:31:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 21 Nov 2024 06:31:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 21 Nov 2024 06:31:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 21 Nov 2024 06:31:33 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 21 Nov 2024 06:31:33 GMT
ENV PHP_VERSION=8.3.14
# Thu, 21 Nov 2024 06:31:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.14.tar.xz.asc
# Thu, 21 Nov 2024 06:31:33 GMT
ENV PHP_SHA256=58b4cb9019bf70c0cbcdb814c7df79b9065059d14cf7dbf48d971f8e56ae9be7
# Thu, 21 Nov 2024 06:31:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 21 Nov 2024 06:31:33 GMT
STOPSIGNAL SIGWINCH
# Thu, 21 Nov 2024 06:31:33 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
WORKDIR /var/www/html
# Thu, 21 Nov 2024 06:31:33 GMT
EXPOSE map[80/tcp:{}]
# Thu, 21 Nov 2024 06:31:33 GMT
CMD ["apache2-foreground"]
# Sat, 14 Dec 2024 11:07:50 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Sat, 14 Dec 2024 11:07:50 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Sat, 14 Dec 2024 11:07:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libicu-dev 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libmagickwand-dev 		libpq-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	pecl install APCu-5.1.23; 	pecl install memcached-3.3.0; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
VOLUME [/var/www/html]
# Sat, 14 Dec 2024 11:07:50 GMT
ENV JOOMLA_VERSION=5.2.1
# Sat, 14 Dec 2024 11:07:50 GMT
ENV JOOMLA_SHA512=87b2e1d01cf13458c5f24cfa7e5a092e087961c823fde8db6a5e5090bbef7e64a5e33900b3354a18d4ce7fc57d5d0719745fac3ec5597d7d44d91753ebd98c6a
# Sat, 14 Dec 2024 11:07:50 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/5.2.1/Joomla_5.2.1-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
COPY makedb.php /makedb.php # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 14 Dec 2024 11:07:50 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:25d432086d20067bebfff2b163f22d49e7da8528782652615fe170bf8c39194d`  
		Last Modified: Tue, 03 Dec 2024 01:27:20 GMT  
		Size: 25.8 MB (25754926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7f38f689bfc81a80b77922476ec5fa4c66c3c95c18a88e0d5c163e4f88a3fa2`  
		Last Modified: Tue, 03 Dec 2024 02:47:24 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1391778530ecd6fb67099da1af9389d8c5e85a5bf4eda9154dc075982c5d03aa`  
		Last Modified: Tue, 03 Dec 2024 02:47:27 GMT  
		Size: 81.8 MB (81799353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1730374a8da7a42b29a8cb7308121c86932f17cf03f72bcbc1157654eab662c6`  
		Last Modified: Tue, 03 Dec 2024 02:47:24 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5d43114e6dacb9dea8dc21a7254e5e88b1cc12a6d007a1431166907121528d6`  
		Last Modified: Tue, 03 Dec 2024 02:51:31 GMT  
		Size: 19.4 MB (19418860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56fab695d67cbdff447c2ab807f8900e1d2a4dce642475708bed149bbdd54dab`  
		Last Modified: Tue, 03 Dec 2024 02:51:30 GMT  
		Size: 431.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5e205d192900e0b63fd0542c47e1a455fa0a703afa9932fd48ab46e05557439`  
		Last Modified: Tue, 03 Dec 2024 02:51:30 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27c8352a413d6bfacf82f8721df65d2ec03478aedc02a625d41f3a6995cc7949`  
		Last Modified: Tue, 03 Dec 2024 03:05:56 GMT  
		Size: 12.6 MB (12646760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcd5d74facdf03f301be214ca62347bf6d3340182f71c9162992a0d7dc3131f8`  
		Last Modified: Tue, 03 Dec 2024 03:05:56 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c48e368b22b420fcf951bf4405a48a09bc527596e7012ec11b5042b48d4aba4`  
		Last Modified: Tue, 03 Dec 2024 03:05:57 GMT  
		Size: 10.6 MB (10619453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a75a495a45fc215485cfa950bd22302ac8c377d246270330659f25281d90b33`  
		Last Modified: Tue, 03 Dec 2024 03:05:56 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b5b94d9ccb90c73ff2dc9f99049b427bbf33552cdd77a28a78aab530647f81f`  
		Last Modified: Tue, 03 Dec 2024 03:05:57 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30fe9b909709fb781724c723c3fb97efda23894a704edb74452c0a35b441711b`  
		Last Modified: Tue, 03 Dec 2024 03:05:57 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8442cc49fd6220313f4f08f959e9b188d77bf3869c7f23461d82ebdcbecd5ae`  
		Last Modified: Mon, 16 Dec 2024 18:45:42 GMT  
		Size: 26.6 MB (26615183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d503ac06aedcace7d27ab427afb4b599dd2037b2d760ffbc1f418731de165ed6`  
		Last Modified: Mon, 16 Dec 2024 18:45:42 GMT  
		Size: 28.0 MB (27971331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd3eb04e2694507c0dfe6c2783d7cb65a895b3d6557075436385826bcb23c26a`  
		Last Modified: Mon, 16 Dec 2024 18:45:41 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c4718fddc581b72ecd0fe680c7fc22d2db1dd9e3614f24cc7cdd2657bf39d93`  
		Last Modified: Mon, 16 Dec 2024 18:45:41 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3c2262350c0ae8546154490ec02fb9aa5174e216e23cdcca419907ebcd77a48`  
		Last Modified: Mon, 16 Dec 2024 18:45:42 GMT  
		Size: 19.2 KB (19156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8aef166fc1d17e889afb02afe1a48e08dd50d0ecf53a2ccd2b8890cab28c3f4`  
		Last Modified: Mon, 16 Dec 2024 18:45:43 GMT  
		Size: 23.8 MB (23775915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f22e94bc6f7d47e106c355b715ab8c4311c9a3636148b46b73de636598ec6d84`  
		Last Modified: Mon, 16 Dec 2024 18:45:43 GMT  
		Size: 3.7 KB (3655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e3cd94e8e6a2dd0f6f5928d4462340062204139ce28a3f880d9b837b7765872`  
		Last Modified: Mon, 16 Dec 2024 18:45:43 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:5-php8.3-apache` - unknown; unknown

```console
$ docker pull joomla@sha256:47814232a1792e91ffb34a8bcf09d9713b07604a884c37396b6280491f893607
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.0 KB (58993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e141e74d4684f2c6fe3cd220f60cc1fa1e346c825d2900c3970a05c21e113ce3`

```dockerfile
```

-	Layers:
	-	`sha256:5a9d88b2d67a989afb1ac864c94abd44648ede6013c0a702838d30b848167982`  
		Last Modified: Mon, 16 Dec 2024 18:45:41 GMT  
		Size: 59.0 KB (58993 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:5-php8.3-apache` - linux; arm variant v7

```console
$ docker pull joomla@sha256:cefc545e7b259e7897dafad45ed088f3a9c69b535ff78795d70e833d1226a87d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.5 MB (217482175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e419ca764a8e9e789a39aa03dcaeb25b3960403074ff766463da9eafeeee65c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 21 Nov 2024 06:31:33 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1733097600'
# Thu, 21 Nov 2024 06:31:33 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 21 Nov 2024 06:31:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 21 Nov 2024 06:31:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 21 Nov 2024 06:31:33 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 21 Nov 2024 06:31:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 21 Nov 2024 06:31:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 21 Nov 2024 06:31:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 21 Nov 2024 06:31:33 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 21 Nov 2024 06:31:33 GMT
ENV PHP_VERSION=8.3.14
# Thu, 21 Nov 2024 06:31:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.14.tar.xz.asc
# Thu, 21 Nov 2024 06:31:33 GMT
ENV PHP_SHA256=58b4cb9019bf70c0cbcdb814c7df79b9065059d14cf7dbf48d971f8e56ae9be7
# Thu, 21 Nov 2024 06:31:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 21 Nov 2024 06:31:33 GMT
STOPSIGNAL SIGWINCH
# Thu, 21 Nov 2024 06:31:33 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
WORKDIR /var/www/html
# Thu, 21 Nov 2024 06:31:33 GMT
EXPOSE map[80/tcp:{}]
# Thu, 21 Nov 2024 06:31:33 GMT
CMD ["apache2-foreground"]
# Sat, 14 Dec 2024 11:07:50 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Sat, 14 Dec 2024 11:07:50 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Sat, 14 Dec 2024 11:07:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libicu-dev 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libmagickwand-dev 		libpq-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	pecl install APCu-5.1.23; 	pecl install memcached-3.3.0; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
VOLUME [/var/www/html]
# Sat, 14 Dec 2024 11:07:50 GMT
ENV JOOMLA_VERSION=5.2.1
# Sat, 14 Dec 2024 11:07:50 GMT
ENV JOOMLA_SHA512=87b2e1d01cf13458c5f24cfa7e5a092e087961c823fde8db6a5e5090bbef7e64a5e33900b3354a18d4ce7fc57d5d0719745fac3ec5597d7d44d91753ebd98c6a
# Sat, 14 Dec 2024 11:07:50 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/5.2.1/Joomla_5.2.1-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
COPY makedb.php /makedb.php # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 14 Dec 2024 11:07:50 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:80b4fb4796cece09f69103235c60ffd0226a78c400a2953144b84c17de4df93d`  
		Last Modified: Tue, 03 Dec 2024 01:28:14 GMT  
		Size: 23.9 MB (23933588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfc399a814abef0b215a25083103b4fcd6382c3040364b6565271bfaad3edcda`  
		Last Modified: Tue, 03 Dec 2024 02:45:44 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c111bef206c9990ed304a2c9e0dbc3e87552d4023cb73e5796908ce98c5a16`  
		Last Modified: Tue, 03 Dec 2024 02:45:47 GMT  
		Size: 76.0 MB (75969214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c345ebeb8ac614dcc4ff559e2cf2d693ff887d5cb958080625dc4d803abd018`  
		Last Modified: Tue, 03 Dec 2024 02:45:44 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64247e8882ecb48484c43614c1bd400c9f3fa7ff601a3e74f81606279623eca2`  
		Last Modified: Tue, 03 Dec 2024 02:49:32 GMT  
		Size: 18.9 MB (18857266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:489174183fa221f132d5b3d11e3bf9b32527d04508f03839c9a1555913aeb51b`  
		Last Modified: Tue, 03 Dec 2024 02:49:31 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3be5de890f1f55562915effb16f54430acf049d0013e862b5942f473118fe5ed`  
		Last Modified: Tue, 03 Dec 2024 02:49:31 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1dae98941703900f5d67eb628e8c739584759a62febbfde2b5732e0e9937a85`  
		Last Modified: Tue, 03 Dec 2024 03:17:38 GMT  
		Size: 12.6 MB (12646708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:575b1547dd67fbc79b2894a9acdbb35c5602751fe946730baeed886d98d317f1`  
		Last Modified: Tue, 03 Dec 2024 03:17:38 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3d03b0e112f9bf2399a8653a7f0f7f44f1574d3d30f59e2bbc680bbb1e7efb7`  
		Last Modified: Tue, 03 Dec 2024 03:17:38 GMT  
		Size: 10.0 MB (10039384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ac32bf7a783595bf28fad56375a219029164e32c1730bb1f4d451bb468cbf43`  
		Last Modified: Tue, 03 Dec 2024 03:17:38 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce01050756d5b9d200fc8b4a234e85c9655ff0b61d5b74cdef42a54ac82e663a`  
		Last Modified: Tue, 03 Dec 2024 03:17:39 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83b99e8de489c2a7c70479fad34915d0f0f085f2c471cd07cd3aa94ee6df3a13`  
		Last Modified: Tue, 03 Dec 2024 03:17:39 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59300773c554f31e4e2763eead6c90aadf6eb06e3568ca9d0e44cee9ed748e63`  
		Last Modified: Mon, 16 Dec 2024 18:50:30 GMT  
		Size: 25.8 MB (25848515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:578318dcb83409d88754d406d4d5fc6a5a2e5521cfeb269831b883927665ab60`  
		Last Modified: Mon, 16 Dec 2024 18:50:30 GMT  
		Size: 26.4 MB (26381480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36d2d31401ae156c1baa9147fa87513a3a3984e403a123eef2cada29a36fb0aa`  
		Last Modified: Mon, 16 Dec 2024 18:50:29 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31765143453cfe1ff18a5741e81ea18c38f7974edc7fcd9bb64f35afa108b6ce`  
		Last Modified: Mon, 16 Dec 2024 18:50:29 GMT  
		Size: 391.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1a0ab4b8581dff5963941e64c24339515d0a8735f28ba6ae0736103fb4591d2`  
		Last Modified: Mon, 16 Dec 2024 18:50:30 GMT  
		Size: 19.2 KB (19154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a7ecda8990ef7b37f6b277326b76e10dd045877836505e21d3c9dc0f6e62ccd`  
		Last Modified: Mon, 16 Dec 2024 18:50:31 GMT  
		Size: 23.8 MB (23775918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddaae392f1e141278a7134c33d845f6c8abfbd3ee43f381294bd2f755544de01`  
		Last Modified: Mon, 16 Dec 2024 18:50:31 GMT  
		Size: 3.7 KB (3655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:318bd34d8c204830c7624245830034e5c4f672a0d38ecf3ea49452dc3f6bb3ec`  
		Last Modified: Mon, 16 Dec 2024 18:50:31 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:5-php8.3-apache` - unknown; unknown

```console
$ docker pull joomla@sha256:13a8485dde3db614e7783d5ddf031695d37a5a641a003dfc1fb90b407b2d5b7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.0 KB (58994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7953ebca906f01f49bb24d129fbf9747fb06ead52fe2cbbae1707aaa8aac4e3d`

```dockerfile
```

-	Layers:
	-	`sha256:8c8c1284f823a34ec19b5366d628a226a2e4d6cab59b22e50b8419a5d9ed4023`  
		Last Modified: Mon, 16 Dec 2024 18:50:29 GMT  
		Size: 59.0 KB (58994 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:5-php8.3-apache` - linux; arm64 variant v8

```console
$ docker pull joomla@sha256:2722240d21ddc0065598e6b74b9b92dfc494cda34dac6425b8507035f8fd5586
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.1 MB (250073815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d31449795a1f49893c7f78e6257510fd46900e1a64723d1d587b4cd77287ddb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 21 Nov 2024 06:31:33 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
# Thu, 21 Nov 2024 06:31:33 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 21 Nov 2024 06:31:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 21 Nov 2024 06:31:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 21 Nov 2024 06:31:33 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 21 Nov 2024 06:31:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 21 Nov 2024 06:31:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 21 Nov 2024 06:31:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 21 Nov 2024 06:31:33 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 21 Nov 2024 06:31:33 GMT
ENV PHP_VERSION=8.3.14
# Thu, 21 Nov 2024 06:31:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.14.tar.xz.asc
# Thu, 21 Nov 2024 06:31:33 GMT
ENV PHP_SHA256=58b4cb9019bf70c0cbcdb814c7df79b9065059d14cf7dbf48d971f8e56ae9be7
# Thu, 21 Nov 2024 06:31:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 21 Nov 2024 06:31:33 GMT
STOPSIGNAL SIGWINCH
# Thu, 21 Nov 2024 06:31:33 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
WORKDIR /var/www/html
# Thu, 21 Nov 2024 06:31:33 GMT
EXPOSE map[80/tcp:{}]
# Thu, 21 Nov 2024 06:31:33 GMT
CMD ["apache2-foreground"]
# Sat, 14 Dec 2024 11:07:50 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Sat, 14 Dec 2024 11:07:50 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Sat, 14 Dec 2024 11:07:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libicu-dev 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libmagickwand-dev 		libpq-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	pecl install APCu-5.1.23; 	pecl install memcached-3.3.0; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
VOLUME [/var/www/html]
# Sat, 14 Dec 2024 11:07:50 GMT
ENV JOOMLA_VERSION=5.2.1
# Sat, 14 Dec 2024 11:07:50 GMT
ENV JOOMLA_SHA512=87b2e1d01cf13458c5f24cfa7e5a092e087961c823fde8db6a5e5090bbef7e64a5e33900b3354a18d4ce7fc57d5d0719745fac3ec5597d7d44d91753ebd98c6a
# Sat, 14 Dec 2024 11:07:50 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/5.2.1/Joomla_5.2.1-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
COPY makedb.php /makedb.php # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 14 Dec 2024 11:07:50 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:bb3f2b52e6af242cee1bc6c19ce79e05544f8a1d13f5a6c1e828d98d2dbdc94e`  
		Last Modified: Tue, 03 Dec 2024 01:30:11 GMT  
		Size: 28.1 MB (28058810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:593b3b5e04c8b4e6110fb0e212055b9c7eb2aaa1cf8779fd681a2462f67111a8`  
		Last Modified: Tue, 03 Dec 2024 03:01:07 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfc980920c054a940b9793a107341acd51b059aed873177ef237579d941f23ef`  
		Last Modified: Tue, 03 Dec 2024 03:01:11 GMT  
		Size: 97.9 MB (97936346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7130ec09764042703bb02f30348dab7ba0380d619963d04ab8ccc9678ca27470`  
		Last Modified: Tue, 03 Dec 2024 03:01:07 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0487dfea6acc671d5a73050d1cb6d9894d55ab6f79fe82e0916fd83c0ee4c37`  
		Last Modified: Tue, 03 Dec 2024 03:04:46 GMT  
		Size: 20.1 MB (20120928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9970f3d36c66c0d81d84d5b43bd8a643ca7669c83b51b9efe950944e0ae9d6b4`  
		Last Modified: Tue, 03 Dec 2024 03:04:45 GMT  
		Size: 433.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78fe821f4633e8a7a268f1b2ee321ff810e3810688d047ab340d79ad5a71f116`  
		Last Modified: Tue, 03 Dec 2024 03:04:45 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361a4309642952cdc346487a3effacb91f3c25526ca46e1fa1ed8a857bff88f5`  
		Last Modified: Tue, 03 Dec 2024 03:32:15 GMT  
		Size: 12.6 MB (12648135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e067713d3bb8bf10e1ccac2aa889ee97dfbbc6ba74efd51b0298d124d23adaf`  
		Last Modified: Tue, 03 Dec 2024 03:32:15 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b8267a65e16f1c67b113b843bd38e16497f2f6db35526a777034c9c2a355b9f`  
		Last Modified: Tue, 03 Dec 2024 03:32:16 GMT  
		Size: 11.6 MB (11640338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80095e87fe8006a1cbe24ff0496d434679a34711f121a035a0f444f555a745cc`  
		Last Modified: Tue, 03 Dec 2024 03:32:15 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39498ca233b715054ed8825ef432138a3cd6ee787078c5a8f4cda9470065b468`  
		Last Modified: Tue, 03 Dec 2024 03:32:16 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:558cf9388e9b575510d5b4af096bb10ebf7daf6c978dd526f8ef0c3f75ebe823`  
		Last Modified: Tue, 03 Dec 2024 03:32:16 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599b4ebb565c73f4723011fc8a5932a823fba781258716150da0543a8dd67557`  
		Last Modified: Mon, 16 Dec 2024 18:47:49 GMT  
		Size: 27.0 MB (26988752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:679b89d198ec733da4729ce455f06377ab3cab56f5235fc5b8ed27f550828516`  
		Last Modified: Mon, 16 Dec 2024 18:47:49 GMT  
		Size: 28.9 MB (28874489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df6e904ebda67b531889370ee499d0d0bcf759959986540f88bb046516d9b864`  
		Last Modified: Mon, 16 Dec 2024 18:47:48 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25f5791dbf0295d48969dfe7873a092909421361c7e29a030cd7b9b9ab77cd35`  
		Last Modified: Mon, 16 Dec 2024 18:47:47 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dde2ccf0977cc84b61f7e0d4306956ef8b3a32e8943e0b372d898346c9ab698`  
		Last Modified: Mon, 16 Dec 2024 18:47:48 GMT  
		Size: 19.2 KB (19161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79a15282cbd894386d7d91e196f214c761bd8e502b14328b2c0119fc754c786a`  
		Last Modified: Mon, 16 Dec 2024 18:47:50 GMT  
		Size: 23.8 MB (23775902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cc79177aa70edcf21ee99fb1dad9c47bfc782028e2e96b5b4cb3946501a44f6`  
		Last Modified: Mon, 16 Dec 2024 18:47:49 GMT  
		Size: 3.7 KB (3654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df6fc1d52d9231bde1cbb8eff0ac5d12b1cbdcce356afef633e70f67443ca002`  
		Last Modified: Mon, 16 Dec 2024 18:47:50 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:5-php8.3-apache` - unknown; unknown

```console
$ docker pull joomla@sha256:386ae0856ac56e04b6fa1ea9e8a6f3d23bdf6097f74f45056785c8a15e577c97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.0 KB (59032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14b080f3a9dce27d596adb194ef8883f450ecb3566b702b4503304871d204ac1`

```dockerfile
```

-	Layers:
	-	`sha256:4a26469aabf021578ef9800adb03f8654e69516ad6faa97d902ae63d656fdff8`  
		Last Modified: Mon, 16 Dec 2024 18:47:47 GMT  
		Size: 59.0 KB (59032 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:5-php8.3-apache` - linux; 386

```console
$ docker pull joomla@sha256:ddd1e30fe21070b2e9e32fb42a15fa2e8445e5d5f955c863f954e2960d98c0b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.6 MB (257578388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0844bb10a870a0f59defc8176a871cef238b25228a80e1fcc1e1da90855eb6c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 21 Nov 2024 06:31:33 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1733097600'
# Thu, 21 Nov 2024 06:31:33 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 21 Nov 2024 06:31:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 21 Nov 2024 06:31:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 21 Nov 2024 06:31:33 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 21 Nov 2024 06:31:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 21 Nov 2024 06:31:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 21 Nov 2024 06:31:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 21 Nov 2024 06:31:33 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 21 Nov 2024 06:31:33 GMT
ENV PHP_VERSION=8.3.14
# Thu, 21 Nov 2024 06:31:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.14.tar.xz.asc
# Thu, 21 Nov 2024 06:31:33 GMT
ENV PHP_SHA256=58b4cb9019bf70c0cbcdb814c7df79b9065059d14cf7dbf48d971f8e56ae9be7
# Thu, 21 Nov 2024 06:31:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 21 Nov 2024 06:31:33 GMT
STOPSIGNAL SIGWINCH
# Thu, 21 Nov 2024 06:31:33 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
WORKDIR /var/www/html
# Thu, 21 Nov 2024 06:31:33 GMT
EXPOSE map[80/tcp:{}]
# Thu, 21 Nov 2024 06:31:33 GMT
CMD ["apache2-foreground"]
# Sat, 14 Dec 2024 11:07:50 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Sat, 14 Dec 2024 11:07:50 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Sat, 14 Dec 2024 11:07:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libicu-dev 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libmagickwand-dev 		libpq-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	pecl install APCu-5.1.23; 	pecl install memcached-3.3.0; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
VOLUME [/var/www/html]
# Sat, 14 Dec 2024 11:07:50 GMT
ENV JOOMLA_VERSION=5.2.1
# Sat, 14 Dec 2024 11:07:50 GMT
ENV JOOMLA_SHA512=87b2e1d01cf13458c5f24cfa7e5a092e087961c823fde8db6a5e5090bbef7e64a5e33900b3354a18d4ce7fc57d5d0719745fac3ec5597d7d44d91753ebd98c6a
# Sat, 14 Dec 2024 11:07:50 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/5.2.1/Joomla_5.2.1-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
COPY makedb.php /makedb.php # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 14 Dec 2024 11:07:50 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:ae6c80ee852fcccae85579165042a3767dcd1190112e87c9f22fa3e76a624c73`  
		Last Modified: Tue, 03 Dec 2024 01:27:10 GMT  
		Size: 29.2 MB (29205487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2bd1912f057b3b8df6c436a9c9e78392d35c02208232a6845353c4ca89b0f4a`  
		Last Modified: Tue, 03 Dec 2024 02:23:11 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f1c7986cc5d66d16a53b4085ebb2e56bdaccb98bb187539a0ca2aa0011a17af`  
		Last Modified: Tue, 03 Dec 2024 02:23:14 GMT  
		Size: 101.3 MB (101319975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66683b96da061ad6997de6ec89d6787aac067e47886baac132cf55116e24fd2d`  
		Last Modified: Tue, 03 Dec 2024 02:23:11 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:295fa2948517d3d073a02268894689d8f83becfde79b5d4aca553784c7642ffc`  
		Last Modified: Tue, 03 Dec 2024 02:23:12 GMT  
		Size: 20.6 MB (20638465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:188fb024d1da7626c99c889280514bbeef9edb59372115352ccc240b5b6c7ab6`  
		Last Modified: Tue, 03 Dec 2024 02:23:12 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b938438b0921b2774babc125634ef6b875533cef7ca66a58cfd9d53b77a5185`  
		Last Modified: Tue, 03 Dec 2024 02:23:12 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e7c8f241e9324bf49d48188ec525d8da2bd276b5681e1de8b7734fe36233e8b`  
		Last Modified: Tue, 03 Dec 2024 02:23:13 GMT  
		Size: 12.6 MB (12647620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46ed81b5834ba31b807f0ada0b19052a0f1687e8e3cef0d5b57d127d05d4e86c`  
		Last Modified: Tue, 03 Dec 2024 02:23:12 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b82c0115a31fbcac69cbba5f94b9d978d86c25becfd40212fedc7141c674fc`  
		Last Modified: Tue, 03 Dec 2024 02:23:13 GMT  
		Size: 11.9 MB (11866215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ddff3b32fc137c029df0712371f085823e1c6253e2a10de8aef863704440527`  
		Last Modified: Tue, 03 Dec 2024 02:23:13 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f73dcd82b985d946e2367369e8cb6a1bed4bcc302ab102093e462e3b65915ff`  
		Last Modified: Tue, 03 Dec 2024 02:23:13 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d1826053480670aa1048e2a31062c4aa6ee3ae64ac101ec4a5c8e52e9d6ceac`  
		Last Modified: Tue, 03 Dec 2024 02:23:14 GMT  
		Size: 887.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c7b8b981b5356becf7c6f1f7d03c8bfbb417c742851f908c51794ed33c59d2e`  
		Last Modified: Mon, 16 Dec 2024 18:31:03 GMT  
		Size: 27.5 MB (27524287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ce17c6e4af176dd66e5fbb82e41b34a1ca1c7a9c1beac2ad1df5e691204a1b`  
		Last Modified: Mon, 16 Dec 2024 18:31:03 GMT  
		Size: 30.6 MB (30570340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcc97b956415f7dba4a4e6599d8c0e202ae71170220360c2a728cab1c8296f65`  
		Last Modified: Mon, 16 Dec 2024 18:31:02 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07cc03e89ced8a91e9e849c4fa5b310ec01f9c60deff7ff4eb50e4df76663c41`  
		Last Modified: Mon, 16 Dec 2024 18:31:02 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:942d51c57a91d1ddb932d0f8fd170cf1d64f56a3489f28fd70ba21fff28c18c5`  
		Last Modified: Mon, 16 Dec 2024 18:31:03 GMT  
		Size: 19.2 KB (19153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37c314fc039d344acb117ff9a828d5af287f161f198bc8d55ed7f601f639c2a3`  
		Last Modified: Mon, 16 Dec 2024 18:31:04 GMT  
		Size: 23.8 MB (23775902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09c3491396eaa24851b6fe57a98e823374d7a1f9d944fc72ac4084cc6a19638a`  
		Last Modified: Mon, 16 Dec 2024 18:30:59 GMT  
		Size: 3.7 KB (3654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbd5e0972a500b2a20f2b694fd0edcc04e730dee006ca964fe810fdb41b51a8e`  
		Last Modified: Mon, 16 Dec 2024 18:31:00 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:5-php8.3-apache` - unknown; unknown

```console
$ docker pull joomla@sha256:6bff5d964fd21c84190ba967ef2eeeecc06cb66e621980ce866fe0bfd4cbbb0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.8 KB (58820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18961689b4afc987a44cd6bd92c2a2ec48902cfbebf0be935f8e7eb9a56cba4b`

```dockerfile
```

-	Layers:
	-	`sha256:5e9be7d868dff456d1ae0bf0c3ec7fc4f670b0c8b549cb35da6b4b8e38d17010`  
		Last Modified: Mon, 16 Dec 2024 18:31:01 GMT  
		Size: 58.8 KB (58820 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:5-php8.3-apache` - linux; mips64le

```console
$ docker pull joomla@sha256:8ab18a5db5201ed8d16cda6e550b98068158e3ffd96729a48c5379d619f03f0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.7 MB (231719738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f600f2b051267106c362c1c7b625fba120e813aad017f440a1b377afc91d500f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 21 Nov 2024 06:31:33 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1733097600'
# Thu, 21 Nov 2024 06:31:33 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 21 Nov 2024 06:31:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 21 Nov 2024 06:31:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 21 Nov 2024 06:31:33 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 21 Nov 2024 06:31:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 21 Nov 2024 06:31:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 21 Nov 2024 06:31:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 21 Nov 2024 06:31:33 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 21 Nov 2024 06:31:33 GMT
ENV PHP_VERSION=8.3.14
# Thu, 21 Nov 2024 06:31:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.14.tar.xz.asc
# Thu, 21 Nov 2024 06:31:33 GMT
ENV PHP_SHA256=58b4cb9019bf70c0cbcdb814c7df79b9065059d14cf7dbf48d971f8e56ae9be7
# Thu, 21 Nov 2024 06:31:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 21 Nov 2024 06:31:33 GMT
STOPSIGNAL SIGWINCH
# Thu, 21 Nov 2024 06:31:33 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
WORKDIR /var/www/html
# Thu, 21 Nov 2024 06:31:33 GMT
EXPOSE map[80/tcp:{}]
# Thu, 21 Nov 2024 06:31:33 GMT
CMD ["apache2-foreground"]
# Sat, 14 Dec 2024 11:07:50 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Sat, 14 Dec 2024 11:07:50 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Sat, 14 Dec 2024 11:07:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libicu-dev 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libmagickwand-dev 		libpq-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	pecl install APCu-5.1.23; 	pecl install memcached-3.3.0; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
VOLUME [/var/www/html]
# Sat, 14 Dec 2024 11:07:50 GMT
ENV JOOMLA_VERSION=5.2.1
# Sat, 14 Dec 2024 11:07:50 GMT
ENV JOOMLA_SHA512=87b2e1d01cf13458c5f24cfa7e5a092e087961c823fde8db6a5e5090bbef7e64a5e33900b3354a18d4ce7fc57d5d0719745fac3ec5597d7d44d91753ebd98c6a
# Sat, 14 Dec 2024 11:07:50 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/5.2.1/Joomla_5.2.1-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
COPY makedb.php /makedb.php # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 14 Dec 2024 11:07:50 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:29ac4ae2849b0c84c0ef17659082268617abeb406402ef46b6fa9140e6d2064d`  
		Last Modified: Tue, 03 Dec 2024 01:28:15 GMT  
		Size: 28.5 MB (28505909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:697b6f869e689f1f7935effcea7aef7505ad04025b0311ff3937b9103eef46fd`  
		Last Modified: Tue, 03 Dec 2024 04:22:33 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72b7f48524d255d2a114c61e2dea94f3576d2144432398eb626ed6bbb8da968d`  
		Last Modified: Tue, 03 Dec 2024 04:22:41 GMT  
		Size: 80.5 MB (80475126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd7c3c34315ea9a93e65cc52bfdaf45d8f691045833035294baddeaa21df2439`  
		Last Modified: Tue, 03 Dec 2024 04:22:33 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df91c5aff622eeb49d30bc53aeda928e25ca30d9809e0caf1fc0dbcf6aec00dd`  
		Last Modified: Tue, 03 Dec 2024 04:42:14 GMT  
		Size: 20.1 MB (20069109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d1873dc58b3bfe6549f8fd226713fa111f41803622dcaa71518533d1ab7f287`  
		Last Modified: Tue, 03 Dec 2024 04:42:11 GMT  
		Size: 434.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1faa97de501943d58384491dc09430289a7e70957ada9f084524d32187e90f64`  
		Last Modified: Tue, 03 Dec 2024 04:42:11 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:086bec4646d1fe7c30afdda8bba2ace7b4ad4cae1e29698e857ad093548b3787`  
		Last Modified: Tue, 03 Dec 2024 05:53:47 GMT  
		Size: 12.6 MB (12646486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63c39f01ec4e8beb6ec481c66348428c0978f4c4e3fe488cea9118707fbfef2d`  
		Last Modified: Tue, 03 Dec 2024 05:53:27 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6151c1d5e70b934c7ad2a723bad2a5fa99ad2a9bd62dc351695764aeec6b3754`  
		Last Modified: Tue, 03 Dec 2024 05:54:30 GMT  
		Size: 10.7 MB (10723164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70c6e59901856c4567a5f6d3c01b56ff9fb0d7b1891f56f82882c4cd178026a9`  
		Last Modified: Tue, 03 Dec 2024 05:53:27 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c31d22511c5559be8defa32ac1e4157850ab5e2f9ed0eea6560edc80675fbde`  
		Last Modified: Tue, 03 Dec 2024 05:53:28 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50b7880ee2a01ba14309b9bef4e9138157568c241edf02934b3a7e9d2b2d6dfc`  
		Last Modified: Tue, 03 Dec 2024 05:53:28 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc59865d88fa48d4ee9c288d7b9b0522c0a69dc2cfd1bc9d453048b5350b8de`  
		Last Modified: Mon, 16 Dec 2024 19:40:50 GMT  
		Size: 26.9 MB (26913097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83daece05930fe649c121898c3420055a686eaabce5a16621fd4fdcc4eb483f0`  
		Last Modified: Mon, 16 Dec 2024 19:40:51 GMT  
		Size: 28.6 MB (28580791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e286b7581088991072857c1770a2d832f80664d85d2a6d0a6da17694ec045230`  
		Last Modified: Mon, 16 Dec 2024 19:40:47 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b36f9b661b0ae0b5777ee53526d070b09f55a4d30d0437d49bb3b8672d0869`  
		Last Modified: Mon, 16 Dec 2024 19:40:48 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f01fbb19acd9f6b4c6efd4138cfbe306a91bc568a221f2bc69c36ceb5d7cef6`  
		Last Modified: Mon, 16 Dec 2024 19:40:48 GMT  
		Size: 19.2 KB (19178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9326335dc30a6347888e1af8b4e5eab35d38a4572ff0acbaf1ead78e492e9164`  
		Last Modified: Mon, 16 Dec 2024 19:40:51 GMT  
		Size: 23.8 MB (23775914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed0d5980ba1699c5afdbe90555c69ff9b828841a9f3587735c2ae8a384245f5`  
		Last Modified: Mon, 16 Dec 2024 19:40:49 GMT  
		Size: 3.7 KB (3655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e85a0bf21a68c0da9138a72b992215e4032d8423374792c67581489a4ec97bd4`  
		Last Modified: Mon, 16 Dec 2024 19:40:50 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:5-php8.3-apache` - unknown; unknown

```console
$ docker pull joomla@sha256:ef1d57e4b194ff53c5db323b6f58ddc24f06584d16e8960c58558cb7050a6ce9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.9 KB (58934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0a606022195f852eb122f24a407f92a97e908c09e8ad3e2c9d1c60b60949a0a`

```dockerfile
```

-	Layers:
	-	`sha256:6052ccb22b31ef736a4bd5f7c295e2c7c19c459290d347fa74ccb0744e2f111d`  
		Last Modified: Mon, 16 Dec 2024 19:40:47 GMT  
		Size: 58.9 KB (58934 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:5-php8.3-apache` - linux; ppc64le

```console
$ docker pull joomla@sha256:a469b9dcb02ca8c8f3fad2d5aa7e5cebcbd6845f97d5e34e0c8acef4fb203cf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.7 MB (264712253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f284089c72c6981577fb51807ff831e9bc5be232e1c4d7f4d2bbedd4cf7419bb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 21 Nov 2024 06:31:33 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1733097600'
# Thu, 21 Nov 2024 06:31:33 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 21 Nov 2024 06:31:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 21 Nov 2024 06:31:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 21 Nov 2024 06:31:33 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 21 Nov 2024 06:31:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 21 Nov 2024 06:31:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 21 Nov 2024 06:31:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 21 Nov 2024 06:31:33 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 21 Nov 2024 06:31:33 GMT
ENV PHP_VERSION=8.3.14
# Thu, 21 Nov 2024 06:31:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.14.tar.xz.asc
# Thu, 21 Nov 2024 06:31:33 GMT
ENV PHP_SHA256=58b4cb9019bf70c0cbcdb814c7df79b9065059d14cf7dbf48d971f8e56ae9be7
# Thu, 21 Nov 2024 06:31:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 21 Nov 2024 06:31:33 GMT
STOPSIGNAL SIGWINCH
# Thu, 21 Nov 2024 06:31:33 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
WORKDIR /var/www/html
# Thu, 21 Nov 2024 06:31:33 GMT
EXPOSE map[80/tcp:{}]
# Thu, 21 Nov 2024 06:31:33 GMT
CMD ["apache2-foreground"]
# Sat, 14 Dec 2024 11:07:50 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Sat, 14 Dec 2024 11:07:50 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Sat, 14 Dec 2024 11:07:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libicu-dev 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libmagickwand-dev 		libpq-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	pecl install APCu-5.1.23; 	pecl install memcached-3.3.0; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
VOLUME [/var/www/html]
# Sat, 14 Dec 2024 11:07:50 GMT
ENV JOOMLA_VERSION=5.2.1
# Sat, 14 Dec 2024 11:07:50 GMT
ENV JOOMLA_SHA512=87b2e1d01cf13458c5f24cfa7e5a092e087961c823fde8db6a5e5090bbef7e64a5e33900b3354a18d4ce7fc57d5d0719745fac3ec5597d7d44d91753ebd98c6a
# Sat, 14 Dec 2024 11:07:50 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/5.2.1/Joomla_5.2.1-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
COPY makedb.php /makedb.php # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 14 Dec 2024 11:07:50 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:e62b6946337cc6b72ec307008f1acc46e12a4f98e6f0e29c92b5538bbafd7ce6`  
		Last Modified: Tue, 03 Dec 2024 01:28:28 GMT  
		Size: 32.1 MB (32063265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dfd0832c6742842354605a68e1c37e01805dbd8dcb42bed521f3b5ffc9d6782`  
		Last Modified: Tue, 03 Dec 2024 03:01:38 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f8241edc102752205916990cef5c543934549ef471e4363e3f37b4d609359e`  
		Last Modified: Tue, 03 Dec 2024 03:01:42 GMT  
		Size: 103.1 MB (103128469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe6a6422bc6eb2d0ecc0d78cfc1ccb6571b1ef03bf7b17f2384e77abef0c849`  
		Last Modified: Tue, 03 Dec 2024 03:01:38 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be563cd21515e56438eeee24e165c5e6eb1efe06f45df830dbb193247c929683`  
		Last Modified: Tue, 03 Dec 2024 03:06:23 GMT  
		Size: 21.3 MB (21308386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34863b54186af36b092695264d86f35c3119978d70427455e85f6fd279681048`  
		Last Modified: Tue, 03 Dec 2024 03:06:23 GMT  
		Size: 435.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7b95b58340fb918a89b18f660a1045c0f902984f4cae1590b337184e865c1a`  
		Last Modified: Tue, 03 Dec 2024 03:06:23 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b36b12ea7855a4f5cc02ab5a21fed90aa6fdeb8e172e9f5ddb12207361aadb10`  
		Last Modified: Tue, 03 Dec 2024 03:22:58 GMT  
		Size: 12.6 MB (12648026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d9cf2577947f916a49bf8b682cd00ae9273a794be7c758adb0aca2d8f5ae709`  
		Last Modified: Tue, 03 Dec 2024 03:22:56 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e3a15fca22dbd0f787bc2c706234ffa6cbefbd219aba99588302ab2f085e8e`  
		Last Modified: Tue, 03 Dec 2024 03:22:57 GMT  
		Size: 12.1 MB (12064217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4dcd2cf193dc764293a488a6b7948c1e45c21572293bd9ccc9d627ff87fa8e6`  
		Last Modified: Tue, 03 Dec 2024 03:22:56 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf630f64cdf4c64eb83d88b5b604f18f9f3502cda5357559624fe6df4cc677e5`  
		Last Modified: Tue, 03 Dec 2024 03:22:57 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f2711004d906b8d821b04608d575be9905c6e99c496f5fb22e0e8f2b6ce6cd1`  
		Last Modified: Tue, 03 Dec 2024 03:22:57 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecc60e9b1c23f2c19397764834a07b35d701c0062eb4d2e354a7a23f9befbf87`  
		Last Modified: Mon, 16 Dec 2024 18:55:59 GMT  
		Size: 28.3 MB (28319483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:716eeff512ce0547941fa4ad56c12ab432f7867cb31134334f410fba80eb9e9d`  
		Last Modified: Mon, 16 Dec 2024 18:55:59 GMT  
		Size: 31.4 MB (31374369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2de962b0d384a463bb8c5a8dec8042c5486b8e81bd9ca704e152bc8039abd925`  
		Last Modified: Mon, 16 Dec 2024 18:55:58 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0015a83adcc864927a47423e5d1dfcb500e20bb5da346957301b5be18ae69150`  
		Last Modified: Mon, 16 Dec 2024 18:55:58 GMT  
		Size: 391.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31662a28d7b352788690797e509109dbc6863fbca05750329a1d7ff226c7122f`  
		Last Modified: Mon, 16 Dec 2024 18:55:59 GMT  
		Size: 19.2 KB (19160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9c1618dba69874eeb475eb16f139767e21ed85b36da8f56794940f702dba58`  
		Last Modified: Mon, 16 Dec 2024 18:56:00 GMT  
		Size: 23.8 MB (23775923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac25c5cd63be1917e41aad9e75f4cecaae5bb6d89324deaad0bcbaa73174677a`  
		Last Modified: Mon, 16 Dec 2024 18:56:00 GMT  
		Size: 3.7 KB (3655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03991eb975e952ea975057e569b6bcadb509ada38dd7af75f4c245c7c148fc2c`  
		Last Modified: Mon, 16 Dec 2024 18:56:00 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:5-php8.3-apache` - unknown; unknown

```console
$ docker pull joomla@sha256:c2f95259c2b9ec30e168747559b13d33113806d3d969eebfcc8815e365e574d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.9 KB (58915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d48fba7702ec44904542a41b9ca5dfc5022e01da66fd1f640f702df2e465998`

```dockerfile
```

-	Layers:
	-	`sha256:e4a19344b5210aeb6f6f8c45c6618d762a169e9ed435815882f8eb45c5b0bc14`  
		Last Modified: Mon, 16 Dec 2024 18:55:57 GMT  
		Size: 58.9 KB (58915 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:5-php8.3-apache` - linux; s390x

```console
$ docker pull joomla@sha256:3bf93ce8bfb11f399e30378cad90c5b000f6072fc7f04366df3fbb6598a644b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.4 MB (229375968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4ac0ab66db9ed5e7137772324e4ae083578b1dc9fdf959e5cde740cd416dc2e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 21 Nov 2024 06:31:33 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1733097600'
# Thu, 21 Nov 2024 06:31:33 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 21 Nov 2024 06:31:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 21 Nov 2024 06:31:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 21 Nov 2024 06:31:33 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 21 Nov 2024 06:31:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 21 Nov 2024 06:31:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 21 Nov 2024 06:31:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 21 Nov 2024 06:31:33 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 21 Nov 2024 06:31:33 GMT
ENV PHP_VERSION=8.3.14
# Thu, 21 Nov 2024 06:31:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.14.tar.xz.asc
# Thu, 21 Nov 2024 06:31:33 GMT
ENV PHP_SHA256=58b4cb9019bf70c0cbcdb814c7df79b9065059d14cf7dbf48d971f8e56ae9be7
# Thu, 21 Nov 2024 06:31:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 21 Nov 2024 06:31:33 GMT
STOPSIGNAL SIGWINCH
# Thu, 21 Nov 2024 06:31:33 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
WORKDIR /var/www/html
# Thu, 21 Nov 2024 06:31:33 GMT
EXPOSE map[80/tcp:{}]
# Thu, 21 Nov 2024 06:31:33 GMT
CMD ["apache2-foreground"]
# Sat, 14 Dec 2024 11:07:50 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Sat, 14 Dec 2024 11:07:50 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Sat, 14 Dec 2024 11:07:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libicu-dev 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libmagickwand-dev 		libpq-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	pecl install APCu-5.1.23; 	pecl install memcached-3.3.0; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
VOLUME [/var/www/html]
# Sat, 14 Dec 2024 11:07:50 GMT
ENV JOOMLA_VERSION=5.2.1
# Sat, 14 Dec 2024 11:07:50 GMT
ENV JOOMLA_SHA512=87b2e1d01cf13458c5f24cfa7e5a092e087961c823fde8db6a5e5090bbef7e64a5e33900b3354a18d4ce7fc57d5d0719745fac3ec5597d7d44d91753ebd98c6a
# Sat, 14 Dec 2024 11:07:50 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/5.2.1/Joomla_5.2.1-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
COPY makedb.php /makedb.php # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 14 Dec 2024 11:07:50 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:9378ae44108012049addde60d193467e2b15a247b2f953ad5c27e073c4573d42`  
		Last Modified: Tue, 03 Dec 2024 01:28:18 GMT  
		Size: 26.9 MB (26878971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ff6d88ca75be60fd842318e38796161d90dc699ddefddb72e584661cafccbb5`  
		Last Modified: Tue, 03 Dec 2024 02:45:09 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c1972b1cde205ce78e000379a6f103cc814e05cf048628db71370f4268b574`  
		Last Modified: Tue, 03 Dec 2024 02:45:10 GMT  
		Size: 80.6 MB (80624347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f0df81e218837c9a0821f00169675df65b6dc92a07a5e60fb03eb1b30c73673`  
		Last Modified: Tue, 03 Dec 2024 02:45:09 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81785c5e81e41257e9343844a3bb03f7c6b683f55e2dd07969f24adcc528917d`  
		Last Modified: Tue, 03 Dec 2024 02:49:17 GMT  
		Size: 19.9 MB (19895239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b912aab84041841b2de0edb1264346e4f5aa519009fc0ab560ea1b76d041e127`  
		Last Modified: Tue, 03 Dec 2024 02:49:17 GMT  
		Size: 437.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3ddea8579f46dc94efa149af85f249d1131297e7dcfce941798a62873eb5745`  
		Last Modified: Tue, 03 Dec 2024 02:49:17 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7a019423bbf4924612bacdb4fb32961bae808beb1a6bbbb0a2b2351d70f4632`  
		Last Modified: Tue, 03 Dec 2024 03:03:57 GMT  
		Size: 12.6 MB (12647106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b58be623527e52c6268e1bc48178a69489a19d8ca7947e04e7225ac949ce9ed`  
		Last Modified: Tue, 03 Dec 2024 03:03:57 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:944f5ab62e81231588ee6d2e4bfe7f5e8ccaf646e6382c8c0a6c4447c67bf5ce`  
		Last Modified: Tue, 03 Dec 2024 03:03:58 GMT  
		Size: 10.9 MB (10867061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9c246e2709d2d338dc489dae54e12bb063c07ebe0647d6178ff5ba45c4c9897`  
		Last Modified: Tue, 03 Dec 2024 03:03:57 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72c394ca57b6cc143ad4697bc1bf77b7409d239a324c0ee8f61a501d0073411e`  
		Last Modified: Tue, 03 Dec 2024 03:03:58 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0841cee2fbbd72ff56980fef3c1e955bf863b1a442877d8eecad48198b1c029f`  
		Last Modified: Tue, 03 Dec 2024 03:03:58 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d78a8f1b4639eea25300cb8cb8384d8e78b4eaa5f70e5f5e6d86a22c74e8dda`  
		Last Modified: Mon, 16 Dec 2024 19:19:29 GMT  
		Size: 26.7 MB (26698563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17385a3d3ec5645b129e723ba7cb8339f8962a73bf538496a2f27230aa4608f2`  
		Last Modified: Mon, 16 Dec 2024 19:19:29 GMT  
		Size: 28.0 MB (27958654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c80c4497720d841607d27c52bd52b7a4e0380651d3f9f2e8d210d7c2dc4026a5`  
		Last Modified: Mon, 16 Dec 2024 19:19:28 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe9d98f8a22f127b9b8309d5cacbae5ee3480de84e68c5f3ea9133da2591926e`  
		Last Modified: Mon, 16 Dec 2024 19:19:28 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a736eb3b1bc55117fcd382f1ea45f5fa288ae4bb79d7fe298aaa63e0ec8c7e8`  
		Last Modified: Mon, 16 Dec 2024 19:19:29 GMT  
		Size: 19.2 KB (19157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a83d6a79d44e8efdf031ce2375b13286abb56554b40672abe4a327b66463fabf`  
		Last Modified: Mon, 16 Dec 2024 19:19:30 GMT  
		Size: 23.8 MB (23775911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a99a3d6d01588d3f3468f54f5c9ab9f49a30fb10546203d0513a0e2ff59e18`  
		Last Modified: Mon, 16 Dec 2024 19:19:30 GMT  
		Size: 3.7 KB (3654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a424939eca2e8bc55eca465207508e893804c68cc43b31fa390d90c334d3931`  
		Last Modified: Mon, 16 Dec 2024 19:19:30 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:5-php8.3-apache` - unknown; unknown

```console
$ docker pull joomla@sha256:1ffa6676d9eefb8c86d016fa15e65d3b0ff46d5919067d51189dcb0e848e71a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.9 KB (58852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f4d4975a34a6e1f2c9401673ee044a4c45e94f73a70bff7d4b8b090a1fa0f97`

```dockerfile
```

-	Layers:
	-	`sha256:2d3c16431e7ca5a953604de18c035013fd784546a8d574fe1282a8a2ec992142`  
		Last Modified: Mon, 16 Dec 2024 19:19:27 GMT  
		Size: 58.9 KB (58852 bytes)  
		MIME: application/vnd.in-toto+json
