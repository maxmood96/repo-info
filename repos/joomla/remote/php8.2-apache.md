## `joomla:php8.2-apache`

```console
$ docker pull joomla@sha256:0249c0807ea9930c8bfc0c781ffc0176718f2558a9d7da77e32d6d059ed070e7
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

### `joomla:php8.2-apache` - linux; amd64

```console
$ docker pull joomla@sha256:e2ddcfe02190a0511a70852437eca84adab4e86f873cf3447cb1246b0b835a80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.4 MB (258430371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:301c0f7edf3ecb7344916b4e8c8eb9a66f2dc69e9b1f341cd980d5928702d0e5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 14 Dec 2024 11:07:50 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Sat, 14 Dec 2024 11:07:50 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 14 Dec 2024 11:07:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 14 Dec 2024 11:07:50 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 14 Dec 2024 11:07:50 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 14 Dec 2024 11:07:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Dec 2024 11:07:50 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Dec 2024 11:07:50 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 14 Dec 2024 11:07:50 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Sat, 14 Dec 2024 11:07:50 GMT
ENV PHP_VERSION=8.2.27
# Sat, 14 Dec 2024 11:07:50 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.27.tar.xz.asc
# Sat, 14 Dec 2024 11:07:50 GMT
ENV PHP_SHA256=3eec91294d8c09b3df80b39ec36d574ed9b05de4c8afcb25fa215d48f9ecbc6b
# Sat, 14 Dec 2024 11:07:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 14 Dec 2024 11:07:50 GMT
STOPSIGNAL SIGWINCH
# Sat, 14 Dec 2024 11:07:50 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
WORKDIR /var/www/html
# Sat, 14 Dec 2024 11:07:50 GMT
EXPOSE map[80/tcp:{}]
# Sat, 14 Dec 2024 11:07:50 GMT
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
	-	`sha256:fd674058ff8f8cfa7fb8a20c006fc0128541cbbad7f7f7f28df570d08f9e4d92`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 28.2 MB (28231581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e012f699cbd9273b388a7fbfc0b21efc1bdeb04f7df29ec80f7bcdeb121d0f3`  
		Last Modified: Tue, 24 Dec 2024 22:27:46 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b35ca6db0b590e7336826719479a1e7045ca7b15f21c4802f6d018d1a7bc4f2`  
		Last Modified: Tue, 24 Dec 2024 22:27:49 GMT  
		Size: 104.2 MB (104150581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:704dee2cabd95abf754c0bcd6ef508f366072cde5bb0b546a9d6133f85d6c378`  
		Last Modified: Tue, 24 Dec 2024 22:27:46 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fdb0e4d812c45b9da22137e86160e20cdf24df893c9774daf9695f31e32bbda`  
		Last Modified: Tue, 24 Dec 2024 22:27:47 GMT  
		Size: 20.1 MB (20123833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd696393bc53da5f966d385701e747ffc637f417b5026a4391d231e743948804`  
		Last Modified: Tue, 24 Dec 2024 22:27:47 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b7af5ff0c1b8c9ad7df3530715022299b19db7a92311552453896707abc05de`  
		Last Modified: Tue, 24 Dec 2024 22:27:47 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:384588a3de49c62bf93e6cf6762d768cdb994696b6c7fcea0632d8ed51838b48`  
		Last Modified: Tue, 24 Dec 2024 22:27:49 GMT  
		Size: 12.3 MB (12279759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bfa95b81973cf7a7eca458dfee4d3b9b00d7c689ffe53722c61fb3e9cbe2d47`  
		Last Modified: Tue, 24 Dec 2024 22:27:48 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b24a3aff350b1108eb63792b66ac243366b39df3a43a1cd4712abae46fcfe569`  
		Last Modified: Tue, 24 Dec 2024 22:27:49 GMT  
		Size: 11.4 MB (11419198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eecbcdb9e3e3e2408c8054dd0f19c2cbbcf1be3c8e212da9e0066f7cc5aaa0c6`  
		Last Modified: Tue, 24 Dec 2024 22:27:49 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fabbb9254aa42925ff07ca289db225b52869be67213af84aeaac46d69233e0d4`  
		Last Modified: Tue, 24 Dec 2024 22:27:50 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f45d2a5ba4b877aac16515fa22cfd4a02033a212ceba0ea6183cb33331e76546`  
		Last Modified: Tue, 24 Dec 2024 22:27:50 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1a56a822ea3c540e8d5071e42bbb561ee8c30ae59968579f7fbb694fb8b984b`  
		Last Modified: Tue, 24 Dec 2024 23:18:53 GMT  
		Size: 27.2 MB (27160006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bef021300e050c7d20e00428b04afcdca755a7e195421a6f25efb5534485af7c`  
		Last Modified: Tue, 24 Dec 2024 23:18:53 GMT  
		Size: 31.3 MB (31259383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b5cab2618f8afdaec55784f873ce1021526576c37bfb8253d73cc51dc8c605`  
		Last Modified: Tue, 24 Dec 2024 23:18:52 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c70550bf0b2320f154b1a40caad1cbd5464380c5905a8190afd2d01a01eaaa06`  
		Last Modified: Tue, 24 Dec 2024 23:18:52 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0525b040b8026be752141a6d5a3e5ad173bc6cc308096d4500d46a9ebc9d1155`  
		Last Modified: Tue, 24 Dec 2024 23:18:53 GMT  
		Size: 19.2 KB (19168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5b656ebbff55860cc878fab9a375188c0f77d188c5e53cadc6911bfee17c837`  
		Last Modified: Tue, 24 Dec 2024 23:18:54 GMT  
		Size: 23.8 MB (23775911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66d16a643fd88763e9db701775be39b3deb55b0da2ddb2dade7fb295dc11e269`  
		Last Modified: Tue, 24 Dec 2024 23:18:54 GMT  
		Size: 3.7 KB (3656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eb83a152674766265d37e48c847a0853a6ac5b4a370bf133c705f76bededeb5`  
		Last Modified: Tue, 24 Dec 2024 23:18:54 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:php8.2-apache` - unknown; unknown

```console
$ docker pull joomla@sha256:36d13ea3800ad7d974954d0c9bca32e586da632692dd4b98ca21f42835a80b8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.5 KB (62468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f201e1cbb026a545356361c26c43ea5ae5e1d9a6733f70012d47964488ba32d9`

```dockerfile
```

-	Layers:
	-	`sha256:79026fe16cfb02c75fe06ad12056b6094a7437e0cde3ea8e806fe9772f03da1d`  
		Last Modified: Tue, 24 Dec 2024 23:18:51 GMT  
		Size: 62.5 KB (62468 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:php8.2-apache` - linux; arm variant v5

```console
$ docker pull joomla@sha256:4070fb66ed8ba86391b2d9a003b22a98c32ca152182f1e940d48056604667ce1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.0 MB (228042480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:355f4205edcfc718ac1e6e83e60ebc161263d9a99ee4300e8b608ea9da801d34`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 14 Dec 2024 11:07:50 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1734912000'
# Sat, 14 Dec 2024 11:07:50 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 14 Dec 2024 11:07:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 14 Dec 2024 11:07:50 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 14 Dec 2024 11:07:50 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 14 Dec 2024 11:07:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Dec 2024 11:07:50 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Dec 2024 11:07:50 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 14 Dec 2024 11:07:50 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Sat, 14 Dec 2024 11:07:50 GMT
ENV PHP_VERSION=8.2.27
# Sat, 14 Dec 2024 11:07:50 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.27.tar.xz.asc
# Sat, 14 Dec 2024 11:07:50 GMT
ENV PHP_SHA256=3eec91294d8c09b3df80b39ec36d574ed9b05de4c8afcb25fa215d48f9ecbc6b
# Sat, 14 Dec 2024 11:07:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 14 Dec 2024 11:07:50 GMT
STOPSIGNAL SIGWINCH
# Sat, 14 Dec 2024 11:07:50 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
WORKDIR /var/www/html
# Sat, 14 Dec 2024 11:07:50 GMT
EXPOSE map[80/tcp:{}]
# Sat, 14 Dec 2024 11:07:50 GMT
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
	-	`sha256:61230a432de02dc9fd57340d88179517d7f651caeb2a5e2fa6ec333d17ed65c5`  
		Last Modified: Tue, 24 Dec 2024 21:33:31 GMT  
		Size: 25.8 MB (25754907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa953064c1f89dc77f80b9dbecc99eff2f7058550fbf33d1224feeafffa4c982`  
		Last Modified: Tue, 24 Dec 2024 22:51:18 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27de1993da0104dd0a7499144d0ad47670b8a876dfdc92326d69d7764f7bdb83`  
		Last Modified: Tue, 24 Dec 2024 22:51:21 GMT  
		Size: 81.8 MB (81799570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:493cadeebee57b8879f2510778f06bb61de8a8ec4c9c482ec5f69046e77af0bd`  
		Last Modified: Tue, 24 Dec 2024 22:51:18 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1531c6e1be970012e02dcc118113c21cc406e277492355c5cd9dab14c78d473`  
		Last Modified: Tue, 24 Dec 2024 22:56:05 GMT  
		Size: 19.4 MB (19418909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:705efd3d3a5c39886ed5460e6efef4b2a57c0ce12db2d040b215eb3613307f20`  
		Last Modified: Tue, 24 Dec 2024 22:56:04 GMT  
		Size: 432.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d21857967a1eaa683559839ed390ddc835d501ea87442daa37df7944ca079a8`  
		Last Modified: Tue, 24 Dec 2024 22:56:05 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d529ac17332520cba0fcd851df99af0f21a440ac726869a69308c4baad99a4f8`  
		Last Modified: Tue, 24 Dec 2024 23:26:25 GMT  
		Size: 12.3 MB (12277668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6c20840cc3e06cebd69c1cec18130bd61b3fabf0af9e21f5c80031ffa7534b9`  
		Last Modified: Tue, 24 Dec 2024 23:26:24 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65b41f7da8f5c053cd8de04808ceb6a8a11ed85647aefcd989c7c1d29f3569e8`  
		Last Modified: Tue, 24 Dec 2024 23:26:25 GMT  
		Size: 10.4 MB (10403940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11adb20d7d41da3d0b6cc63d78ea6f0239d0040fd0fe8625fee46e9d2a8f9a94`  
		Last Modified: Tue, 24 Dec 2024 23:26:24 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcee2eb427187ff7912108f104b7640e6c5e1b2273bfafde0cebfc5ccc46b8e7`  
		Last Modified: Tue, 24 Dec 2024 23:26:25 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b6d80c79b1e15c06f2adc26dcac96826e9d45bf9d02b59d9c115164555ac222`  
		Last Modified: Tue, 24 Dec 2024 23:26:25 GMT  
		Size: 895.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50a7a053ad52411e72b65ab105a9db8261e645dc34eac2061a7b8487378b1089`  
		Last Modified: Wed, 25 Dec 2024 05:05:30 GMT  
		Size: 26.6 MB (26615071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0bb282bc824d91bcc42bfd1935bc1b7057a79603eff7a4ba79da3d235215877`  
		Last Modified: Wed, 25 Dec 2024 05:05:30 GMT  
		Size: 28.0 MB (27966371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:292c1115c4faed84dc11500999f02f6a5e3590c91aec369c03badd9c1d6223bc`  
		Last Modified: Wed, 25 Dec 2024 05:05:29 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4ea2df2e25b382c0184d0b05ecbf74f9d7a68ca21c85b9df8c58456eea48f42`  
		Last Modified: Wed, 25 Dec 2024 05:05:29 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b0a0de39d68debf0adbf26dba6fdb9d124ad251f51a1e3a9ee8cb0eb57ef88c`  
		Last Modified: Wed, 25 Dec 2024 05:05:30 GMT  
		Size: 19.2 KB (19158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ce2420c8223d81dc729d1940048721594fe590d09af93cbc39cd3b08bc1927`  
		Last Modified: Wed, 25 Dec 2024 05:05:31 GMT  
		Size: 23.8 MB (23775922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9a7bd671a7431c8278583e4273d27e57ea165fa7bcd8d93e3eb35799b898706`  
		Last Modified: Mon, 16 Dec 2024 18:38:58 GMT  
		Size: 3.7 KB (3655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1973d1816104e9d01410954028c79c85382787bd4df5f7eb4bb62a262b76181`  
		Last Modified: Mon, 16 Dec 2024 18:38:58 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:php8.2-apache` - unknown; unknown

```console
$ docker pull joomla@sha256:b3535213a6d71ad3ba1ba04513885cbb5e8d8e6626a1ec1cfe438737dd3e82ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.7 KB (62696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39fe0abebca860d07330508bc84b72d622c3f56d490dee34e854aa020eb271f4`

```dockerfile
```

-	Layers:
	-	`sha256:5a4abba883256e67f23a11f3a8cab983dc422a986aabdb016269171e55f81636`  
		Last Modified: Wed, 25 Dec 2024 05:05:29 GMT  
		Size: 62.7 KB (62696 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:php8.2-apache` - linux; arm variant v7

```console
$ docker pull joomla@sha256:c3d32505967bac3c521cd261552fe7f00fba69313941033a02ffc11add125702
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.9 MB (216901832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d911e40e45e486c2338d79a1664b99f6c8addfbf8aec60b0de445cbcc2220998`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 14 Dec 2024 11:07:50 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1734912000'
# Sat, 14 Dec 2024 11:07:50 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 14 Dec 2024 11:07:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 14 Dec 2024 11:07:50 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 14 Dec 2024 11:07:50 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 14 Dec 2024 11:07:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Dec 2024 11:07:50 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Dec 2024 11:07:50 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 14 Dec 2024 11:07:50 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Sat, 14 Dec 2024 11:07:50 GMT
ENV PHP_VERSION=8.2.27
# Sat, 14 Dec 2024 11:07:50 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.27.tar.xz.asc
# Sat, 14 Dec 2024 11:07:50 GMT
ENV PHP_SHA256=3eec91294d8c09b3df80b39ec36d574ed9b05de4c8afcb25fa215d48f9ecbc6b
# Sat, 14 Dec 2024 11:07:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 14 Dec 2024 11:07:50 GMT
STOPSIGNAL SIGWINCH
# Sat, 14 Dec 2024 11:07:50 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
WORKDIR /var/www/html
# Sat, 14 Dec 2024 11:07:50 GMT
EXPOSE map[80/tcp:{}]
# Sat, 14 Dec 2024 11:07:50 GMT
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
	-	`sha256:24f0da30a772db626789cda3e7b0911098d07574c40b30be943d43dec3ed685f`  
		Last Modified: Tue, 24 Dec 2024 21:33:51 GMT  
		Size: 23.9 MB (23933522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f371487cffce8356bcfafa73641fa9f2323f8772bee294bab86eafd60098c3fa`  
		Last Modified: Tue, 24 Dec 2024 22:46:18 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4642677cc143257aa73de7964d6b5cc5b6060d2a6edb9a5ddd3be8f1945443b`  
		Last Modified: Tue, 24 Dec 2024 22:46:20 GMT  
		Size: 76.0 MB (75969024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfc80a55774350869ee992b98dcd86030b72390bb6be124ca4de61219527683e`  
		Last Modified: Tue, 24 Dec 2024 22:46:18 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25a47f58182addfc006a08b0f176b99027cafa95cbb11bd8c2a67cea998652ef`  
		Last Modified: Tue, 24 Dec 2024 22:51:10 GMT  
		Size: 18.9 MB (18857375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:489299adde02364094cf7b587949e62efb94af380c86790375890e5970e48964`  
		Last Modified: Tue, 24 Dec 2024 22:51:09 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f182d84621ff8030b0063e0c13b0e085d2c01da0e1058aaf33a38c64516b003`  
		Last Modified: Tue, 24 Dec 2024 22:51:09 GMT  
		Size: 481.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:793c0df89f098015dc866ff09c9050986c0bbb3180ff4851b1d12eadea564a19`  
		Last Modified: Tue, 24 Dec 2024 23:49:19 GMT  
		Size: 12.3 MB (12277641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f5847a4e28be839305e6fb6ef16c7973b9eee98601f1bd7be8fd7e91f4adf9f`  
		Last Modified: Tue, 24 Dec 2024 23:49:19 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b098673c36cdffc51485f6c4fce187b8a51d161f07107a76dd668030b44c857`  
		Last Modified: Tue, 24 Dec 2024 23:49:19 GMT  
		Size: 9.8 MB (9833488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0d94024d8bab5720087b618fcc3c26afe2d8c5cde4d83f91856ff2dbb37cada`  
		Last Modified: Tue, 24 Dec 2024 23:49:19 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aa5dd6b11eb386136c376f3237dcf7d37c575c8deb73bedcce89827233a53aa`  
		Last Modified: Tue, 24 Dec 2024 23:49:20 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25f693d47c5980b5322cb24c9d0b3dc6150fb62ef64bc86936df9bddafaaea05`  
		Last Modified: Tue, 24 Dec 2024 23:49:20 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b2676a90bfa4c42ed631ab3546aeca192da4e70149b6f3aca0282df02737c8`  
		Last Modified: Wed, 25 Dec 2024 13:47:01 GMT  
		Size: 25.8 MB (25848566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85717283959fe5f3639f65519e24522b2fef2ceab0428e036eb862e0b26ec340`  
		Last Modified: Wed, 25 Dec 2024 13:47:01 GMT  
		Size: 26.4 MB (26376204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82f59107ba284a51b24c4f2e43cc000e568cf91f77ac5fa0cb72dbfaaa60bae7`  
		Last Modified: Wed, 25 Dec 2024 13:47:00 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0d8123f128ffa8a8d2621e9b0d9a00927dcf45f212934541e4c88cebd8a3861`  
		Last Modified: Wed, 25 Dec 2024 13:47:00 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cec3983f9b9117a91068c991caf2d4524b77358dfa789b9f10b07afc9be27ce4`  
		Last Modified: Wed, 25 Dec 2024 13:47:01 GMT  
		Size: 19.2 KB (19151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7b548b71d528945035695d99b887767b997e9a926a6b8d5ad2fd54ad574a216`  
		Last Modified: Wed, 25 Dec 2024 13:47:02 GMT  
		Size: 23.8 MB (23775914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fd94400f71502321f53a6b3a3670bf524f313f6ddee0a6a305e0abab01aa27c`  
		Last Modified: Wed, 25 Dec 2024 13:47:02 GMT  
		Size: 3.7 KB (3655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a55567f0d63ce44d27e8f47c79f3f2f18a53548b8796d84b2a4ec6dff5c433df`  
		Last Modified: Wed, 25 Dec 2024 13:47:02 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:php8.2-apache` - unknown; unknown

```console
$ docker pull joomla@sha256:89493f58850423b51da010b0b7d451fe928671a7d0cfca8a6b91a42310dbc4b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.7 KB (62687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:684d352958dcae36cf43804beec7ff16a26632205f65e1d850317837e35c509d`

```dockerfile
```

-	Layers:
	-	`sha256:c0dea6a54b2b6781a725e0ba04f05b277645a93022ea586f87b191c1cd1c3b34`  
		Last Modified: Wed, 25 Dec 2024 13:47:00 GMT  
		Size: 62.7 KB (62687 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:php8.2-apache` - linux; arm64 variant v8

```console
$ docker pull joomla@sha256:b476b78851c463d50ddf3ab86354410f6c6fc1945d7dfd69a1a22dc91d0876ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.5 MB (249485129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c63f7b3952a9926593ce007e420c588e6f742ae8a97daaf64b372b63b19b453`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 14 Dec 2024 11:07:50 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Sat, 14 Dec 2024 11:07:50 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 14 Dec 2024 11:07:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 14 Dec 2024 11:07:50 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 14 Dec 2024 11:07:50 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 14 Dec 2024 11:07:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Dec 2024 11:07:50 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Dec 2024 11:07:50 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 14 Dec 2024 11:07:50 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Sat, 14 Dec 2024 11:07:50 GMT
ENV PHP_VERSION=8.2.27
# Sat, 14 Dec 2024 11:07:50 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.27.tar.xz.asc
# Sat, 14 Dec 2024 11:07:50 GMT
ENV PHP_SHA256=3eec91294d8c09b3df80b39ec36d574ed9b05de4c8afcb25fa215d48f9ecbc6b
# Sat, 14 Dec 2024 11:07:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 14 Dec 2024 11:07:50 GMT
STOPSIGNAL SIGWINCH
# Sat, 14 Dec 2024 11:07:50 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
WORKDIR /var/www/html
# Sat, 14 Dec 2024 11:07:50 GMT
EXPOSE map[80/tcp:{}]
# Sat, 14 Dec 2024 11:07:50 GMT
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
	-	`sha256:f5c6876bb3d7d368455916fa98c705330bd8a8d9c080ccea8fe4c4b35a2ecb1f`  
		Last Modified: Tue, 24 Dec 2024 21:34:20 GMT  
		Size: 28.1 MB (28058723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6de54321d531850ff87c6246d4017603a5b45913b21b1ac9fec3f05fbfef635`  
		Last Modified: Tue, 24 Dec 2024 23:07:21 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bdf08462934214f25431962b05d5cacd6c3f869869f8db5363e56c95c2bc31`  
		Last Modified: Tue, 24 Dec 2024 23:07:23 GMT  
		Size: 97.9 MB (97936231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f9687803207cdc9b6efb7871b95e27621a8a6b095ab542b254f0ecc6d9f697b`  
		Last Modified: Tue, 24 Dec 2024 23:07:21 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c85655b9cbf2eb17eb8b5f60129702dc98ba0a66c0702618db93a9ccc8124a`  
		Last Modified: Tue, 24 Dec 2024 23:11:04 GMT  
		Size: 20.1 MB (20120902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c19158f224f42298adef7b5830217f5a6d43a9e3025997c52bf103c2099eeac3`  
		Last Modified: Tue, 24 Dec 2024 23:11:03 GMT  
		Size: 432.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28e3a6b915cc6eda19b3e2bc89aadd18d243bb9a1c06307453f890619d373a20`  
		Last Modified: Tue, 24 Dec 2024 23:11:03 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46740b6b502d21fa205498eb0f5ccc989623f5f65f27ac24a4a040ad4cdcfaa9`  
		Last Modified: Wed, 25 Dec 2024 00:09:19 GMT  
		Size: 12.3 MB (12279567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bdaab51464db6186dcae478cd875364c8cd471bf69b11b45dfb9cfa8f5d6c39`  
		Last Modified: Wed, 25 Dec 2024 00:09:18 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01e3754cc78f0880109595159519013e1dcb2d541b664a5e8ddcbddc67081456`  
		Last Modified: Wed, 25 Dec 2024 00:09:19 GMT  
		Size: 11.4 MB (11427319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61f407de387460420e7b4f0f9d797a74be4a646351b12b68987307b55993a98f`  
		Last Modified: Wed, 25 Dec 2024 00:09:18 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe9e7b7d77899b1cf3a70f79841504a107ab90aa4138c3208ec2b27dc7700269`  
		Last Modified: Wed, 25 Dec 2024 00:09:19 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8ae8e00fd3d31eb79cad7c1c9c2167308a4c2d2fef0e74765d5ef037fce4bb2`  
		Last Modified: Wed, 25 Dec 2024 00:09:19 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a89b44ece6c054098b12322d7f6538193805789d339710e30cf7d543ba3a9b96`  
		Last Modified: Wed, 25 Dec 2024 09:13:51 GMT  
		Size: 27.0 MB (26988676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da7ff4b7122c03b3641cd4273e17a380a04d929e968681152ba59dc078b3ac8`  
		Last Modified: Wed, 25 Dec 2024 09:13:51 GMT  
		Size: 28.9 MB (28867693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31e594e4b5126327254495f521a548fa8862e6cb1e154102e1b7821aa6d6ee05`  
		Last Modified: Wed, 25 Dec 2024 09:13:50 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aff542715c1f24799826413354eb0037accd96906b9c92343d501ec9a674d10`  
		Last Modified: Wed, 25 Dec 2024 09:13:50 GMT  
		Size: 391.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b71f757a10937aae64c6b28cafa14c7ee8a162eea528b61b54bce8638cba3a88`  
		Last Modified: Wed, 25 Dec 2024 09:13:51 GMT  
		Size: 19.2 KB (19158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5e3465d175903b26f87e000915d8a12c9ec4c59613dd9d46c4c173e65968e78`  
		Last Modified: Wed, 25 Dec 2024 09:13:52 GMT  
		Size: 23.8 MB (23775911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cfa5fa5c6b5e35540d490c5c1412f3c4f41707b08b3c4367fff24535aa040fb`  
		Last Modified: Wed, 25 Dec 2024 09:13:52 GMT  
		Size: 3.7 KB (3656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d46c64341cd73cfef5af473ff3a1353fa8c96862acefc2d96153d62cb618d3d2`  
		Last Modified: Wed, 25 Dec 2024 09:13:52 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:php8.2-apache` - unknown; unknown

```console
$ docker pull joomla@sha256:2beab538e271003424cc68771114dd015e476ca56f58c3e0bfbe42d63714be9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.8 KB (62782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d97266e043dbcf11a4aae6fc529ee24b866704c4c41872613876ef065e8e387`

```dockerfile
```

-	Layers:
	-	`sha256:ae674aa8b43ec9e0b97ee1a7eee2736e84e7e0d4cd040971d758ebb381261e74`  
		Last Modified: Wed, 25 Dec 2024 09:13:50 GMT  
		Size: 62.8 KB (62782 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:php8.2-apache` - linux; 386

```console
$ docker pull joomla@sha256:a777af541ef9feacdcca2ea6968c9e012850909fd784f918cad8387be744b999
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.0 MB (256984509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1eddd0a7f4b8f063c8b8f5b3525d37246183431871ec74c85d84754513b04fc5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 14 Dec 2024 11:07:50 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1734912000'
# Sat, 14 Dec 2024 11:07:50 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 14 Dec 2024 11:07:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 14 Dec 2024 11:07:50 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 14 Dec 2024 11:07:50 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 14 Dec 2024 11:07:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Dec 2024 11:07:50 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Dec 2024 11:07:50 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 14 Dec 2024 11:07:50 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Sat, 14 Dec 2024 11:07:50 GMT
ENV PHP_VERSION=8.2.27
# Sat, 14 Dec 2024 11:07:50 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.27.tar.xz.asc
# Sat, 14 Dec 2024 11:07:50 GMT
ENV PHP_SHA256=3eec91294d8c09b3df80b39ec36d574ed9b05de4c8afcb25fa215d48f9ecbc6b
# Sat, 14 Dec 2024 11:07:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 14 Dec 2024 11:07:50 GMT
STOPSIGNAL SIGWINCH
# Sat, 14 Dec 2024 11:07:50 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
WORKDIR /var/www/html
# Sat, 14 Dec 2024 11:07:50 GMT
EXPOSE map[80/tcp:{}]
# Sat, 14 Dec 2024 11:07:50 GMT
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
	-	`sha256:fba9c0797a7b5bba079e0fd9d815a8878aea58430ea12c84047010f98fbe34d7`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 29.2 MB (29205387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fc64c0b0d1a66b75da26e50378599150d7f43d8fd00aa98aa5a5336298675fa`  
		Last Modified: Tue, 24 Dec 2024 22:24:42 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51d6894a607b7c07c5598ffa6f21264b4118f909d290075b267505ef3b1213b0`  
		Last Modified: Tue, 24 Dec 2024 22:24:45 GMT  
		Size: 101.3 MB (101320342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:276f6ba0c29ec20863212d5d4f7052d4a135dd5edc200c4108c7a7f951e21590`  
		Last Modified: Tue, 24 Dec 2024 22:24:42 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05fcb49270809cb3fa9c8f817dd3f2817b225436d85dbb1e907903fe2aa30b71`  
		Last Modified: Tue, 24 Dec 2024 22:24:43 GMT  
		Size: 20.6 MB (20638442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90ae9500275a664ab056c13c5864414a1c8e0ac4a2c72e546a8b6203d8ce3655`  
		Last Modified: Tue, 24 Dec 2024 22:24:43 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:668e07532948f09c40e7868fd11e46c4d51b2d404413b0695460bb69526b713f`  
		Last Modified: Tue, 24 Dec 2024 22:24:43 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11493bf426ced066d7909c795bc6e95947b93bbcdf6fd7ec32ad4020fe08bd45`  
		Last Modified: Tue, 24 Dec 2024 22:24:45 GMT  
		Size: 12.3 MB (12278770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76b743f157bac725236ce1a9c995bccd51e5a12e4df04ea5c86f3bafcc5d12a0`  
		Last Modified: Tue, 24 Dec 2024 22:24:44 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d1a16b05104fc6172cc380346138d8a8bfb50361646c26288f0044e4ba1c27`  
		Last Modified: Tue, 24 Dec 2024 22:24:45 GMT  
		Size: 11.6 MB (11646829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc81d007068286fe0f173b041b21b9c50e500eaea95db80cf3edb6445f5f8da5`  
		Last Modified: Tue, 24 Dec 2024 22:24:45 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b5e3d17321576f568523dff0bb4dd11c1558f31629618f03991c236aae29b98`  
		Last Modified: Tue, 24 Dec 2024 22:24:46 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d39dfe501dcaa71769732d98d5485fbdd42bed49ce7fc23eb9a2ef9d01fa65c`  
		Last Modified: Tue, 24 Dec 2024 22:24:46 GMT  
		Size: 888.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcd6b50f0b7fa33c72c5f0d3c603b80ba183a767948791d14251cecf0c69bbfd`  
		Last Modified: Tue, 24 Dec 2024 23:23:05 GMT  
		Size: 27.5 MB (27524274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34523982bf7d3bbba3be6feb7f6ac0b350c065c276c23dd701c5bb0cdad51027`  
		Last Modified: Tue, 24 Dec 2024 23:23:06 GMT  
		Size: 30.6 MB (30564460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:613a7c268b6226db3aa6f19529356dd9334dc7406799b191522e92d5cda74e0e`  
		Last Modified: Tue, 24 Dec 2024 23:23:05 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c6fb2b7be47311e644ab71e029a11aa940b9e48f8889457b8830e550f314f6a`  
		Last Modified: Tue, 24 Dec 2024 23:23:04 GMT  
		Size: 391.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1077cabd6b3e05d5c173261705d4e2fa99a1f46c68e99927688d25505d14ae1`  
		Last Modified: Tue, 24 Dec 2024 23:23:05 GMT  
		Size: 19.1 KB (19150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c72f73c70f2141a068b108c33d6e395396b26e4e9b6dce6f78c81038abdbb6b`  
		Last Modified: Tue, 24 Dec 2024 23:23:07 GMT  
		Size: 23.8 MB (23775911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7be0ea3da0471280e37c488070136ca553c6513448f5d7b6dd7545fe078d564c`  
		Last Modified: Tue, 24 Dec 2024 23:23:06 GMT  
		Size: 3.7 KB (3656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14cf445820a9051e1008e6c27b69426a98d70754efffa542f93664df7c0f6aac`  
		Last Modified: Tue, 24 Dec 2024 23:23:07 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:php8.2-apache` - unknown; unknown

```console
$ docker pull joomla@sha256:f518c17eba1e8115f3a1130bc684efef9d4db0ee95a748d9e583e69888018761
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 KB (62366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0004fb0eb4fa41d8880fcad1938d97b7cf5d0863eb04695dd2b6be2fe30a9ab3`

```dockerfile
```

-	Layers:
	-	`sha256:f3ea1d418a81fe63236dad6e9ccf7c7c873295de6076ea4a6bd1216937528a0b`  
		Last Modified: Tue, 24 Dec 2024 23:23:04 GMT  
		Size: 62.4 KB (62366 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:php8.2-apache` - linux; mips64le

```console
$ docker pull joomla@sha256:45a09224ad25fb0386830b45501bc53a1149858fffecc03bc04c744682bb1d71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.1 MB (231118652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:918e1ff9b29bb84f7ff06a06101f9f92f86ccf819d0863596d4c5656a66d96e6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1733097600'
# Sat, 14 Dec 2024 11:07:50 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 14 Dec 2024 11:07:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 14 Dec 2024 11:07:50 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 14 Dec 2024 11:07:50 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 14 Dec 2024 11:07:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Dec 2024 11:07:50 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Dec 2024 11:07:50 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 14 Dec 2024 11:07:50 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Sat, 14 Dec 2024 11:07:50 GMT
ENV PHP_VERSION=8.2.27
# Sat, 14 Dec 2024 11:07:50 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.27.tar.xz.asc
# Sat, 14 Dec 2024 11:07:50 GMT
ENV PHP_SHA256=3eec91294d8c09b3df80b39ec36d574ed9b05de4c8afcb25fa215d48f9ecbc6b
# Sat, 14 Dec 2024 11:07:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 14 Dec 2024 11:07:50 GMT
STOPSIGNAL SIGWINCH
# Sat, 14 Dec 2024 11:07:50 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
WORKDIR /var/www/html
# Sat, 14 Dec 2024 11:07:50 GMT
EXPOSE map[80/tcp:{}]
# Sat, 14 Dec 2024 11:07:50 GMT
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
	-	`sha256:54b9aedec0de3569e1ddfcbd9ab5764de6f25144761b1c7b6218bd140b1957ee`  
		Last Modified: Sat, 21 Dec 2024 00:24:45 GMT  
		Size: 12.3 MB (12277260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6166efb722f6eec588b364fae89e9836c90f2dac306b3b6c508a3d6a7d90d545`  
		Last Modified: Sat, 21 Dec 2024 00:24:43 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f862b01222f4c229a81493e3a935e586d01f64cbc4c03acef774fc1084a2ab`  
		Last Modified: Sat, 21 Dec 2024 00:24:45 GMT  
		Size: 10.5 MB (10497791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9e4695df2e8362cfb1821a012517364c0f8c2e7e0548cd0d3b96e6b2cb1d3f3`  
		Last Modified: Sat, 21 Dec 2024 00:24:43 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:613b7f4b226ffd065741b2c1b7c73fa662dcaf3ee99af361dfb4bdf9a0c31de1`  
		Last Modified: Sat, 21 Dec 2024 00:24:44 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:772bc94cbaab9510d682c88ff10c8d50d0f3c795d6720b2846827d742df89003`  
		Last Modified: Sat, 21 Dec 2024 00:24:44 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ae674f6c7aa26af0a4a36a7e9be2bc141aef0208638838208827c1a476113b7`  
		Last Modified: Sat, 21 Dec 2024 03:25:55 GMT  
		Size: 26.9 MB (26913267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b05a62bfe13ccefeb228a40f997526aa7805f12db257ba41341c8ec73052039`  
		Last Modified: Sat, 21 Dec 2024 03:25:55 GMT  
		Size: 28.6 MB (28574128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc2e9e679e163c189a61e21ac949144408b17f4ce10f64d9fe9a37d42c32755f`  
		Last Modified: Sat, 21 Dec 2024 03:25:52 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:602054aece8c2d6f009148d32dbd3189250317ca7f53f5947ec59bd66940ff78`  
		Last Modified: Sat, 21 Dec 2024 03:25:52 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be3e3b4e480a637b71f6477e3ad9d0639040d512e094f70a455eaa6e40ffb78c`  
		Last Modified: Sat, 21 Dec 2024 03:25:53 GMT  
		Size: 19.2 KB (19166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95da8716cde1d8b3a1886013035811226446cc645a2888e62c8f0439a8eb9579`  
		Last Modified: Sat, 21 Dec 2024 03:25:56 GMT  
		Size: 23.8 MB (23775924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:996c532c1b394e32d400a721b2812a3c0fe20387862133357823a170d2f60c3e`  
		Last Modified: Mon, 16 Dec 2024 19:11:14 GMT  
		Size: 3.7 KB (3655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7378eaf5e9ff359bc07de099262b03aeb86e2af01a6c29e2cf7ecd192435772`  
		Last Modified: Mon, 16 Dec 2024 19:11:14 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:php8.2-apache` - unknown; unknown

```console
$ docker pull joomla@sha256:34c510b280435136e55ba00c105c7bd044edc8e256d763173e1f2e2573be33bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.6 KB (62648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79d114ce702d8e88dd4fcaf1848e6af122c319f42efcdacc63d2adfc4e6ea6d3`

```dockerfile
```

-	Layers:
	-	`sha256:842249a97806b6a1d95018377c5bc6a7d69377bf126ba9ca367140ab3fd56640`  
		Last Modified: Sat, 21 Dec 2024 03:25:52 GMT  
		Size: 62.6 KB (62648 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:php8.2-apache` - linux; ppc64le

```console
$ docker pull joomla@sha256:bc64e705ccfef7892de9a8004b3073417dca85335c997b155aa4d11da451f889
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.1 MB (264109155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:608070951fa1a998d51bf4a3b7248b8ffbdd7f2c180528ee6c0db5c239188db6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 14 Dec 2024 11:07:50 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1734912000'
# Sat, 14 Dec 2024 11:07:50 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 14 Dec 2024 11:07:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 14 Dec 2024 11:07:50 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 14 Dec 2024 11:07:50 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 14 Dec 2024 11:07:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Dec 2024 11:07:50 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Dec 2024 11:07:50 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 14 Dec 2024 11:07:50 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Sat, 14 Dec 2024 11:07:50 GMT
ENV PHP_VERSION=8.2.27
# Sat, 14 Dec 2024 11:07:50 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.27.tar.xz.asc
# Sat, 14 Dec 2024 11:07:50 GMT
ENV PHP_SHA256=3eec91294d8c09b3df80b39ec36d574ed9b05de4c8afcb25fa215d48f9ecbc6b
# Sat, 14 Dec 2024 11:07:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 14 Dec 2024 11:07:50 GMT
STOPSIGNAL SIGWINCH
# Sat, 14 Dec 2024 11:07:50 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
WORKDIR /var/www/html
# Sat, 14 Dec 2024 11:07:50 GMT
EXPOSE map[80/tcp:{}]
# Sat, 14 Dec 2024 11:07:50 GMT
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
	-	`sha256:4a1ea4d3c9e0863e99d27aae6dac9a4b908a6413e758c7785d8fefe555b0e760`  
		Last Modified: Wed, 25 Dec 2024 00:32:48 GMT  
		Size: 32.1 MB (32063240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d132df684634db62d3c01ce1613d6eb2566301af85c63410ac30f024166112ae`  
		Last Modified: Wed, 25 Dec 2024 04:36:00 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd875cb56d0accafa903279e20e2f4504ccbb9a52d3356e35159318d6e6cac86`  
		Last Modified: Wed, 25 Dec 2024 04:36:04 GMT  
		Size: 103.1 MB (103128544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46c503622cfce9dd90835f8eb52e082345bb8d299e64a5d12507cacb0203fab6`  
		Last Modified: Wed, 25 Dec 2024 04:36:00 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ccc535b192e7a86a518e6f79725942e51c09ecbfe2b3a18e1ac7ba323d04859`  
		Last Modified: Wed, 25 Dec 2024 04:40:54 GMT  
		Size: 21.3 MB (21308315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d144b282eeec3a288e4659f298308f4f6703eec9b9e924a1bc18380740166116`  
		Last Modified: Wed, 25 Dec 2024 04:40:53 GMT  
		Size: 435.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2c966348685f6c718513b59fe339b4bee7adf696c1a64b706b268a42add51d3`  
		Last Modified: Wed, 25 Dec 2024 04:40:53 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91169a513b955fa4ee4703866c4585751dc3ce382416f43b4263651e5a4a0fd4`  
		Last Modified: Wed, 25 Dec 2024 05:13:14 GMT  
		Size: 12.3 MB (12279168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b3476115ba0db82303d93f560f03eb26c1b9049a6a417790fbada9d21d2ffa3`  
		Last Modified: Wed, 25 Dec 2024 05:13:13 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30c23b5a9aa99b7f32856e5b0a1c48217b71efce5b0aee737d62b70337955aee`  
		Last Modified: Wed, 25 Dec 2024 05:13:14 GMT  
		Size: 11.8 MB (11833341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ad7d38347f3f5fb067898d8f38f36a026839487f61016401a91e256ba8d3e1`  
		Last Modified: Wed, 25 Dec 2024 05:13:13 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5c354b0ae924f1a7d12a5c821b5a668df2d000d15001f19bdc328423c5437b6`  
		Last Modified: Wed, 25 Dec 2024 05:13:14 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c35f95d828ba34c2c2e941b133ac59ed5518129d15f48a0e943149e14988d85c`  
		Last Modified: Wed, 25 Dec 2024 05:13:14 GMT  
		Size: 887.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b87a9ec0b2f5cce3cd01dcf5ada028bb65aae908466df51067b50baaae588cb`  
		Last Modified: Wed, 25 Dec 2024 10:19:55 GMT  
		Size: 28.3 MB (28319291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87318a42101912ea3cfe2a2ba7fa51cb4928fdf79ba089977bf17e74e0d67907`  
		Last Modified: Wed, 25 Dec 2024 10:19:55 GMT  
		Size: 31.4 MB (31371244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deafc2b5498553230fa64563960dca939666193cda84fb37ff14e93fe2a8de8a`  
		Last Modified: Wed, 25 Dec 2024 10:19:54 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8064ee46e9b13f301573570782f279aa28a2aa2c8522ac5f751e298778de6ba`  
		Last Modified: Wed, 25 Dec 2024 10:19:54 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff893812afdfa58b58579782282dc30eb1af631e415a48f66fe34abe5a4c4302`  
		Last Modified: Wed, 25 Dec 2024 10:19:55 GMT  
		Size: 19.2 KB (19154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf9913b88cead4ca50ee493a45c8817aabc8ded84ca26a3f19ad74d332c1bbb`  
		Last Modified: Wed, 25 Dec 2024 10:19:57 GMT  
		Size: 23.8 MB (23775915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b414a484fbff4898738c66b71619ad6bc63c4427d61b99210f49ed9250022d9`  
		Last Modified: Wed, 25 Dec 2024 10:19:56 GMT  
		Size: 3.7 KB (3656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f9c90a08f9f4a5a033b862c08fa1d57febf7068922d08b1de32d2cf48b2dd4`  
		Last Modified: Wed, 25 Dec 2024 10:19:56 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:php8.2-apache` - unknown; unknown

```console
$ docker pull joomla@sha256:26fe4b44596fc9c6f376099054074ff4a671ae62cc8c7956b5ef9abdeebd1e12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.6 KB (62594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41f2fe3252a54c3d402e8801da79fa91392fb73fa263387e65dc316031d83835`

```dockerfile
```

-	Layers:
	-	`sha256:fc970c72e7d91ed7dc1aa1e6d73acc8009d0b004feec579903cfe8b627f48a17`  
		Last Modified: Wed, 25 Dec 2024 10:19:53 GMT  
		Size: 62.6 KB (62594 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:php8.2-apache` - linux; s390x

```console
$ docker pull joomla@sha256:9709f4527175fc9232576f026ab417b9cc5022541b4d013fdf5f85e2431de5cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.8 MB (228781381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b2104f2d36f8f4808b5ea5f7a18f9e2a9a747c83c7a76485823fc6176a68285`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 14 Dec 2024 11:07:50 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1734912000'
# Sat, 14 Dec 2024 11:07:50 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 14 Dec 2024 11:07:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 14 Dec 2024 11:07:50 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 14 Dec 2024 11:07:50 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 14 Dec 2024 11:07:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Dec 2024 11:07:50 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Dec 2024 11:07:50 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 14 Dec 2024 11:07:50 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Sat, 14 Dec 2024 11:07:50 GMT
ENV PHP_VERSION=8.2.27
# Sat, 14 Dec 2024 11:07:50 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.27.tar.xz.asc
# Sat, 14 Dec 2024 11:07:50 GMT
ENV PHP_SHA256=3eec91294d8c09b3df80b39ec36d574ed9b05de4c8afcb25fa215d48f9ecbc6b
# Sat, 14 Dec 2024 11:07:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 14 Dec 2024 11:07:50 GMT
STOPSIGNAL SIGWINCH
# Sat, 14 Dec 2024 11:07:50 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Sat, 14 Dec 2024 11:07:50 GMT
WORKDIR /var/www/html
# Sat, 14 Dec 2024 11:07:50 GMT
EXPOSE map[80/tcp:{}]
# Sat, 14 Dec 2024 11:07:50 GMT
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
	-	`sha256:0e7e84bd4cca9e29f08dfac96d436e65bdd31929520e73147137b382fbc89b70`  
		Last Modified: Tue, 24 Dec 2024 21:33:49 GMT  
		Size: 26.9 MB (26878901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f00cbfa93c448a5709b2ab89b4eecafcf312bab962f82f649a898256b58523f5`  
		Last Modified: Tue, 24 Dec 2024 22:49:53 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:457328e6b14be13d9f88b508b5952998504e5014f0290e6e1be39897bab54ba4`  
		Last Modified: Tue, 24 Dec 2024 22:49:55 GMT  
		Size: 80.6 MB (80624323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b9339c0eb88e9961929bd0005c1c4f86104f98d5884f539ed8d91ef9f169fd7`  
		Last Modified: Tue, 24 Dec 2024 22:49:53 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e47fb800ea78c724c59025d5ac46e9c60dea88853ca2b4ae21855f62533c1a76`  
		Last Modified: Tue, 24 Dec 2024 22:54:21 GMT  
		Size: 19.9 MB (19895315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31cd195bf1bc34d371e309aeabf0a6d8810a778544fb754738ceebbed7152b26`  
		Last Modified: Tue, 24 Dec 2024 22:54:20 GMT  
		Size: 434.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc4a7840b6ec52c065ff2d8ad71af54e6267fa1bbca2329da95e751d55ef9cc`  
		Last Modified: Tue, 24 Dec 2024 22:54:20 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00de7bf1eb84ec6ce0d8dc9b2b1d7ff6a52e27f8b4d81e672a508499b1adbe88`  
		Last Modified: Tue, 24 Dec 2024 23:24:33 GMT  
		Size: 12.3 MB (12278042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69bb52d4e350ae034217988d6815a8083632bbfcae84a05af30e44dc1b035570`  
		Last Modified: Tue, 24 Dec 2024 23:24:32 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2fd48c458d41447cb0e9f2c7acd51942534ef05446a768fbb5324fc6dc85b6b`  
		Last Modified: Tue, 24 Dec 2024 23:24:33 GMT  
		Size: 10.7 MB (10650059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3703e8a8c1af0d1959068ca0fd3cb9ca8e203b186de9d526d744da5681ec9c31`  
		Last Modified: Tue, 24 Dec 2024 23:24:32 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c708deb7caee13da39f9d5808b2f61ebc07146052df66417bc7ce49d4aa8bdc7`  
		Last Modified: Tue, 24 Dec 2024 23:24:33 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2d36b2afa23f0a1c8d652d27a73d3f4b875775149ab75377b5629784ea40909`  
		Last Modified: Tue, 24 Dec 2024 23:24:33 GMT  
		Size: 887.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0402fe9b842a2bb7534d8c1c6be588639dc87f273b297280bafd95027c4d6170`  
		Last Modified: Wed, 25 Dec 2024 03:56:34 GMT  
		Size: 26.7 MB (26698309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11205f9eb6ebbee006d93df8519a5db2b268e86e4b3a8706f99f1614cb8bba7`  
		Last Modified: Wed, 25 Dec 2024 03:56:34 GMT  
		Size: 28.0 MB (27950418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5b39c19c5686c1471a88be330c3dbe5fe5334aceffa05521753ef6a45ab6325`  
		Last Modified: Wed, 25 Dec 2024 03:56:33 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6384e713e115a2976a8dedfe14947ee2b1e45f9fa7957d4cb084b2662c4f5637`  
		Last Modified: Wed, 25 Dec 2024 03:56:33 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5dcb12ff4ed960421c1ad1075e22b463519e564de7c7818f00cc0753581807a`  
		Last Modified: Wed, 25 Dec 2024 03:56:34 GMT  
		Size: 19.2 KB (19152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be6b4c273333a2b50145d2432bcecfbf0734e8f5671824b5b2750c90cbe46529`  
		Last Modified: Wed, 25 Dec 2024 03:56:35 GMT  
		Size: 23.8 MB (23775916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4627841c7009ab87166cf54fd770b8702c3b00427b47f2265cb0fe8d2a6db7d7`  
		Last Modified: Wed, 25 Dec 2024 03:56:35 GMT  
		Size: 3.7 KB (3653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08e53f7af627f6ce472acb89c4680550d6b4923ae1d40399016a78397688a8bd`  
		Last Modified: Wed, 25 Dec 2024 03:56:35 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:php8.2-apache` - unknown; unknown

```console
$ docker pull joomla@sha256:fcd3ab8081b408585fde7f4b6f7eab4f1014a285f45d7c9002be162f6391e9a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.5 KB (62459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf9ae651d2d7b1ace2a3ad5f76ac1acd3385a76715aee4b542a411e944ae1a01`

```dockerfile
```

-	Layers:
	-	`sha256:e83638156adbae8cb21441321db5a331628970136b88abbce8a55e1011d142c8`  
		Last Modified: Wed, 25 Dec 2024 03:56:33 GMT  
		Size: 62.5 KB (62459 bytes)  
		MIME: application/vnd.in-toto+json
