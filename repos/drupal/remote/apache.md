## `drupal:apache`

```console
$ docker pull drupal@sha256:54d8951c1e2346a239b0ddc4897b0a67665f4738a5659414cd51c3f22db52c81
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `drupal:apache` - linux; amd64

```console
$ docker pull drupal@sha256:a39c16b7cc4157028600d2d5cc9c75cfc0e7c141c47f4d970282e142628bc55b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.0 MB (204010845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c303e9e1f363ba6f6cd709ce08aef6157c920c10a288130fbb303ae5f94a9441`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 25 Jun 2025 09:56:45 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 25 Jun 2025 09:56:45 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_VERSION=8.4.8
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 25 Jun 2025 09:56:45 GMT
STOPSIGNAL SIGWINCH
# Wed, 25 Jun 2025 09:56:45 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
WORKDIR /var/www/html
# Wed, 25 Jun 2025 09:56:45 GMT
EXPOSE map[80/tcp:{}]
# Wed, 25 Jun 2025 09:56:45 GMT
CMD ["apache2-foreground"]
# Thu, 26 Jun 2025 15:58:59 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
ENV DRUPAL_VERSION=11.2.2
# Thu, 26 Jun 2025 15:58:59 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 26 Jun 2025 15:58:59 GMT
WORKDIR /opt/drupal
# Thu, 26 Jun 2025 15:58:59 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:dad67da3f26bce15939543965e09c4059533b025f707aad72ed3d3f3a09c66f8`  
		Last Modified: Tue, 10 Jun 2025 23:26:09 GMT  
		Size: 28.2 MB (28230129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f258d4e47039b347f87c60c487e5296f67327178b0c5d7c257316064e161b05`  
		Last Modified: Wed, 25 Jun 2025 19:56:26 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5c3dd218afa7930e1778b833199c840ceb0a7163ce8751f1181e85a4fbc7e09`  
		Last Modified: Wed, 25 Jun 2025 19:56:32 GMT  
		Size: 104.3 MB (104331412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29539b7ce2243bf98a73ff6599af69218b0ce883b70330e15d3fd40ea2df43b6`  
		Last Modified: Wed, 25 Jun 2025 19:56:25 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a6e95ec7c55331a4de75177744f45d69d14944f941cf99c97e02250c69c2a2c`  
		Last Modified: Wed, 25 Jun 2025 19:56:26 GMT  
		Size: 20.1 MB (20123788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2972820874ef016a7a93614bfcc4495313640167590fb275b5c2773cd4921910`  
		Last Modified: Wed, 25 Jun 2025 19:56:24 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddca6364a3024618999c1dd315fc28562652664934cea41074f9aa0820d9479b`  
		Last Modified: Wed, 25 Jun 2025 19:56:24 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa43a9342a6e32c088fbdbbf7a00c2f407d90dc37498b911973c44f29e468a7c`  
		Last Modified: Wed, 25 Jun 2025 19:56:25 GMT  
		Size: 13.7 MB (13748152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef5144a7fb9a878d65dc61d4cb8681517e8f8ff8e7a79534f009c797b60cc0f`  
		Last Modified: Wed, 25 Jun 2025 19:56:23 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ded8d8a79a706b8869070aa85960a7613d145d14700d8b76fa3c80eef69dcd98`  
		Last Modified: Wed, 25 Jun 2025 19:56:25 GMT  
		Size: 14.2 MB (14169669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb74384d82b1ab0fafcf604a68d3e70571660c4dc1c50ae0f0c12aa2770a4813`  
		Last Modified: Wed, 25 Jun 2025 19:56:23 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98a7d1c280ab7e4dd1bcbeea76266a680b6f7ae22cc3d4e092eb5112ce01c8e9`  
		Last Modified: Wed, 25 Jun 2025 19:56:23 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:146db4084e6aca69b57492a0f4ddd7b3c357ce4a243173fd3210e41d50a2f61b`  
		Last Modified: Wed, 25 Jun 2025 19:56:23 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9c173ab3b69d43052841730862b3d1c3dc334405b0c576478afa1cb2665026f`  
		Last Modified: Wed, 25 Jun 2025 19:56:23 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b757fa046357c7017a45657f09b235b118114fc80571b92f090cd1b309946f5`  
		Last Modified: Thu, 26 Jun 2025 20:03:05 GMT  
		Size: 2.1 MB (2129525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e868b53bb5595db5ebf5270e587297ff72e38fad08d070da70dfbf055db3081`  
		Last Modified: Thu, 26 Jun 2025 20:03:04 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29425bdc0c8ccc62787afbe710537eaf73b8e6b5ca625be6b4647e0b9acbab16`  
		Last Modified: Thu, 26 Jun 2025 20:03:04 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44854699788388a8818e0ad1af242d75b9ddd953ecb638914381481da874ba7f`  
		Last Modified: Thu, 26 Jun 2025 20:03:05 GMT  
		Size: 752.8 KB (752770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db3ab1355ca8476981107f8a0c80b3550e7c38b8ca1ff6abdbb16780eb5c2533`  
		Last Modified: Thu, 26 Jun 2025 20:03:04 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d675faef45a2be46fd38910c76bddcf5f07826ed688d22c2d86c36de1a7cfa39`  
		Last Modified: Thu, 26 Jun 2025 20:03:08 GMT  
		Size: 20.5 MB (20518976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:apache` - unknown; unknown

```console
$ docker pull drupal@sha256:9308656cb82686a93f341f95aedd6fedc6f87a8124544885035b5288fc116682
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7106043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52d15425cf83d8c04a91adaa7e20fd196ed76931b6f541b6aeac91aa963ca2f1`

```dockerfile
```

-	Layers:
	-	`sha256:0026555fe1e3be50b6f725fdeac086cef3cbc0171dd61ac8bc01e76a9e9c8140`  
		Last Modified: Thu, 26 Jun 2025 23:01:57 GMT  
		Size: 7.1 MB (7056957 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e875fc42eb4a19c902faa0e23c2403a64d1f73be7680d039ba1fbfe21a5da6a`  
		Last Modified: Thu, 26 Jun 2025 23:01:57 GMT  
		Size: 49.1 KB (49086 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:apache` - linux; arm variant v7

```console
$ docker pull drupal@sha256:dc7e1f4b9f2966c4d9036098ac90908e8cbcf6089753a90623eb93570c586855
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.6 MB (167602423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8ee5ed6a761e4cf2402f138676cd27d619f0947deb5bc0207f2d2d1dd568a4e`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1749513600'
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 25 Jun 2025 09:56:45 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 25 Jun 2025 09:56:45 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_VERSION=8.4.8
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 25 Jun 2025 09:56:45 GMT
STOPSIGNAL SIGWINCH
# Wed, 25 Jun 2025 09:56:45 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
WORKDIR /var/www/html
# Wed, 25 Jun 2025 09:56:45 GMT
EXPOSE map[80/tcp:{}]
# Wed, 25 Jun 2025 09:56:45 GMT
CMD ["apache2-foreground"]
# Thu, 26 Jun 2025 15:58:59 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
ENV DRUPAL_VERSION=11.2.2
# Thu, 26 Jun 2025 15:58:59 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 26 Jun 2025 15:58:59 GMT
WORKDIR /opt/drupal
# Thu, 26 Jun 2025 15:58:59 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:6aafc35ac588733109bc0c55587676a69c7a13b7c2d7306cdb389c2db1299c9c`  
		Last Modified: Tue, 10 Jun 2025 23:58:28 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc7e129ebc47cfb419b9baed6e494c99e8122d50bbdef5c47a23d99fa67bcbb1`  
		Last Modified: Tue, 10 Jun 2025 23:59:42 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3510790a012b31ddda9feb019968af4c3b5afc39bc69e8a86243793dc1278d31`  
		Last Modified: Wed, 11 Jun 2025 02:02:19 GMT  
		Size: 76.1 MB (76133481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7a4467e239356b42185ae523baf135c70abd0641b0d4c23494d1d8a7eaf87c9`  
		Last Modified: Tue, 10 Jun 2025 23:59:42 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4bd99c841c62a8c7597b28f01dab475d45c077230e138fba187ce731e24347a`  
		Last Modified: Wed, 11 Jun 2025 01:13:44 GMT  
		Size: 18.9 MB (18857586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a064890dcb56400fd4cb8c803a0204a8912de9d92e459d1f0d4787314714d8c3`  
		Last Modified: Wed, 11 Jun 2025 00:45:17 GMT  
		Size: 433.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3ddabc9f5981514dd562757ac88989dbb8f03f93ce96a172f900134a3e77163`  
		Last Modified: Wed, 11 Jun 2025 00:45:21 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40aacbe108c0209a2952b8a793e398aa5a5f05b8a5273d831dce63bafb138bcc`  
		Last Modified: Wed, 11 Jun 2025 18:44:46 GMT  
		Size: 13.7 MB (13746012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57e2932af4f235f30915882fc9dd14ddf2350e20c309a6ebfd015df21719a20b`  
		Last Modified: Wed, 11 Jun 2025 16:26:26 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bbf44bd766edaef1decbb549e95c236b6fcb1c3cecb6c5747e33d83afad48e9`  
		Last Modified: Wed, 11 Jun 2025 18:44:48 GMT  
		Size: 12.3 MB (12282085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:722279a2880fb1833af87e9468c0490f650f1d8abc6376429e99841e2202f126`  
		Last Modified: Wed, 25 Jun 2025 19:19:35 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36a3fceee06e54696aca4bcae0343f2227792188beaf1089b2d98c8b79435f6d`  
		Last Modified: Wed, 25 Jun 2025 19:19:36 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aec12b48d192fd2e8bc4cabbdfa0dd7790107648acdaab22f6cfc609215be432`  
		Last Modified: Wed, 25 Jun 2025 19:19:35 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:127a32f04dcee032a9cd513556a501ae082a4d50b81583b6b85286fdc35918ab`  
		Last Modified: Wed, 25 Jun 2025 19:19:36 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daed1478d409341da9f1c7be47c10d90cc67199cd47d98eb01f3be06c407ce35`  
		Last Modified: Wed, 25 Jun 2025 23:56:42 GMT  
		Size: 1.4 MB (1366024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e1f7b5de2c5c478a2ab5f38a01cbf09ae1e1154f4f43cb396957faaf5ed9236`  
		Last Modified: Wed, 25 Jun 2025 23:56:42 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4280eb4f82b1125ccb2526428bb3e798de35f7ca2ca7a76b3aebd862d0831454`  
		Last Modified: Wed, 25 Jun 2025 23:56:41 GMT  
		Size: 260.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:185b53ca02a2ca744e501490b58bb1a9e4d76206e9b35cf3c998aed2183dab86`  
		Last Modified: Wed, 25 Jun 2025 23:56:42 GMT  
		Size: 752.8 KB (752771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:166077063fa1e867bd62d5851c9c079df795cd3c8733a79b7370ba88b98002d7`  
		Last Modified: Wed, 25 Jun 2025 23:56:41 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d750d34ff08601b5a2b550d10e191397dc20eebace424c827a9090dfaa8efe18`  
		Last Modified: Thu, 26 Jun 2025 20:01:51 GMT  
		Size: 20.5 MB (20519276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:apache` - unknown; unknown

```console
$ docker pull drupal@sha256:6047fe6d01713c75d81f133e51600bd034192aefd89328bff6870f2cd17fc402
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6918473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b01335fa65590c38d8f3c659e0991e21242c031320ead5790c1c0c538fc34dd`

```dockerfile
```

-	Layers:
	-	`sha256:ff92ace96f5d9d065a0427f1ae127a1c7814740957d53e0a6a011527244ecc68`  
		Last Modified: Thu, 26 Jun 2025 23:02:03 GMT  
		Size: 6.9 MB (6869097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d006f917d42e303324966c1c9b539defaa57a85ded4475ebbe9aa02dda507d9a`  
		Last Modified: Thu, 26 Jun 2025 23:02:04 GMT  
		Size: 49.4 KB (49376 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:apache` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:c756990f2ec106fe4e21aee6cc88d1a7cf98666ce724b5beb9a6580a8dd4f29b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.2 MB (197195649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0e16585a4a1d091c1f108ec7977215286c9d8dc80427db47d14e0875d6e7b77`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 25 Jun 2025 09:56:45 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 25 Jun 2025 09:56:45 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_VERSION=8.4.8
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 25 Jun 2025 09:56:45 GMT
STOPSIGNAL SIGWINCH
# Wed, 25 Jun 2025 09:56:45 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
WORKDIR /var/www/html
# Wed, 25 Jun 2025 09:56:45 GMT
EXPOSE map[80/tcp:{}]
# Wed, 25 Jun 2025 09:56:45 GMT
CMD ["apache2-foreground"]
# Thu, 26 Jun 2025 15:58:59 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
ENV DRUPAL_VERSION=11.2.2
# Thu, 26 Jun 2025 15:58:59 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 26 Jun 2025 15:58:59 GMT
WORKDIR /opt/drupal
# Thu, 26 Jun 2025 15:58:59 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:34ef2a75627f6089e01995bfd3b3786509bbdc7cfb4dbc804b642e195340dbc9`  
		Last Modified: Tue, 10 Jun 2025 22:48:42 GMT  
		Size: 28.1 MB (28077675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3630c4a6bfab28c7ce5de97d716ebcd720dbf83dcf0eb1c761482ff53aefecc2`  
		Last Modified: Wed, 11 Jun 2025 00:30:58 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:877a4d3e37c32b0606f0cdd36bf1d42e5e59ac5729fa9e5e94c40a68ebbbd7ff`  
		Last Modified: Wed, 11 Jun 2025 00:31:07 GMT  
		Size: 98.1 MB (98128104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39acdc3547850b2843d66bec50193728979d970d5b3dbee391835e42e8af76bd`  
		Last Modified: Wed, 11 Jun 2025 00:30:58 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fff45d01fc3a1c40ea5502d151378828ff3da3ce4c3160630a1bfb6fbfcaa59`  
		Last Modified: Wed, 11 Jun 2025 00:58:28 GMT  
		Size: 20.1 MB (20121056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a25063be4912895a54cba397a2b5a11fb66365d7db306ed5cc230f4ec4ecc3f3`  
		Last Modified: Wed, 11 Jun 2025 00:58:27 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8dd604a657c684c548321c337058fdb4c7d07328a25884f339c5ace8d05f3f1`  
		Last Modified: Wed, 11 Jun 2025 00:58:27 GMT  
		Size: 481.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fcec1acaef1a0748e916821687b763a7269b7aa7d27bec8e346e4cd854cccc6`  
		Last Modified: Wed, 11 Jun 2025 01:15:51 GMT  
		Size: 13.7 MB (13747867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d508ded73c311d9696ebd90d38c894eee1201422a3253793009d1f9de9fbfe5`  
		Last Modified: Wed, 11 Jun 2025 01:15:48 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51f5f481e5f40588fd62242c3b4d3dfa13b2bc7564f47fce35d33aceca140393`  
		Last Modified: Wed, 11 Jun 2025 02:00:19 GMT  
		Size: 13.8 MB (13810329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d91b9d01ffce6a57e8124c1bbcd080c47b52d17eb5fe39e52197c26cda67625`  
		Last Modified: Wed, 25 Jun 2025 19:45:11 GMT  
		Size: 2.5 KB (2464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c485457537cc9badf13a49d13392833ba828d86e12d6f2541eae82c9144270`  
		Last Modified: Wed, 25 Jun 2025 19:45:13 GMT  
		Size: 254.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ccf388dd4552c5d7558003e253fd6631e7d8714e33158dadeb63bddfee50c94`  
		Last Modified: Wed, 25 Jun 2025 19:45:17 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ae5dbb196cdb04b5dd953d447c2f6d3eb05d62e9dd9b4023327babac4646659`  
		Last Modified: Wed, 25 Jun 2025 19:45:21 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a50c7dee009a6b37cce0c5e6976acf8640741a89bd5e0b5b93c0410035912e2`  
		Last Modified: Thu, 26 Jun 2025 03:52:40 GMT  
		Size: 2.0 MB (2032331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d417c38f43a687e2291e600632b13748f33d7e8400c271cedd80f5cc427ed8`  
		Last Modified: Thu, 26 Jun 2025 03:52:38 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d294c515b2f14af58701c31e108d7fdca578e48b35ca23629bb556ac70c09023`  
		Last Modified: Thu, 26 Jun 2025 03:52:39 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72b4ae7d1699001e49f6b8bfb212f6d702a179d47c2bf7eabe856327b78e333a`  
		Last Modified: Thu, 26 Jun 2025 03:52:39 GMT  
		Size: 752.8 KB (752771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfaa0288fdd62e0a6121b27f6692bb61cb0ee71b01b1e380f66010c38dcedc34`  
		Last Modified: Thu, 26 Jun 2025 03:52:38 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e5d7854ef6219b85126bde82768ab95d946d73caaab78e95e297a0a6c82c24f`  
		Last Modified: Thu, 26 Jun 2025 20:01:40 GMT  
		Size: 20.5 MB (20519086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:apache` - unknown; unknown

```console
$ docker pull drupal@sha256:44d06acf2f0312796063366f970ed5d9a0d442441f2b9574173a7a6149932c6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7133748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22968439cb8e98870a212544777826720b75adac2f456c3ca1ebcc90030a63a5`

```dockerfile
```

-	Layers:
	-	`sha256:c33a8df3c37a2f0165752a50ecfbc07c77973b4492fbf33cabfeda41d2076b2d`  
		Last Modified: Thu, 26 Jun 2025 23:02:10 GMT  
		Size: 7.1 MB (7084254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc5c464c30f5c5df4f1a1f4a6e2a817de3f78d1b9f3596c829d828e2a9936f61`  
		Last Modified: Thu, 26 Jun 2025 23:02:10 GMT  
		Size: 49.5 KB (49494 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:apache` - linux; 386

```console
$ docker pull drupal@sha256:2fa2f9ceee07dd1f21683716c9b222393cd0a635afa0c085d521b4bc54730a7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.1 MB (203077162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd7dfb7ed8a39e29f6f8dfe8f3cd5ed5be46dbf45b85e88b624b782ccaffb2fa`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1749513600'
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 25 Jun 2025 09:56:45 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 25 Jun 2025 09:56:45 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_VERSION=8.4.8
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 25 Jun 2025 09:56:45 GMT
STOPSIGNAL SIGWINCH
# Wed, 25 Jun 2025 09:56:45 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
WORKDIR /var/www/html
# Wed, 25 Jun 2025 09:56:45 GMT
EXPOSE map[80/tcp:{}]
# Wed, 25 Jun 2025 09:56:45 GMT
CMD ["apache2-foreground"]
# Thu, 26 Jun 2025 15:58:59 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
ENV DRUPAL_VERSION=11.2.2
# Thu, 26 Jun 2025 15:58:59 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 26 Jun 2025 15:58:59 GMT
WORKDIR /opt/drupal
# Thu, 26 Jun 2025 15:58:59 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:c3d46fed134488b3ee18c12cb308c8d5520b8c647122c392f9fb76e3e1e2fc61`  
		Last Modified: Tue, 10 Jun 2025 22:47:25 GMT  
		Size: 29.2 MB (29212433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dd7c6a433133a4e36c8dbbf68ad3561561ff03a3a87fe24256a388119402540`  
		Last Modified: Wed, 25 Jun 2025 19:56:39 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55024fbc5d234ce1dc9c5b3484033146070b0800e1e393ea9149a59c335e5e20`  
		Last Modified: Wed, 25 Jun 2025 19:56:45 GMT  
		Size: 101.5 MB (101515058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed3f7190deb8bed922e6070ab05858c9d81c3c4905663d9fa01257fe5b13315`  
		Last Modified: Wed, 25 Jun 2025 19:56:38 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5556d68a66d91d7181fa338855a1bdf1027ce94ab160f6cd9a4cfdb1c921f9fb`  
		Last Modified: Wed, 25 Jun 2025 19:56:39 GMT  
		Size: 20.6 MB (20638465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ac21b0fc639d60c3d103f55e2007c45fbc65cb4ba724e1d69ec243751b7e78`  
		Last Modified: Wed, 25 Jun 2025 19:56:38 GMT  
		Size: 427.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e389cc928cf28552e023517dc101a1555ea280d4e4936e032c9e633cffbec1b2`  
		Last Modified: Wed, 25 Jun 2025 19:56:37 GMT  
		Size: 481.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00dab7ed21840830e8f6895f07f50b22ee6f8a1223739820edc74fcf2cb74253`  
		Last Modified: Wed, 25 Jun 2025 19:56:38 GMT  
		Size: 13.7 MB (13747044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14102322715308abcd744fa421f6b1312556d77a4c59a0243d2d5efda3e71c78`  
		Last Modified: Wed, 25 Jun 2025 19:56:37 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8736aa061c0b22ae0608d51bd461598d6dafa089907579d692929181afa28dd4`  
		Last Modified: Wed, 25 Jun 2025 19:56:38 GMT  
		Size: 14.5 MB (14463083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10aced2d7e492172ef1e65fba913ec11f0cd7539f493167b9075a00ea79b7013`  
		Last Modified: Wed, 25 Jun 2025 19:56:37 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25ac35b7fb342b380dbf62354a0ba8358addebdb82ba9c0e5ea4e31797b5f118`  
		Last Modified: Wed, 25 Jun 2025 19:56:37 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58a1f11fe1ee365f52851132fd34630295373342c5a753058fcb5a6786982b2e`  
		Last Modified: Wed, 25 Jun 2025 19:56:37 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f1bdaa48614b9ef29cffd7607c1819824e4b3a14637033531fb47c4c8abfc1c`  
		Last Modified: Wed, 25 Jun 2025 19:56:37 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890aa9aba5f6192bb37a518086379e9cdf607f78a0a90cc113a76ceda9969f87`  
		Last Modified: Fri, 27 Jun 2025 00:01:41 GMT  
		Size: 2.2 MB (2222666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46153159dc588f67b6391d525066ad991918a13fb71a72722d823bcf9d02e7f8`  
		Last Modified: Fri, 27 Jun 2025 00:01:42 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e94d29ece6c41e6e6fc7ffdcf887223e1f67fda17260ad21d7fe354426eea8`  
		Last Modified: Fri, 27 Jun 2025 00:01:42 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e3e848a5c0a0113b22405e98ff079c2717dde7cc02015519167910ce3d95a03`  
		Last Modified: Fri, 27 Jun 2025 00:01:42 GMT  
		Size: 752.8 KB (752770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc1c5acf3d8d2dfee5eba7a8051d1900360089432bb1d962dc2ce733163a2bcd`  
		Last Modified: Fri, 27 Jun 2025 00:01:42 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:925aee216bf8ca115ff68ac9438d8d4d65f0315b50cfa6b9faee43de8ecb9b65`  
		Last Modified: Fri, 27 Jun 2025 00:01:45 GMT  
		Size: 20.5 MB (20519233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:apache` - unknown; unknown

```console
$ docker pull drupal@sha256:d79181505013c7fcd99b25846ee95b90b037f65f7c40c19aae346705ea7a72c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7085546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d44d669646a70d15e5761b5bb3b86044628ff1bfe5811c034e1ba25195eb8877`

```dockerfile
```

-	Layers:
	-	`sha256:47bdd30af831baad5236ad7bce1f1f83b04df327d52b92ddf3a3ef6327eab871`  
		Last Modified: Thu, 26 Jun 2025 23:02:15 GMT  
		Size: 7.0 MB (7036605 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e741b8b86e9e25f0415a316c76a02ab4413452147ef04d959f4f0425a4ead852`  
		Last Modified: Thu, 26 Jun 2025 23:02:16 GMT  
		Size: 48.9 KB (48941 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:apache` - linux; ppc64le

```console
$ docker pull drupal@sha256:d31fdd337cd29f30df4cfa6e96aaf19376a2c23536f84ea2c822005514e65f21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.2 MB (208185488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c18a80120f05ecfc19506b9b4ebbda6cc220c8164b7e2d1c12f3ab1d23d82a90`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1749513600'
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 25 Jun 2025 09:56:45 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 25 Jun 2025 09:56:45 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_VERSION=8.4.8
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 25 Jun 2025 09:56:45 GMT
STOPSIGNAL SIGWINCH
# Wed, 25 Jun 2025 09:56:45 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
WORKDIR /var/www/html
# Wed, 25 Jun 2025 09:56:45 GMT
EXPOSE map[80/tcp:{}]
# Wed, 25 Jun 2025 09:56:45 GMT
CMD ["apache2-foreground"]
# Thu, 26 Jun 2025 15:58:59 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
ENV DRUPAL_VERSION=11.2.2
# Thu, 26 Jun 2025 15:58:59 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 26 Jun 2025 15:58:59 GMT
WORKDIR /opt/drupal
# Thu, 26 Jun 2025 15:58:59 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:c9cd5d5c131a8141631d87d9507a82e0549a2144689442301c07d2da80f39d19`  
		Last Modified: Tue, 10 Jun 2025 23:58:45 GMT  
		Size: 32.1 MB (32072795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24080cf7a9f9030de6956835b567127c780a50d76fe3938c5cd866a6dac26023`  
		Last Modified: Wed, 11 Jun 2025 03:03:42 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76526385fd8e386cf6c038055e99723ffbb0aa517b93631441caedc0a0753304`  
		Last Modified: Wed, 11 Jun 2025 03:03:51 GMT  
		Size: 103.3 MB (103318539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd7e8958d2ce3cdc36201bfc36d3a2d97f4d7a91ae69e3506b18972eee9594fd`  
		Last Modified: Wed, 11 Jun 2025 03:03:41 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b82c8878a37c47261582f8bb724e9d4af07a08fc4eec03c30cb700604ac5b6f`  
		Last Modified: Wed, 11 Jun 2025 03:08:23 GMT  
		Size: 21.3 MB (21308411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9afea7841a4fa56bc13ea79c125347dedb821bb9565c68975100e36ff84afa21`  
		Last Modified: Wed, 11 Jun 2025 03:08:22 GMT  
		Size: 434.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2371a8ec6e746f39978ac01124bfc3ea9db3d106f65c9fe218ca960ce886e85f`  
		Last Modified: Wed, 11 Jun 2025 03:08:22 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1749d5218a9c12347823647735fe123579e90cd6ab27105a15bf2e8dfda3540a`  
		Last Modified: Wed, 11 Jun 2025 03:08:24 GMT  
		Size: 13.7 MB (13747521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a36bf95e240386df8ed4b078197efb07fc8d882718e2bc46a094c4efd967c691`  
		Last Modified: Wed, 11 Jun 2025 03:08:23 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f4b0f93f946b6e216c1fc6279c48b309f3b26a76eef9f98937a2cf1844667f`  
		Last Modified: Wed, 11 Jun 2025 03:08:24 GMT  
		Size: 14.6 MB (14587933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5acd23c370c0442eabfae1a7fcc2afeec1145a582ad40c7f10993310e5981139`  
		Last Modified: Wed, 25 Jun 2025 19:19:53 GMT  
		Size: 2.5 KB (2464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:181513d84e370b6d13a206bbcb81e75fd5e5918f5348492673f1d16e723dd348`  
		Last Modified: Wed, 25 Jun 2025 19:19:54 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6875aaff6d5a1583bd22c08c465cfc391a9c564525d3bc962d9c660a6afc5d1`  
		Last Modified: Wed, 25 Jun 2025 19:19:54 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f9dbe8e6054db3622a15d770efcf7c0671930db38c9575f433099ec19453b57`  
		Last Modified: Wed, 25 Jun 2025 19:19:54 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f61a760048352bbeeda3983d74c78eea2fe7a9198907bb0980d52d315cf9726`  
		Last Modified: Thu, 26 Jun 2025 02:25:09 GMT  
		Size: 1.9 MB (1871692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc86af6c402e6637f2dd279a6d09b250370baff26d02ff65ae08ce547e6de969`  
		Last Modified: Thu, 26 Jun 2025 02:25:09 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5c5e178e722af894cd1626c9dd2a0e8c91906685ebdb8b7342c19cfd2a8d772`  
		Last Modified: Thu, 26 Jun 2025 02:25:09 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aab07a47146c1e7e5ba38bc91139f5208cc255b08bc2fbb330f95d7f0c5775f`  
		Last Modified: Thu, 26 Jun 2025 02:25:10 GMT  
		Size: 752.8 KB (752771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6737bae2125361d1f67e61e73fc232171d0e34bb4c4bbf0f9bb9f10edfe8c555`  
		Last Modified: Thu, 26 Jun 2025 02:25:10 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8930fb9d802ddb615819075739bdd84c974e7d85db9fb380b082ca59b0d8600e`  
		Last Modified: Thu, 26 Jun 2025 20:03:13 GMT  
		Size: 20.5 MB (20519391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:apache` - unknown; unknown

```console
$ docker pull drupal@sha256:22f227f6964337d54f70d72788c49c63405c0bc7e5b1c80286c009112d2791d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7081822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dc9b0571b743411879e3a7cd45d8256e1658c742765d7b59525dd806599f1e4`

```dockerfile
```

-	Layers:
	-	`sha256:2cf07c0a35b322837352a51d9efad45311ae9e95af92b16130c901b1f3b43646`  
		Last Modified: Thu, 26 Jun 2025 23:02:21 GMT  
		Size: 7.0 MB (7032557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:548eb184922a4dd5a799af070930870a11a38a2298fa26f8636b3462ffb0d09a`  
		Last Modified: Thu, 26 Jun 2025 23:02:22 GMT  
		Size: 49.3 KB (49265 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:apache` - linux; s390x

```console
$ docker pull drupal@sha256:90064f3ee808ca14399cb0e6718e8d0cc8016099115588818c8899a623cc8b02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.5 MB (178477004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2114a693c9875ba04f5079078395d9d282446e39b4df7bd5ed9dc2cf3c3cf32`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1749513600'
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 25 Jun 2025 09:56:45 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 25 Jun 2025 09:56:45 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_VERSION=8.4.8
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 25 Jun 2025 09:56:45 GMT
STOPSIGNAL SIGWINCH
# Wed, 25 Jun 2025 09:56:45 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
WORKDIR /var/www/html
# Wed, 25 Jun 2025 09:56:45 GMT
EXPOSE map[80/tcp:{}]
# Wed, 25 Jun 2025 09:56:45 GMT
CMD ["apache2-foreground"]
# Thu, 26 Jun 2025 15:58:59 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
ENV DRUPAL_VERSION=11.2.2
# Thu, 26 Jun 2025 15:58:59 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 26 Jun 2025 15:58:59 GMT
WORKDIR /opt/drupal
# Thu, 26 Jun 2025 15:58:59 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:0f8692aee2900a8d946bd57522757b4d5de83b6af52eb0aa55e05d787a077615`  
		Last Modified: Tue, 10 Jun 2025 23:56:06 GMT  
		Size: 26.9 MB (26887853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6372fcd6d72a64e9952c1f98b81b9f9773c1b3874422ec0ef84cc9a9401ff8f1`  
		Last Modified: Wed, 11 Jun 2025 00:13:38 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4d8ff699d43e5155841feb2101e20cad4c539a873b5f8bc25f50ef7c7ee7597`  
		Last Modified: Wed, 11 Jun 2025 00:13:46 GMT  
		Size: 80.8 MB (80825266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba42c53eb537dcf508d7ad83efac6d9dbe2d8b1f572a7e7de2c5f49afc8a0add`  
		Last Modified: Wed, 11 Jun 2025 00:13:39 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a6658771fe8cc9003213d5fcc4ea7e52a3fda7e566df78ca7c79403e765141a`  
		Last Modified: Fri, 20 Jun 2025 19:47:21 GMT  
		Size: 19.9 MB (19895346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb164d0bf0d894ceff23b95daf2c801bcbcb343b40029aadb13af60df15eec96`  
		Last Modified: Fri, 20 Jun 2025 19:21:25 GMT  
		Size: 438.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e300d27550c010f15b474f01f2d2cb66f658165c6a7383204093e1706cf8403c`  
		Last Modified: Fri, 20 Jun 2025 19:21:29 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c9f28072db7784f68034c76c9d52efb56028e897c00ce5938f202cd1de1aa3c`  
		Last Modified: Wed, 25 Jun 2025 23:42:24 GMT  
		Size: 13.7 MB (13746442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df64f191962fd8821deb8b9fe6bdb82433b4a3df0f814405393043718a4cf13b`  
		Last Modified: Wed, 25 Jun 2025 23:42:23 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36767cd7212639d07feb23aaf431aba3c516fc476bf50f207ac80a40f017ff15`  
		Last Modified: Wed, 25 Jun 2025 23:42:25 GMT  
		Size: 14.3 MB (14278281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ca9f3834542a6b2177fde88b90dbdd92287f6cfa504570e5c7fb5ad995067a`  
		Last Modified: Wed, 25 Jun 2025 23:42:23 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88a94b770e4ed4d4fc06570ecad79a9cf3e1229349c12f3243178ba1d1df7f5c`  
		Last Modified: Wed, 25 Jun 2025 23:42:23 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fe98734828c17e15cf9c6a1e09c5c13b2694bcc0dc04daa6543a22a5cb05fc3`  
		Last Modified: Wed, 25 Jun 2025 23:42:23 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0401d924ef80f9fc176daf6ee8c16041290c9795a5253edf06c7e4ea7e62e6cd`  
		Last Modified: Wed, 25 Jun 2025 23:42:22 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81d22f7dc12bc272b43bd3c4102ef923019ce39923a88e820b99ab2a54de0156`  
		Last Modified: Thu, 26 Jun 2025 05:26:07 GMT  
		Size: 1.6 MB (1565314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57bbe1ce0b2b466e1b07a6aa4fe34f58a70c662f811d5c72f3214f332e6338a2`  
		Last Modified: Thu, 26 Jun 2025 05:26:07 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c027f4845567ce5be6fcd08cfa8f290127fd64d2be48fc4caf56853e162a78eb`  
		Last Modified: Thu, 26 Jun 2025 05:26:09 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0e99ef50ffdb58a280c9cc08eec0e4df436d683c7874388017ccc8821fb5efe`  
		Last Modified: Thu, 26 Jun 2025 05:26:10 GMT  
		Size: 752.8 KB (752770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45093fd694a58374e0111155e4139fb62d933bc0bfa5f895b8fbbc249395135e`  
		Last Modified: Thu, 26 Jun 2025 05:26:11 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1db99fcf55932149751deab36a760aa67175a5466b93d6458b7f43dc79799504`  
		Last Modified: Thu, 26 Jun 2025 20:03:41 GMT  
		Size: 20.5 MB (20519304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:apache` - unknown; unknown

```console
$ docker pull drupal@sha256:c1babf560db80f84ace86e3476f5c93c010ba8958ba6de81e76269a76b26f011
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6941882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:204ab680a5c19a3535c63799acfd47b11910912752dcd246541a46dcb3277868`

```dockerfile
```

-	Layers:
	-	`sha256:e4b1df8d946ea930d6dc411e638ed70bfe95eacbb51fb4dbd5e5d777a94d23a4`  
		Last Modified: Thu, 26 Jun 2025 23:02:27 GMT  
		Size: 6.9 MB (6892803 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f0fabe83e355d74068c9b6c71f83b89b9d792e7529eafbd9a3952c0ca08493b`  
		Last Modified: Thu, 26 Jun 2025 23:02:28 GMT  
		Size: 49.1 KB (49079 bytes)  
		MIME: application/vnd.in-toto+json
