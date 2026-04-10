## `yourls:latest`

```console
$ docker pull yourls@sha256:55faf4da37fe018cb5c215359429a9da8211d9315de059f8d9ce69e7152ed0ba
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
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `yourls:latest` - linux; amd64

```console
$ docker pull yourls@sha256:abb86a49acbedf96f315623947d1b16142a87c31afad10a45b49037ba474f215
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.5 MB (190502558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3029033a13a2736c19e0dc1f2543deae2489cb3d53781b2aaf2c4d4d1027ce6`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Thu, 09 Apr 2026 22:11:47 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 09 Apr 2026 22:12:04 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 09 Apr 2026 22:12:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 09 Apr 2026 22:12:04 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 09 Apr 2026 22:12:04 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 09 Apr 2026 22:12:04 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 09 Apr 2026 22:12:04 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 09 Apr 2026 22:12:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 09 Apr 2026 22:12:10 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 09 Apr 2026 22:12:10 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 09 Apr 2026 22:12:10 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 09 Apr 2026 22:12:10 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 09 Apr 2026 22:12:10 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 09 Apr 2026 22:12:10 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Thu, 09 Apr 2026 22:12:10 GMT
ENV PHP_VERSION=8.5.5
# Thu, 09 Apr 2026 22:12:10 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.5.tar.xz.asc
# Thu, 09 Apr 2026 22:12:10 GMT
ENV PHP_SHA256=95bec382f4bd00570a8ef52a58ec04d8d9b9a90494781f1c106d1b274a3902f2
# Thu, 09 Apr 2026 22:12:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 09 Apr 2026 22:12:19 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 22:15:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 09 Apr 2026 22:15:16 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 22:15:16 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 09 Apr 2026 22:15:16 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 09 Apr 2026 22:15:16 GMT
STOPSIGNAL SIGWINCH
# Thu, 09 Apr 2026 22:15:16 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 22:15:16 GMT
WORKDIR /var/www/html
# Thu, 09 Apr 2026 22:15:16 GMT
EXPOSE map[80/tcp:{}]
# Thu, 09 Apr 2026 22:15:16 GMT
CMD ["apache2-foreground"]
# Thu, 09 Apr 2026 23:13:42 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)"     bcmath     pdo_mysql     mysqli # buildkit
# Thu, 09 Apr 2026 23:13:42 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Thu, 09 Apr 2026 23:13:43 GMT
RUN a2enmod rewrite expires # buildkit
# Thu, 09 Apr 2026 23:13:43 GMT
ARG YOURLS_VERSION=1.10.3
# Thu, 09 Apr 2026 23:13:43 GMT
ARG YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
# Thu, 09 Apr 2026 23:13:43 GMT
ENV YOURLS_VERSION=1.10.3
# Thu, 09 Apr 2026 23:13:43 GMT
ENV YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
# Thu, 09 Apr 2026 23:13:43 GMT
# ARGS: YOURLS_VERSION=1.10.3 YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Thu, 09 Apr 2026 23:13:43 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Thu, 09 Apr 2026 23:13:43 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 23:13:43 GMT
COPY files/vhost.conf /etc/apache2/sites-available/000-default.conf # buildkit
# Thu, 09 Apr 2026 23:13:43 GMT
COPY files/vhost-https.conf /etc/apache2/sites-available/default-ssl.conf # buildkit
# Thu, 09 Apr 2026 23:13:43 GMT
COPY files/ports.conf /etc/apache2/ports.conf # buildkit
# Thu, 09 Apr 2026 23:13:43 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 09 Apr 2026 23:13:43 GMT
EXPOSE map[8443/tcp:{}]
# Thu, 09 Apr 2026 23:13:43 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Thu, 09 Apr 2026 23:13:43 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:5435b2dcdf5cb7faa0d5b1d4d54be2c72a776fab9a605336f5067d6e9ecb5976`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 29.8 MB (29775640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c7db4a70ef5aa708b5ca7fc754bbe3d01eb24e9ceafbf9a4da84a06dae738f5`  
		Last Modified: Thu, 09 Apr 2026 22:15:39 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e715735ff63a82824c8fac5cd6a870cc7ceebdde61b815ad4ef08c5a18c32651`  
		Last Modified: Thu, 09 Apr 2026 22:15:43 GMT  
		Size: 120.8 MB (120797883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0945ee5e8db480385c9e3fa06d0ccc85fd3e4852d116f01b4389b8865f93d91d`  
		Last Modified: Thu, 09 Apr 2026 22:15:39 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3769a9846acf8facf9f6fae1710f9a0202aace284bf9d15a4e341e6868028799`  
		Last Modified: Thu, 09 Apr 2026 22:15:39 GMT  
		Size: 4.2 MB (4227171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1c8b82e7a27ae7941cb85fcafb8e76bd80c58d58a640fdbc5eb0716bba27b08`  
		Last Modified: Thu, 09 Apr 2026 22:15:40 GMT  
		Size: 431.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9ba52b6db0aeb2a680b6033771bec77abed5819a815e18a2f9d9fb82c280abb`  
		Last Modified: Thu, 09 Apr 2026 22:15:40 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4353c28c1ac7b0321ec55c50686a62fe4e80dd50c61b6f915413ffc318921774`  
		Last Modified: Thu, 09 Apr 2026 22:15:42 GMT  
		Size: 14.5 MB (14522679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e021796a72d1a4c839e0eb0cdcdaa35903480dbdc040f48cc8bbc9bc0dbc2a91`  
		Last Modified: Thu, 09 Apr 2026 22:15:41 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65b00f27e36fb18a42a7ddf38b06fca050a6aa4e2204f739b580a5443d95515`  
		Last Modified: Thu, 09 Apr 2026 22:15:43 GMT  
		Size: 15.0 MB (15010577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60872a09cd81401500d17f1dbb53b1f78fbfacf9e944c303ae9d5788630b8624`  
		Last Modified: Thu, 09 Apr 2026 22:15:43 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ab4a308406fec4ac4e36dcd852cc5618d28f15a940f0b96269e9abb78aaaf12`  
		Last Modified: Thu, 09 Apr 2026 22:15:43 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96b0748adb1d3cf8d33f9e36a9b16e8658a95d9497c0f84d1a2297d6fb32b5a5`  
		Last Modified: Thu, 09 Apr 2026 22:15:44 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af3c67851ebc126e498238eac96b632840d09ee7f2d87bb27ec80e290a790e04`  
		Last Modified: Thu, 09 Apr 2026 23:13:49 GMT  
		Size: 108.4 KB (108376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2388d73b600b0b8772f497dc37fdad7097e4a36e3e443e40a569865f96de61c`  
		Last Modified: Thu, 09 Apr 2026 23:13:49 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f240f2adc978c080d23f237889c6f04b0b117a6dcd657f3ac8462b20e664180`  
		Last Modified: Thu, 09 Apr 2026 23:13:49 GMT  
		Size: 344.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bba95ced740eefe5c3de797313f6920d4be56ff561e37f1d4476c3b0b00be84c`  
		Last Modified: Thu, 09 Apr 2026 23:13:49 GMT  
		Size: 6.0 MB (6048926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38c273c0eab4004ef621a584b67774213cd6a5ddf584447c94af6091d11f2916`  
		Last Modified: Thu, 09 Apr 2026 23:13:50 GMT  
		Size: 2.1 KB (2095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c2d4826a2ac945f70f1d677aa1f39b145cb4eb96489d06adf7dbc65830ffbd6`  
		Last Modified: Thu, 09 Apr 2026 23:13:50 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fad4116a824ffb49288e63ca65f553ea1d47b3a42e76d4606b3e9b08acd8817`  
		Last Modified: Thu, 09 Apr 2026 23:13:50 GMT  
		Size: 499.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:183bb42eb5eaf4ba34c75f94a0dd790123be0efe6e3e08128fa5f7c86cc7ddc1`  
		Last Modified: Thu, 09 Apr 2026 23:13:50 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4f5c77ece25ab6202aa37879e6cbdae641ac5bcd5b9090559f674715f26a6c0`  
		Last Modified: Thu, 09 Apr 2026 23:13:51 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:latest` - unknown; unknown

```console
$ docker pull yourls@sha256:ccc075582f1b629837f7f3ae10a1911a53773469a0ae4006b5bdfbfa70bba4b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.6 KB (47589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75bdc8847251fd398bd9ecdd46f076665e86f1a6f5ebef5dc25446f2b959b952`

```dockerfile
```

-	Layers:
	-	`sha256:27b97d0bda4bf354fd60ac7ebdeaa65fa6739d1217d9b7c6fb0587906071ab37`  
		Last Modified: Thu, 09 Apr 2026 23:13:48 GMT  
		Size: 47.6 KB (47589 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:latest` - linux; arm variant v5

```console
$ docker pull yourls@sha256:6561c854814d0cbc0b67adf3b4e1c009d5f5a0f905aed21b829295145d254c8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.1 MB (163082027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec8563f1fe2a71afb41aa3d6c89f802c3e18b4362eaf36b7ef4df47b9f809a19`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1775433600'
# Thu, 09 Apr 2026 22:16:12 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 09 Apr 2026 22:16:44 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 09 Apr 2026 22:16:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 09 Apr 2026 22:16:44 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 09 Apr 2026 22:16:44 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 09 Apr 2026 22:16:44 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 09 Apr 2026 22:16:44 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 09 Apr 2026 22:16:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 09 Apr 2026 22:16:54 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 09 Apr 2026 22:16:54 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 09 Apr 2026 22:16:54 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 09 Apr 2026 22:16:54 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 09 Apr 2026 22:16:54 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 09 Apr 2026 22:16:54 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Thu, 09 Apr 2026 22:16:54 GMT
ENV PHP_VERSION=8.5.5
# Thu, 09 Apr 2026 22:16:54 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.5.tar.xz.asc
# Thu, 09 Apr 2026 22:16:54 GMT
ENV PHP_SHA256=95bec382f4bd00570a8ef52a58ec04d8d9b9a90494781f1c106d1b274a3902f2
# Thu, 09 Apr 2026 22:17:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 09 Apr 2026 22:17:07 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 22:20:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 09 Apr 2026 22:20:37 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 22:20:37 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 09 Apr 2026 22:20:37 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 09 Apr 2026 22:20:37 GMT
STOPSIGNAL SIGWINCH
# Thu, 09 Apr 2026 22:20:37 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 22:20:37 GMT
WORKDIR /var/www/html
# Thu, 09 Apr 2026 22:20:37 GMT
EXPOSE map[80/tcp:{}]
# Thu, 09 Apr 2026 22:20:37 GMT
CMD ["apache2-foreground"]
# Thu, 09 Apr 2026 23:19:42 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)"     bcmath     pdo_mysql     mysqli # buildkit
# Thu, 09 Apr 2026 23:19:42 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Thu, 09 Apr 2026 23:19:42 GMT
RUN a2enmod rewrite expires # buildkit
# Thu, 09 Apr 2026 23:19:43 GMT
ARG YOURLS_VERSION=1.10.3
# Thu, 09 Apr 2026 23:19:43 GMT
ARG YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
# Thu, 09 Apr 2026 23:19:43 GMT
ENV YOURLS_VERSION=1.10.3
# Thu, 09 Apr 2026 23:19:43 GMT
ENV YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
# Thu, 09 Apr 2026 23:19:43 GMT
# ARGS: YOURLS_VERSION=1.10.3 YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Thu, 09 Apr 2026 23:19:43 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Thu, 09 Apr 2026 23:19:43 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 23:19:43 GMT
COPY files/vhost.conf /etc/apache2/sites-available/000-default.conf # buildkit
# Thu, 09 Apr 2026 23:19:43 GMT
COPY files/vhost-https.conf /etc/apache2/sites-available/default-ssl.conf # buildkit
# Thu, 09 Apr 2026 23:19:43 GMT
COPY files/ports.conf /etc/apache2/ports.conf # buildkit
# Thu, 09 Apr 2026 23:19:43 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 09 Apr 2026 23:19:43 GMT
EXPOSE map[8443/tcp:{}]
# Thu, 09 Apr 2026 23:19:43 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Thu, 09 Apr 2026 23:19:43 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:3a32056c13d69abfd2a107f36cfc2049bdb6b52dbb76427fb9c1f688273f6bce`  
		Last Modified: Tue, 07 Apr 2026 00:11:10 GMT  
		Size: 27.9 MB (27943808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80917709d208d17ac60eb023eb9055ddba2aee5700510ea8fc95a7f009336279`  
		Last Modified: Thu, 09 Apr 2026 22:19:28 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61258591951b659ada571cfb44c0eb5c82612c0dd0b0aba20c5164bc5907e543`  
		Last Modified: Thu, 09 Apr 2026 22:21:00 GMT  
		Size: 97.3 MB (97252921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd11d988ae198bb657efdf524c59ec7b6a9595de01b48b3bd02545c272d909b3`  
		Last Modified: Thu, 09 Apr 2026 22:20:57 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd0820dcfef4a1ad1007ccfb411a6d9a3646f6ffcdd7c7630cf49b21fb26ae4f`  
		Last Modified: Thu, 09 Apr 2026 22:20:57 GMT  
		Size: 4.1 MB (4089502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:addd0616f24fb76c836dab4057ab829d25acc7461a04e11ff34814177fdf533f`  
		Last Modified: Thu, 09 Apr 2026 22:20:58 GMT  
		Size: 426.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6f196cf4dff23c583d1a6dcabcebaf5a769c728112b2456217c84f48198eb2c`  
		Last Modified: Thu, 09 Apr 2026 22:20:58 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d4eed0d9324834f5b7f2f902a1fa68508cc0f29eecf8cfd5e92659241957cd7`  
		Last Modified: Thu, 09 Apr 2026 22:20:59 GMT  
		Size: 14.5 MB (14519949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:680bc7c49ae6916cb0c5ea875cc412f665572641de65c2e3eeac3a45c4b010ba`  
		Last Modified: Thu, 09 Apr 2026 22:20:59 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:096cbc33dfcdcef015c9134fc4b4c71d2fae70b2e3cb64427657b959707aba1b`  
		Last Modified: Thu, 09 Apr 2026 22:21:00 GMT  
		Size: 13.1 MB (13118660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92cf92755ad188c6cdfe2b8c8bab32deb08d616ab1b8daafce65dd5b17c156bc`  
		Last Modified: Thu, 09 Apr 2026 22:21:00 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2287e8ba7679a700bef737fdd36b4876f48ca7368416ed1e8d3378d74edbcc94`  
		Last Modified: Thu, 09 Apr 2026 22:21:00 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:958acb90dc63ed2a58e5c522d7f17efe59532ad387a702453050dfe24299eeb7`  
		Last Modified: Thu, 09 Apr 2026 22:21:01 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eb672f65d620e1decc9fb54ec84f0cad149d64a5d269b5a0002da087649f11c`  
		Last Modified: Thu, 09 Apr 2026 23:19:49 GMT  
		Size: 97.0 KB (96964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e532179c82c89c813f0507f8b45644fcdaa4dcf7695bf9f8216ea5cec9a95c`  
		Last Modified: Thu, 09 Apr 2026 23:19:48 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8df5193e49b14505e370822d4ab7f264be9aaf2b39de726e23bb9d50bd40538c`  
		Last Modified: Thu, 09 Apr 2026 23:19:48 GMT  
		Size: 342.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf7d2581ffeaa1a8d9846271515bbedcd296c211f92d7acba86d249dc47b295e`  
		Last Modified: Thu, 09 Apr 2026 23:19:49 GMT  
		Size: 6.0 MB (6048926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9789093fd8458a34822d341ac98abde7cd26c77db2f0c25fcda039331db82a39`  
		Last Modified: Thu, 09 Apr 2026 23:19:49 GMT  
		Size: 2.1 KB (2093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e283f6f8677f7d2c0a85071563411381709683e5b969a671fe0be6145ff4df11`  
		Last Modified: Thu, 09 Apr 2026 23:19:50 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a12139f83d1f74e859dfb0e646e92f4c2471620110e1c4c6ebf65bd0668569f0`  
		Last Modified: Thu, 09 Apr 2026 23:19:50 GMT  
		Size: 499.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a52f5a9d84594c50ea5de306d5cbf9155f4f068f72265a2b696d21e068051fd8`  
		Last Modified: Thu, 09 Apr 2026 23:19:50 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f6c956b4d6b8163f926617ebe26f2715f7d4cc7530dc8134fe7aca081831048`  
		Last Modified: Thu, 09 Apr 2026 23:19:51 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:latest` - unknown; unknown

```console
$ docker pull yourls@sha256:8fa626067c036e251dff736989c411c2606497ae59e391262207bb7366737b15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 KB (47721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4028546ccd3c1bdaded7a5348d620fcea36cec0cb9b775e016c1d853f0c382f6`

```dockerfile
```

-	Layers:
	-	`sha256:5704aedbbcee669045b67c685b89ea0b143876896b405b716bbaee399413cd24`  
		Last Modified: Thu, 09 Apr 2026 23:19:48 GMT  
		Size: 47.7 KB (47721 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:latest` - linux; arm variant v7

```console
$ docker pull yourls@sha256:a963a1e34d8015892fd7e11119313b2d6dd8f296aa5010a1af37fc73dd453f7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.6 MB (151602612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0658b3b10c9fe9439b59eaf14ff804103db0974b6c7073633c00bdb35738488`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1775433600'
# Thu, 09 Apr 2026 22:11:58 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 09 Apr 2026 22:12:16 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 09 Apr 2026 22:12:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 09 Apr 2026 22:12:16 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 09 Apr 2026 22:12:16 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 09 Apr 2026 22:12:16 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 09 Apr 2026 22:12:16 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 09 Apr 2026 22:12:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 09 Apr 2026 22:12:23 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 09 Apr 2026 22:12:24 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 09 Apr 2026 22:12:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 09 Apr 2026 22:12:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 09 Apr 2026 22:12:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 09 Apr 2026 22:12:24 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Thu, 09 Apr 2026 22:12:24 GMT
ENV PHP_VERSION=8.5.5
# Thu, 09 Apr 2026 22:12:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.5.tar.xz.asc
# Thu, 09 Apr 2026 22:12:24 GMT
ENV PHP_SHA256=95bec382f4bd00570a8ef52a58ec04d8d9b9a90494781f1c106d1b274a3902f2
# Thu, 09 Apr 2026 22:12:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 09 Apr 2026 22:12:34 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 22:15:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 09 Apr 2026 22:15:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 22:15:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 09 Apr 2026 22:15:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 09 Apr 2026 22:15:32 GMT
STOPSIGNAL SIGWINCH
# Thu, 09 Apr 2026 22:15:32 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 22:15:32 GMT
WORKDIR /var/www/html
# Thu, 09 Apr 2026 22:15:32 GMT
EXPOSE map[80/tcp:{}]
# Thu, 09 Apr 2026 22:15:32 GMT
CMD ["apache2-foreground"]
# Thu, 09 Apr 2026 23:23:29 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)"     bcmath     pdo_mysql     mysqli # buildkit
# Thu, 09 Apr 2026 23:23:29 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Thu, 09 Apr 2026 23:23:29 GMT
RUN a2enmod rewrite expires # buildkit
# Thu, 09 Apr 2026 23:23:30 GMT
ARG YOURLS_VERSION=1.10.3
# Thu, 09 Apr 2026 23:23:30 GMT
ARG YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
# Thu, 09 Apr 2026 23:23:30 GMT
ENV YOURLS_VERSION=1.10.3
# Thu, 09 Apr 2026 23:23:30 GMT
ENV YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
# Thu, 09 Apr 2026 23:23:30 GMT
# ARGS: YOURLS_VERSION=1.10.3 YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Thu, 09 Apr 2026 23:23:30 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Thu, 09 Apr 2026 23:23:30 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 23:23:30 GMT
COPY files/vhost.conf /etc/apache2/sites-available/000-default.conf # buildkit
# Thu, 09 Apr 2026 23:23:30 GMT
COPY files/vhost-https.conf /etc/apache2/sites-available/default-ssl.conf # buildkit
# Thu, 09 Apr 2026 23:23:30 GMT
COPY files/ports.conf /etc/apache2/ports.conf # buildkit
# Thu, 09 Apr 2026 23:23:30 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 09 Apr 2026 23:23:30 GMT
EXPOSE map[8443/tcp:{}]
# Thu, 09 Apr 2026 23:23:30 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Thu, 09 Apr 2026 23:23:30 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:4c6d27739d1db2f26843c4e427219b60cd29d0d75a2f4c9eae2e732971275433`  
		Last Modified: Tue, 07 Apr 2026 01:00:39 GMT  
		Size: 26.2 MB (26209653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0951be236376ba73e378d6249050d9e17212df68387f6ad4c25896708d61ca70`  
		Last Modified: Thu, 09 Apr 2026 22:15:49 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cb23b7ee9a65a65833526324b6c205b0172e49875aabb82aa347057d3fc96c4`  
		Last Modified: Thu, 09 Apr 2026 22:15:54 GMT  
		Size: 88.5 MB (88463433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea82348423a1832677700208334d1d85fbc0dc7725bee2699f5fb9a9ddc7f434`  
		Last Modified: Thu, 09 Apr 2026 22:15:49 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b19c3b8561190cd6134c617cdaa0a2aa2fffa94785f9e82eb78bf6ab665f5e2`  
		Last Modified: Thu, 09 Apr 2026 22:15:50 GMT  
		Size: 3.8 MB (3757403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:700ddcb3a74665bfdec86bfd4a10b5e65713045a4e2090465d4c9dd026bd389d`  
		Last Modified: Thu, 09 Apr 2026 22:15:51 GMT  
		Size: 427.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:231e6b2e1cb21854080db16b9d0c16b9507c8cec7cefcbd9168b29c1b00843e7`  
		Last Modified: Thu, 09 Apr 2026 22:15:51 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:398f8f110edd92d5e815add213a3f3b4fbcd4e84e0041c9a1ce49d4c24d3d161`  
		Last Modified: Thu, 09 Apr 2026 22:15:51 GMT  
		Size: 14.5 MB (14520073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cae77864127e77473a3c69ca40b920665e57e8f7e225d847ccb3127113509b5`  
		Last Modified: Thu, 09 Apr 2026 22:15:52 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6e2b0ea5fcb6d1bf625e880350a3613e3ffb8fec7a9f5983eb8c8b08b4c1655`  
		Last Modified: Thu, 09 Apr 2026 22:15:52 GMT  
		Size: 12.5 MB (12500952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63f3466e7869aa045a965f6d8070e6316cd7cd1bf6729ba546f2a99b5798fcd1`  
		Last Modified: Thu, 09 Apr 2026 22:15:53 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc2657dbb614523cdd3d74f1db155e84f5db1f7e114794af366e915b89a2aca9`  
		Last Modified: Thu, 09 Apr 2026 22:15:53 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d2d805a8ec2a503481c6e2b1aacceb7fc5185baeb029815f14c7dc56e4ef0a8`  
		Last Modified: Thu, 09 Apr 2026 22:15:54 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d46b28a9ad28d1be6a55ceca0d364e9838559d0281925a0a347c8d1f1c136f7`  
		Last Modified: Thu, 09 Apr 2026 23:23:35 GMT  
		Size: 90.9 KB (90871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8cee3752ab303faa232fad3513ad5ecfcf2f71337abac23c06fdaf48da15177`  
		Last Modified: Thu, 09 Apr 2026 23:23:35 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fae8cee43fde8de56812dc217d94abb850643a9043ed54518abc905ceee8ccc4`  
		Last Modified: Thu, 09 Apr 2026 23:23:35 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33afed349b865c7924e62da83e5e9cae3abb1b155db8ba2610d89306e378aa19`  
		Last Modified: Thu, 09 Apr 2026 23:23:35 GMT  
		Size: 6.0 MB (6048923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4909209ad6085754c8dfff04ea8b04dfdeb94b3c63f9adb9608bfb051241c77`  
		Last Modified: Thu, 09 Apr 2026 23:23:36 GMT  
		Size: 2.1 KB (2092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b43347a80075437b9133b443db94a7149c6bd38ce5b2a207b44a7cee607e2115`  
		Last Modified: Thu, 09 Apr 2026 23:23:36 GMT  
		Size: 1.7 KB (1694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9404e954a18dd12420c15521a97d1fb710c900e0a68fe9645bdd3c450021047`  
		Last Modified: Thu, 09 Apr 2026 23:23:36 GMT  
		Size: 500.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88e4d848b65af635853a67d2c5f2f32ff8d4260ad6f573b407f164ec32c663cc`  
		Last Modified: Thu, 09 Apr 2026 23:23:37 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19ff2e621059aa345c44c5b9b73a96e6b5821c36fd6896201818d21346b7467c`  
		Last Modified: Thu, 09 Apr 2026 23:23:37 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:latest` - unknown; unknown

```console
$ docker pull yourls@sha256:729c332e7e0ebeea0616cbfdecb09548cc07fe5d0191dbccaf8355d1a7c579be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 KB (47721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2170cd2692d130690367aebc2ac1e1042d30e457c835a0afe233bc30d2346ee8`

```dockerfile
```

-	Layers:
	-	`sha256:7036532153683faa47be30d3cf8da4a6c3d4eb58861fec470c08687be0b930f7`  
		Last Modified: Thu, 09 Apr 2026 23:23:35 GMT  
		Size: 47.7 KB (47721 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:latest` - linux; arm64 variant v8

```console
$ docker pull yourls@sha256:c715f679c0bd2da675e6d37c18f4fbde6bf9332d07ddd45ca320a829b34af34a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.2 MB (183212332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f656039a302d774161cd40bc887234fd2f9c4974289a72566f759a36e76b302e`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Thu, 09 Apr 2026 22:11:58 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 09 Apr 2026 22:12:16 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 09 Apr 2026 22:12:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 09 Apr 2026 22:12:16 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 09 Apr 2026 22:12:16 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 09 Apr 2026 22:12:16 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 09 Apr 2026 22:12:16 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 09 Apr 2026 22:12:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 09 Apr 2026 22:12:23 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 09 Apr 2026 22:12:23 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 09 Apr 2026 22:12:23 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 09 Apr 2026 22:12:23 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 09 Apr 2026 22:12:23 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 09 Apr 2026 22:12:23 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Thu, 09 Apr 2026 22:12:23 GMT
ENV PHP_VERSION=8.5.5
# Thu, 09 Apr 2026 22:12:23 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.5.tar.xz.asc
# Thu, 09 Apr 2026 22:12:23 GMT
ENV PHP_SHA256=95bec382f4bd00570a8ef52a58ec04d8d9b9a90494781f1c106d1b274a3902f2
# Thu, 09 Apr 2026 22:12:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 09 Apr 2026 22:12:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 22:15:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 09 Apr 2026 22:15:44 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 22:15:45 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 09 Apr 2026 22:15:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 09 Apr 2026 22:15:45 GMT
STOPSIGNAL SIGWINCH
# Thu, 09 Apr 2026 22:15:45 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 22:15:45 GMT
WORKDIR /var/www/html
# Thu, 09 Apr 2026 22:15:45 GMT
EXPOSE map[80/tcp:{}]
# Thu, 09 Apr 2026 22:15:45 GMT
CMD ["apache2-foreground"]
# Thu, 09 Apr 2026 23:14:09 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)"     bcmath     pdo_mysql     mysqli # buildkit
# Thu, 09 Apr 2026 23:14:09 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Thu, 09 Apr 2026 23:14:09 GMT
RUN a2enmod rewrite expires # buildkit
# Thu, 09 Apr 2026 23:14:10 GMT
ARG YOURLS_VERSION=1.10.3
# Thu, 09 Apr 2026 23:14:10 GMT
ARG YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
# Thu, 09 Apr 2026 23:14:10 GMT
ENV YOURLS_VERSION=1.10.3
# Thu, 09 Apr 2026 23:14:10 GMT
ENV YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
# Thu, 09 Apr 2026 23:14:10 GMT
# ARGS: YOURLS_VERSION=1.10.3 YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Thu, 09 Apr 2026 23:14:10 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Thu, 09 Apr 2026 23:14:10 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 23:14:10 GMT
COPY files/vhost.conf /etc/apache2/sites-available/000-default.conf # buildkit
# Thu, 09 Apr 2026 23:14:10 GMT
COPY files/vhost-https.conf /etc/apache2/sites-available/default-ssl.conf # buildkit
# Thu, 09 Apr 2026 23:14:10 GMT
COPY files/ports.conf /etc/apache2/ports.conf # buildkit
# Thu, 09 Apr 2026 23:14:10 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 09 Apr 2026 23:14:10 GMT
EXPOSE map[8443/tcp:{}]
# Thu, 09 Apr 2026 23:14:10 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Thu, 09 Apr 2026 23:14:10 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:53196b1f47bdd6997874156c61491c9a36e115d9b7bd5d74e0cb5c2fc4ee69ce`  
		Last Modified: Tue, 07 Apr 2026 00:11:28 GMT  
		Size: 30.1 MB (30138551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5de5ef7a06ec9f00b1f365779dbc7cd9d13a38a5c2817ec996efa4ed52a3ac39`  
		Last Modified: Thu, 09 Apr 2026 22:16:06 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48f31afc6cbc851ec55f0c5a1768ea9d5a93e09d95394728a9e64a7b33e16992`  
		Last Modified: Thu, 09 Apr 2026 22:16:09 GMT  
		Size: 113.5 MB (113507074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea82348423a1832677700208334d1d85fbc0dc7725bee2699f5fb9a9ddc7f434`  
		Last Modified: Thu, 09 Apr 2026 22:15:49 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a13cae6711ad9f25bf1c0475f269c57263045673f58c36026bd3a125985807a0`  
		Last Modified: Thu, 09 Apr 2026 22:16:06 GMT  
		Size: 4.3 MB (4305687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72566a5a814c6dd6783136d46f245d3e73e62fad282ab4e23e748da2e57ac679`  
		Last Modified: Thu, 09 Apr 2026 22:16:07 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54d1cfe3fcefdd346b52ad92014e99d9db75b1ad6f6996c2cc9b88a61da1c38b`  
		Last Modified: Thu, 09 Apr 2026 22:16:07 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f360416ae7aeeea67ff455a29becdc6ec64aa6af20c6a6df6148d156c2beaa00`  
		Last Modified: Thu, 09 Apr 2026 22:16:08 GMT  
		Size: 14.5 MB (14522248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6df6c2d89ea47d4c4359f9989bfdd87a3a317641dc7b438c426a7aaaaafaf753`  
		Last Modified: Thu, 09 Apr 2026 22:16:08 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de4be27263bc4305215574b50b10b2dad2689ed570ab172489d8d5dcaae79be5`  
		Last Modified: Thu, 09 Apr 2026 22:16:09 GMT  
		Size: 14.6 MB (14572785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7241a63001c41b8e652f7826cf44335ad180535dc0dd350ddb9e97b6aec7e8c7`  
		Last Modified: Thu, 09 Apr 2026 22:16:09 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af6cb7097247eabf9fcde5f92eafb090b4eb5dc7011694563a22466006a4b678`  
		Last Modified: Thu, 09 Apr 2026 22:16:09 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:437a2cba1a9b2c245395a9c2bf56958dbf0acc7d6d542ef19ec495a797fa4f8b`  
		Last Modified: Thu, 09 Apr 2026 22:16:10 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da8b02f5dbf227a3a85a3b64ffa0b679599bd7eb2b42eb102b5483f1ee592bda`  
		Last Modified: Thu, 09 Apr 2026 23:14:15 GMT  
		Size: 105.7 KB (105746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e145a7a5a584c9c3430115de856820c17ccc37967b742e5fa9974470eb3e45a3`  
		Last Modified: Thu, 09 Apr 2026 23:14:15 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da37ff32527d114c69cad6d0a4fc74cc58a406cb52f902b41cd654deab50b5e9`  
		Last Modified: Thu, 09 Apr 2026 23:14:15 GMT  
		Size: 344.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63fd8297b1bd1f01dffead3d188b41e9e4d05e13ea6041a8171c83008716d76b`  
		Last Modified: Thu, 09 Apr 2026 23:14:15 GMT  
		Size: 6.0 MB (6048925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41a8e4a554c71059c6aa0ada1e66007040a7735e7ebbfe2028e45419a04c5374`  
		Last Modified: Thu, 09 Apr 2026 23:14:16 GMT  
		Size: 2.1 KB (2096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c951f3a680f34f7040edac2b690dcd9bf8e09eaf66b8207153276429e56fce2`  
		Last Modified: Thu, 09 Apr 2026 23:14:16 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f578d520bae5a4d9f9b0516aabe262e4f28a64d5c5661ffa712ca68f6d5040`  
		Last Modified: Thu, 09 Apr 2026 23:14:17 GMT  
		Size: 500.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:241461bb43d009a17a3bf041b7947bb1a17174d464a80c856a8112633aca6898`  
		Last Modified: Thu, 09 Apr 2026 23:14:17 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c91a84bcdb3fbd184f2214c726f17704ebe08dc4e6f3141a3a27c773b8864be`  
		Last Modified: Thu, 09 Apr 2026 23:14:17 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:latest` - unknown; unknown

```console
$ docker pull yourls@sha256:8a6b552c407347b93c6c9df937b63c2a942db68db14d902e84148158e78acf58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 KB (47786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:851cc2b2fe3fb2536ea79d097c049ef10f3d826d74009eda378a8186bfc3ba19`

```dockerfile
```

-	Layers:
	-	`sha256:cfba2a35095855095b65846b37cddb582329f4523f38e13a3424ce164fcc73d0`  
		Last Modified: Thu, 09 Apr 2026 23:14:15 GMT  
		Size: 47.8 KB (47786 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:latest` - linux; 386

```console
$ docker pull yourls@sha256:9e5ec8abfea055ae8b7313519a722a696ca5d12ecf0a687b498bd57ea9a9a502
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.8 MB (190834658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ae1204ed29996bfb721b37a5a7643140b4b45d2980c32f271bf00fd6c72cbdd`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1775433600'
# Fri, 10 Apr 2026 00:12:34 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 10 Apr 2026 00:12:54 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 10 Apr 2026 00:12:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Fri, 10 Apr 2026 00:12:54 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 10 Apr 2026 00:12:54 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 10 Apr 2026 00:12:54 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 10 Apr 2026 00:12:54 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 10 Apr 2026 00:13:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 10 Apr 2026 00:13:01 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 10 Apr 2026 00:13:01 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 10 Apr 2026 00:13:01 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 10 Apr 2026 00:13:01 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 10 Apr 2026 00:13:01 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 10 Apr 2026 00:13:01 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Fri, 10 Apr 2026 00:13:01 GMT
ENV PHP_VERSION=8.5.5
# Fri, 10 Apr 2026 00:13:01 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.5.tar.xz.asc
# Fri, 10 Apr 2026 00:13:01 GMT
ENV PHP_SHA256=95bec382f4bd00570a8ef52a58ec04d8d9b9a90494781f1c106d1b274a3902f2
# Fri, 10 Apr 2026 00:13:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 10 Apr 2026 00:13:12 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 10 Apr 2026 00:16:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 10 Apr 2026 00:16:41 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 10 Apr 2026 00:16:41 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 10 Apr 2026 00:16:41 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 10 Apr 2026 00:16:41 GMT
STOPSIGNAL SIGWINCH
# Fri, 10 Apr 2026 00:16:41 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 10 Apr 2026 00:16:41 GMT
WORKDIR /var/www/html
# Fri, 10 Apr 2026 00:16:41 GMT
EXPOSE map[80/tcp:{}]
# Fri, 10 Apr 2026 00:16:41 GMT
CMD ["apache2-foreground"]
# Fri, 10 Apr 2026 03:29:16 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)"     bcmath     pdo_mysql     mysqli # buildkit
# Fri, 10 Apr 2026 03:29:17 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Fri, 10 Apr 2026 03:29:17 GMT
RUN a2enmod rewrite expires # buildkit
# Fri, 10 Apr 2026 03:29:18 GMT
ARG YOURLS_VERSION=1.10.3
# Fri, 10 Apr 2026 03:29:18 GMT
ARG YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
# Fri, 10 Apr 2026 03:29:18 GMT
ENV YOURLS_VERSION=1.10.3
# Fri, 10 Apr 2026 03:29:18 GMT
ENV YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
# Fri, 10 Apr 2026 03:29:18 GMT
# ARGS: YOURLS_VERSION=1.10.3 YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Fri, 10 Apr 2026 03:29:18 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Fri, 10 Apr 2026 03:29:18 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 10 Apr 2026 03:29:18 GMT
COPY files/vhost.conf /etc/apache2/sites-available/000-default.conf # buildkit
# Fri, 10 Apr 2026 03:29:18 GMT
COPY files/vhost-https.conf /etc/apache2/sites-available/default-ssl.conf # buildkit
# Fri, 10 Apr 2026 03:29:18 GMT
COPY files/ports.conf /etc/apache2/ports.conf # buildkit
# Fri, 10 Apr 2026 03:29:18 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 10 Apr 2026 03:29:18 GMT
EXPOSE map[8443/tcp:{}]
# Fri, 10 Apr 2026 03:29:18 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Fri, 10 Apr 2026 03:29:18 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:3c3d391a832256e6eca1fcef63254ce2b8cf2d25bc53ac0b56d9de64a11a7f30`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 31.3 MB (31291252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9447e5c319c2e28b58a2f0572fcc1c2377ca08c891c0c1899a478018558682d3`  
		Last Modified: Fri, 10 Apr 2026 00:17:03 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2e86d74ca80c1b116d29685c8f05327a326cdded9e5150f72c61ad123ede3e5`  
		Last Modified: Fri, 10 Apr 2026 00:17:09 GMT  
		Size: 119.0 MB (119027764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3637dce8b6bf6b9a90db00c2c2e49e157a5e3bb5f867d622ffe31bc4187c223`  
		Last Modified: Fri, 10 Apr 2026 00:17:03 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09acf383e3e3fc2661b6f80602a3f2a9efbd4c915b4cbcf26bacf6b66c70047a`  
		Last Modified: Fri, 10 Apr 2026 00:17:04 GMT  
		Size: 4.5 MB (4458665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57aacd7d62b741985a30ed732366b7e907facc5734238520e8a49e199b9d39f7`  
		Last Modified: Fri, 10 Apr 2026 00:17:04 GMT  
		Size: 427.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deb887662c1cbfa9b12b5f467fd6b5a535b9f73537f34eb47c75389782606140`  
		Last Modified: Fri, 10 Apr 2026 00:17:04 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e76ad5da162f5d00b6d4af736369e607c74224cc22cdce69609f8f9ef55fbd3`  
		Last Modified: Fri, 10 Apr 2026 00:17:07 GMT  
		Size: 14.5 MB (14521594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b5ac4451adf49a611d68dc5192611173bc2db789e7aea52820cb274e6f9732`  
		Last Modified: Fri, 10 Apr 2026 00:17:06 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8165b5dd0c58712b150fe4e6fca281b6fe056ce7184a577b8709a44ea17d0d61`  
		Last Modified: Fri, 10 Apr 2026 00:17:08 GMT  
		Size: 15.4 MB (15363324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37ab8f2e1fc9188bf3f757745fdc93af6d72a0bf5865b337e3bde2685efd2ce4`  
		Last Modified: Fri, 10 Apr 2026 00:17:08 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c11999cafacd237ae966a222b485dabdd944f136cb5b00118063a9122f56745`  
		Last Modified: Fri, 10 Apr 2026 00:17:09 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16811b9f2b86fd65e5090267c2eb4b40cb7abc32bfe5424c776e38bcfcd79e39`  
		Last Modified: Fri, 10 Apr 2026 00:17:09 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80a427055fec077085dae62fc9ff048da602a9ba45c6ca4db8330b889fd531d1`  
		Last Modified: Fri, 10 Apr 2026 03:29:23 GMT  
		Size: 111.8 KB (111827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e5370f6fe50faca6448891d9490826f159ecdf475c3f250f9d1c3d43f7af3a`  
		Last Modified: Fri, 10 Apr 2026 03:29:23 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:985fd06aac934a49d4990ce5936c172a885e5ed440d32e0f9fe83d30871f65d9`  
		Last Modified: Fri, 10 Apr 2026 03:29:23 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f56adc9e1777a56c7f27b59f695b4757d52b3290bef8665887742eb3cc95ff8`  
		Last Modified: Fri, 10 Apr 2026 03:29:24 GMT  
		Size: 6.0 MB (6048926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d78052e1c21fe3845e188ca04e1a6281ad90e58bcc5e36702033ab63bf5ee3c`  
		Last Modified: Fri, 10 Apr 2026 03:29:24 GMT  
		Size: 2.1 KB (2095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:428b4fe3c9424dc8ae44860dd787948353ca4d9c0788e20d179d0df9335b810d`  
		Last Modified: Fri, 10 Apr 2026 03:29:24 GMT  
		Size: 1.7 KB (1694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a97385bf88628c4904f50b2775e80f00ae4f145f61ff1641ed469f52445e150b`  
		Last Modified: Fri, 10 Apr 2026 03:29:25 GMT  
		Size: 499.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6712f0b24a45476b3bf462973dd3dd7fff6004fdcefcff0c43b44e41e72648a`  
		Last Modified: Fri, 10 Apr 2026 03:29:25 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:950ea34d7ec6a46a3caf98aad37dc36a7177c5f542572688f8cc76225230b71c`  
		Last Modified: Fri, 10 Apr 2026 03:29:26 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:latest` - unknown; unknown

```console
$ docker pull yourls@sha256:ac7f68aac84a80895e09645e501b52d39aa71a975713b2a3a7a33b3579461f5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.5 KB (47531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72b59703dc7941443167850371003ede1d913b5c7b82850a7fefebda11ba6e05`

```dockerfile
```

-	Layers:
	-	`sha256:91f0d84a8ad59e4bf0f0e57487e5c080707767f455c6ad1c5a6e4528cde2eaa5`  
		Last Modified: Fri, 10 Apr 2026 03:29:23 GMT  
		Size: 47.5 KB (47531 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:latest` - linux; ppc64le

```console
$ docker pull yourls@sha256:b864a6ff5d7b80da11db8ed15271d6e3560e74ac4bcb201964ee1af4df4e7c44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.5 MB (187459617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dc46cac2b51e59a63802aeb2d25f23dd539a2710712bcdb0335e14f225e8201`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:52:18 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 07 Apr 2026 01:53:05 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 07 Apr 2026 01:53:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 01:53:05 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 07 Apr 2026 01:53:06 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 07 Apr 2026 01:53:06 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 07 Apr 2026 01:53:06 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 07 Apr 2026 02:15:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 07 Apr 2026 02:15:47 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 07 Apr 2026 02:15:48 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 07 Apr 2026 02:15:48 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 07 Apr 2026 02:15:48 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 07 Apr 2026 02:15:48 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 07 Apr 2026 02:15:48 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Tue, 07 Apr 2026 02:15:48 GMT
ENV PHP_VERSION=8.5.5
# Tue, 07 Apr 2026 02:15:48 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.5.tar.xz.asc
# Tue, 07 Apr 2026 02:15:48 GMT
ENV PHP_SHA256=95bec382f4bd00570a8ef52a58ec04d8d9b9a90494781f1c106d1b274a3902f2
# Thu, 09 Apr 2026 22:11:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 09 Apr 2026 22:11:29 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 22:17:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 09 Apr 2026 22:17:12 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 22:17:12 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 09 Apr 2026 22:17:12 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 09 Apr 2026 22:17:12 GMT
STOPSIGNAL SIGWINCH
# Thu, 09 Apr 2026 22:17:13 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 22:17:16 GMT
WORKDIR /var/www/html
# Thu, 09 Apr 2026 22:17:16 GMT
EXPOSE map[80/tcp:{}]
# Thu, 09 Apr 2026 22:17:16 GMT
CMD ["apache2-foreground"]
# Fri, 10 Apr 2026 00:17:01 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)"     bcmath     pdo_mysql     mysqli # buildkit
# Fri, 10 Apr 2026 00:17:03 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Fri, 10 Apr 2026 00:17:05 GMT
RUN a2enmod rewrite expires # buildkit
# Fri, 10 Apr 2026 00:17:09 GMT
ARG YOURLS_VERSION=1.10.3
# Fri, 10 Apr 2026 00:17:09 GMT
ARG YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
# Fri, 10 Apr 2026 00:17:09 GMT
ENV YOURLS_VERSION=1.10.3
# Fri, 10 Apr 2026 00:17:09 GMT
ENV YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
# Fri, 10 Apr 2026 00:17:09 GMT
# ARGS: YOURLS_VERSION=1.10.3 YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Fri, 10 Apr 2026 00:17:10 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Fri, 10 Apr 2026 00:17:11 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 10 Apr 2026 00:17:12 GMT
COPY files/vhost.conf /etc/apache2/sites-available/000-default.conf # buildkit
# Fri, 10 Apr 2026 00:17:12 GMT
COPY files/vhost-https.conf /etc/apache2/sites-available/default-ssl.conf # buildkit
# Fri, 10 Apr 2026 00:17:12 GMT
COPY files/ports.conf /etc/apache2/ports.conf # buildkit
# Fri, 10 Apr 2026 00:17:12 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 10 Apr 2026 00:17:12 GMT
EXPOSE map[8443/tcp:{}]
# Fri, 10 Apr 2026 00:17:12 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Fri, 10 Apr 2026 00:17:12 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:6e3428d4efac15fe7728b465c9c3bc5d71a07ad502becbd70250a2c560e32b53`  
		Last Modified: Tue, 07 Apr 2026 00:12:50 GMT  
		Size: 33.6 MB (33593016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cf9146bf73c8a452f415773cc4d7b28152e6a0132b4872c062036e93ceda4a1`  
		Last Modified: Tue, 07 Apr 2026 01:58:45 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f4a0e07fb6454284581cfcdd933b1a8aeaf834a24a8768bd1bdee7fe76ac43`  
		Last Modified: Tue, 07 Apr 2026 01:58:49 GMT  
		Size: 109.6 MB (109599084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d79e4f5187124bd689202e1c0b532dcdbfed0adfcf45354b5dcc246a80a88c8e`  
		Last Modified: Tue, 07 Apr 2026 01:58:45 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c2826d5bd7597d2bc055cec74a30953477482f418eb99bc191b54a5657bea0`  
		Last Modified: Tue, 07 Apr 2026 02:22:07 GMT  
		Size: 4.9 MB (4881630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bb4711f0a1e700d515af14d521ed74bc330dbff10a897db0c88f1da3017c82e`  
		Last Modified: Tue, 07 Apr 2026 02:22:06 GMT  
		Size: 432.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1ea076c7d43b09b2edeb333274a93e4615a067914cc9eb5a71e39816735581b`  
		Last Modified: Tue, 07 Apr 2026 02:22:06 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e2111ba7f1d1b92a7cc3b26dc049ef8d5c7949e2bd04bf453c78403b8545391`  
		Last Modified: Thu, 09 Apr 2026 22:17:41 GMT  
		Size: 14.5 MB (14536799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84711c5d24e01e0973e4361731ab0e5f723a8d2f30ab0ba5615de991403a0063`  
		Last Modified: Thu, 09 Apr 2026 22:17:12 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ade0d12e2306385ad41f4bcc65437706b8f0222cd822e6f14e90bb459694f4f`  
		Last Modified: Thu, 09 Apr 2026 22:17:41 GMT  
		Size: 18.7 MB (18671511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca9937a58dc8b3e35ec5febefc069c6396347cfe5a0b49d2925d727d8400f8cd`  
		Last Modified: Thu, 09 Apr 2026 22:17:40 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5ea58e9675ba1ca2a2f68a6b6c5b139fc1e7053b3109088f22630509d3df393`  
		Last Modified: Thu, 09 Apr 2026 22:17:40 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32516d3b6022be5e204b707f1e3be1f0b54a77f130411135643e440569a21bc3`  
		Last Modified: Thu, 09 Apr 2026 22:17:41 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8568d740ef8db3e667f19d0fe080de68772eef6bfd5f221f87a75dfed8fbe781`  
		Last Modified: Fri, 10 Apr 2026 00:17:24 GMT  
		Size: 117.3 KB (117319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ad875f40a92b9fe80046fd944cad10aa39abf68c09cef38c827b8471425326d`  
		Last Modified: Fri, 10 Apr 2026 00:17:24 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87a2b3611b6e96c0269cb02d59133ecd339726a7dee8bb2b9f6418d35b582a46`  
		Last Modified: Fri, 10 Apr 2026 00:17:24 GMT  
		Size: 351.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f17f0b2620ef9a0b90d279e4c3478b92ee749925c737781df652449edab18d60`  
		Last Modified: Fri, 10 Apr 2026 00:17:24 GMT  
		Size: 6.0 MB (6048926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71edf121f227b0fe287caf2aae11a4a7a131f5184eca9a9cae8be71ca468db9e`  
		Last Modified: Fri, 10 Apr 2026 00:17:25 GMT  
		Size: 2.1 KB (2097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ec066192b937f748640ae153366a70b0d884d33fa4ff4306ac2ee7e09e829da`  
		Last Modified: Fri, 10 Apr 2026 00:17:25 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a532bc4f7b1bfc017ca46aa52745b7a4491282216aac7d431486479978f69802`  
		Last Modified: Fri, 10 Apr 2026 00:17:26 GMT  
		Size: 501.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:754907f86ebfca9d043f6be78477d8824737bb089d535d25448952014fe513e6`  
		Last Modified: Fri, 10 Apr 2026 00:17:26 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70b31f6ad9f40567e3d1c45ba94ef71a6dd23231062c0edf06ff2f301511eb2f`  
		Last Modified: Fri, 10 Apr 2026 00:17:26 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:latest` - unknown; unknown

```console
$ docker pull yourls@sha256:b9cd46bc4737a3e264b370d0d2c95f825f71f67a6ca572f98ea715a13d1dddad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 KB (47663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62c727ef28bb79597ac2b6ae16867dcb1ef9db737a118a505027747b72dd2f73`

```dockerfile
```

-	Layers:
	-	`sha256:93533956c5d65cbf185954fd3eee043e2de8a6201be830d322a36f75a5e69953`  
		Last Modified: Fri, 10 Apr 2026 00:17:24 GMT  
		Size: 47.7 KB (47663 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:latest` - linux; riscv64

```console
$ docker pull yourls@sha256:91b2681b88a117fa0014faf2aa8e2c891be0386cc49de6cf9aa6699468f12952
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.5 MB (213496529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e1711d126663ce6b6cb7106c2ef8b7923a5792f9be2068ff257795f891b2d81`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 06:49:14 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 17 Mar 2026 06:51:16 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 17 Mar 2026 06:51:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 06:51:16 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 17 Mar 2026 06:51:17 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 17 Mar 2026 06:51:17 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 17 Mar 2026 06:51:17 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 17 Mar 2026 07:56:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 17 Mar 2026 07:56:14 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 17 Mar 2026 07:56:14 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 17 Mar 2026 07:56:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 17 Mar 2026 07:56:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 17 Mar 2026 07:56:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 17 Mar 2026 07:56:14 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Tue, 17 Mar 2026 07:56:14 GMT
ENV PHP_VERSION=8.5.4
# Tue, 17 Mar 2026 07:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.4.tar.xz.asc
# Tue, 17 Mar 2026 07:56:14 GMT
ENV PHP_SHA256=c1569f1f543f6b025c583cdc0e730e5c5833c603618613f1aa8e75d1524b8c91
# Tue, 17 Mar 2026 07:57:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 17 Mar 2026 07:57:19 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 08:53:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 17 Mar 2026 08:53:35 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 08:53:36 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 17 Mar 2026 08:53:36 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 17 Mar 2026 08:53:36 GMT
STOPSIGNAL SIGWINCH
# Tue, 17 Mar 2026 08:53:36 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 08:53:36 GMT
WORKDIR /var/www/html
# Tue, 17 Mar 2026 08:53:36 GMT
EXPOSE map[80/tcp:{}]
# Tue, 17 Mar 2026 08:53:36 GMT
CMD ["apache2-foreground"]
# Thu, 19 Mar 2026 05:06:41 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)"     bcmath     pdo_mysql     mysqli # buildkit
# Thu, 19 Mar 2026 05:06:41 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Thu, 19 Mar 2026 05:06:42 GMT
RUN a2enmod rewrite expires # buildkit
# Thu, 19 Mar 2026 05:06:45 GMT
ARG YOURLS_VERSION=1.10.3
# Thu, 19 Mar 2026 05:06:45 GMT
ARG YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
# Thu, 19 Mar 2026 05:06:45 GMT
ENV YOURLS_VERSION=1.10.3
# Thu, 19 Mar 2026 05:06:45 GMT
ENV YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
# Thu, 19 Mar 2026 05:06:45 GMT
# ARGS: YOURLS_VERSION=1.10.3 YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Thu, 19 Mar 2026 05:06:45 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Thu, 19 Mar 2026 05:06:45 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Mar 2026 05:06:46 GMT
COPY files/vhost.conf /etc/apache2/sites-available/000-default.conf # buildkit
# Thu, 19 Mar 2026 05:06:46 GMT
COPY files/vhost-https.conf /etc/apache2/sites-available/default-ssl.conf # buildkit
# Thu, 19 Mar 2026 05:06:46 GMT
COPY files/ports.conf /etc/apache2/ports.conf # buildkit
# Thu, 19 Mar 2026 05:06:46 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 19 Mar 2026 05:06:46 GMT
EXPOSE map[8443/tcp:{}]
# Thu, 19 Mar 2026 05:06:46 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Thu, 19 Mar 2026 05:06:46 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:0b5164900a4737bd8c71921f9d6095f2a9499d5081755c56a4aa46d8f37e9865`  
		Last Modified: Mon, 16 Mar 2026 22:10:41 GMT  
		Size: 28.3 MB (28275636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:052ed4f02aa31c663fadd7dcbdf7d48cff60f65277fca52fb6bc071ae3231c16`  
		Last Modified: Tue, 17 Mar 2026 07:54:10 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:162d9824bd9e3774ef91ecc16979a3f4b3a7fbeaa59ac22d99b7357247d2682f`  
		Last Modified: Tue, 17 Mar 2026 07:54:37 GMT  
		Size: 146.6 MB (146577811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18fb554c2db715df402d78477452cfa9b3584aef39b30723b2ef10d4426fa35b`  
		Last Modified: Tue, 17 Mar 2026 07:54:10 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76f12fc09529fe17ee50bb7b7c7dddad29d860b052519ad501c69557bdf9de64`  
		Last Modified: Tue, 17 Mar 2026 08:56:47 GMT  
		Size: 4.0 MB (4031214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b81af5a2dba9cbadede6c5ef9d497dd3628c5428646e32b3ffb77268532ec22`  
		Last Modified: Tue, 17 Mar 2026 08:56:46 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2acc95446d3d3d6fbaf3750592e294e1995ef308b8b6b6cc25ff89f374bdd686`  
		Last Modified: Tue, 17 Mar 2026 08:56:46 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0057c5ee6f3cdb5294a68d90b449a9fa818bf5223e42a2f136f5c81bdf0ee5c`  
		Last Modified: Tue, 17 Mar 2026 08:56:51 GMT  
		Size: 14.5 MB (14514591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ecf700cacb01888c300e0cfb0637c28428001cde555b96dd9ca56bd545de543`  
		Last Modified: Tue, 17 Mar 2026 08:56:48 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cce969b67fab793aa855500654f3087c449859445c60044383416b98d5acb24`  
		Last Modified: Tue, 17 Mar 2026 08:56:51 GMT  
		Size: 13.9 MB (13930422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:396984cfff954689d8093eb54b771bf1492bb2597d9251f17f65bc983e6b6402`  
		Last Modified: Tue, 17 Mar 2026 08:56:49 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2ee6075840c26146549ecfbd68fe8779c42895025381294783f508af987ef1b`  
		Last Modified: Tue, 17 Mar 2026 08:56:50 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2c58ed423789ba78d54a8a107d862260c0260f97e0741ee66dd42c1ed21abf8`  
		Last Modified: Tue, 17 Mar 2026 08:56:51 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bb84539adc0e5e14cbdb513cddc846c563a9093bd9e2ae1c51b7e9a2a1911fd`  
		Last Modified: Thu, 19 Mar 2026 05:07:36 GMT  
		Size: 106.6 KB (106571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20dc7b7b6931d94e68ba8241ff1fe0c058001487843b16b826c121414417552c`  
		Last Modified: Thu, 19 Mar 2026 05:07:36 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067bb2484245b04de1d75755635a7752d1eb26c5ce8dd9db99429fe8910e4434`  
		Last Modified: Thu, 19 Mar 2026 05:07:36 GMT  
		Size: 352.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7908c5f9994ad11ba6304821018bc4ed4bff2c0423063d624347454563400d3d`  
		Last Modified: Thu, 19 Mar 2026 05:07:37 GMT  
		Size: 6.0 MB (6048925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403f8647e03b6ae86a24bf59c5b93c12e56f5d81b3cb6bb805eaa215e9b65d35`  
		Last Modified: Thu, 19 Mar 2026 05:07:38 GMT  
		Size: 2.1 KB (2094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a2fe9c628814e17c50c48735b0a900b504c209678cd980b9e2aee68541255b`  
		Last Modified: Thu, 19 Mar 2026 05:07:38 GMT  
		Size: 1.7 KB (1694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b22689b9e23a2b6fb4cd15e0ffc2239eb899be0ebab64a0b39a2d6abb6bf054a`  
		Last Modified: Thu, 19 Mar 2026 05:07:38 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77aaa11fa72f54b96fc7ad38baca63e31c96299c219b7d060d75a4939e7de4da`  
		Last Modified: Thu, 19 Mar 2026 05:07:39 GMT  
		Size: 548.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:681b183260e23180b92cda9c7e7615fc25dc4a80ce8228be81ae773e27eece93`  
		Last Modified: Thu, 19 Mar 2026 05:07:39 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:latest` - unknown; unknown

```console
$ docker pull yourls@sha256:6c71167e7efa2dbb7490b76c612b19fa9eb4a7aad424ef77f9ab65aa39cd0b1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 KB (47663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b95bceacba535e25dff39e5a4788042189418abdcfce20068032ded5a8ee8e2`

```dockerfile
```

-	Layers:
	-	`sha256:a8f35460c230936198ffb3d7e8d0722884dd54190ea8f41e911d1d99c16401d7`  
		Last Modified: Thu, 19 Mar 2026 05:07:36 GMT  
		Size: 47.7 KB (47663 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:latest` - linux; s390x

```console
$ docker pull yourls@sha256:6d0aa703380d60f5d50fbf53372f8910060fd4ad3f9eb5f69aa6ae0874b0ce96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.8 MB (164802032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5093ae8d8957d54a24798edab7191eb8a0c87974ed3efefc3c5566f16a66a4b6`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:28:20 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 07 Apr 2026 01:28:47 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 07 Apr 2026 01:28:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 01:28:47 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 07 Apr 2026 01:28:48 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 07 Apr 2026 01:28:48 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 07 Apr 2026 01:28:48 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 07 Apr 2026 01:29:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 07 Apr 2026 01:29:01 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 07 Apr 2026 01:29:01 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 07 Apr 2026 01:29:01 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 07 Apr 2026 01:29:01 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 07 Apr 2026 01:29:01 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 07 Apr 2026 01:29:01 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Tue, 07 Apr 2026 01:29:01 GMT
ENV PHP_VERSION=8.5.5
# Tue, 07 Apr 2026 01:29:01 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.5.tar.xz.asc
# Tue, 07 Apr 2026 01:29:01 GMT
ENV PHP_SHA256=95bec382f4bd00570a8ef52a58ec04d8d9b9a90494781f1c106d1b274a3902f2
# Thu, 09 Apr 2026 22:11:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 09 Apr 2026 22:11:03 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 22:15:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 09 Apr 2026 22:15:44 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 22:15:44 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 09 Apr 2026 22:15:44 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 09 Apr 2026 22:15:44 GMT
STOPSIGNAL SIGWINCH
# Thu, 09 Apr 2026 22:15:44 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 22:15:44 GMT
WORKDIR /var/www/html
# Thu, 09 Apr 2026 22:15:44 GMT
EXPOSE map[80/tcp:{}]
# Thu, 09 Apr 2026 22:15:44 GMT
CMD ["apache2-foreground"]
# Thu, 09 Apr 2026 23:16:41 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)"     bcmath     pdo_mysql     mysqli # buildkit
# Thu, 09 Apr 2026 23:16:41 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Thu, 09 Apr 2026 23:16:41 GMT
RUN a2enmod rewrite expires # buildkit
# Thu, 09 Apr 2026 23:16:42 GMT
ARG YOURLS_VERSION=1.10.3
# Thu, 09 Apr 2026 23:16:42 GMT
ARG YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
# Thu, 09 Apr 2026 23:16:42 GMT
ENV YOURLS_VERSION=1.10.3
# Thu, 09 Apr 2026 23:16:42 GMT
ENV YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
# Thu, 09 Apr 2026 23:16:42 GMT
# ARGS: YOURLS_VERSION=1.10.3 YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Thu, 09 Apr 2026 23:16:42 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Thu, 09 Apr 2026 23:16:43 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 23:16:43 GMT
COPY files/vhost.conf /etc/apache2/sites-available/000-default.conf # buildkit
# Thu, 09 Apr 2026 23:16:43 GMT
COPY files/vhost-https.conf /etc/apache2/sites-available/default-ssl.conf # buildkit
# Thu, 09 Apr 2026 23:16:43 GMT
COPY files/ports.conf /etc/apache2/ports.conf # buildkit
# Thu, 09 Apr 2026 23:16:43 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 09 Apr 2026 23:16:43 GMT
EXPOSE map[8443/tcp:{}]
# Thu, 09 Apr 2026 23:16:43 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Thu, 09 Apr 2026 23:16:43 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:82e48a38ec87473a03164a244b5d8dfc2b55ef7a891305e41ee39d937de3c4a4`  
		Last Modified: Tue, 07 Apr 2026 00:13:47 GMT  
		Size: 29.8 MB (29835418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02a0ba9dd82d347df99933450adc7b4b5ebd450ecf06d8e33de4590c01baf6f2`  
		Last Modified: Tue, 07 Apr 2026 01:34:27 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60a2ecb81d69135694beb29b311f6564c601c6401fc3cfc01e848c637cd902c1`  
		Last Modified: Tue, 07 Apr 2026 01:34:29 GMT  
		Size: 92.6 MB (92573387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d9f4ead5e9fe90fedf7ab6cc72e260983245abfab9745bcaf8ac63573660bbe`  
		Last Modified: Tue, 07 Apr 2026 01:34:27 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d86b92cceade56e257b7a0c3b83c30180afbebb18d02d9326aa539f1432b4ae`  
		Last Modified: Tue, 07 Apr 2026 01:34:27 GMT  
		Size: 4.3 MB (4329556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58e0deda63bdf870ce31de2d7ef225061f1607e1d17d255e6c312982dfdf0038`  
		Last Modified: Tue, 07 Apr 2026 01:34:28 GMT  
		Size: 431.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7f8e217a79dfaa8369a757d0d5fb236f873bf2cc136b107c4094232fad4c071`  
		Last Modified: Tue, 07 Apr 2026 01:34:28 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c9096e4214af709c2ba5b0fdc06d705a03f4bd7f2748394da2e07df531d6be7`  
		Last Modified: Thu, 09 Apr 2026 22:16:02 GMT  
		Size: 14.5 MB (14536092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a8504db482271317d209338429055ef119f1401bc532738b0b52c3ae91bc0d0`  
		Last Modified: Thu, 09 Apr 2026 22:16:02 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bc80a37bc04d6cb037435118a0772becbc595ceccb15f8c13c6f3a6be9d488f`  
		Last Modified: Thu, 09 Apr 2026 22:16:02 GMT  
		Size: 17.4 MB (17355661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:438d8f74403265d22d4eb85f78302d4f825ee0b064cf30fb746d31102bc236c3`  
		Last Modified: Thu, 09 Apr 2026 22:16:02 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0678c06a9b3e095aeaae9fa4eff62d3fa578721e6812ca97ed8e7582a0bb652a`  
		Last Modified: Thu, 09 Apr 2026 22:16:03 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b9df0dc44779aa9de8705af16ed7df72fb2c95515bcad500b8cedc9440ebc82`  
		Last Modified: Thu, 09 Apr 2026 22:16:03 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa247af277fe4e74180ecc33ed9f69d0f42c695db1c58b53cd88aac92fe1115d`  
		Last Modified: Thu, 09 Apr 2026 23:16:52 GMT  
		Size: 111.7 KB (111677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeaeb5efa3eec9045f16f5b4313527ac09e9164f3e0c1d79076762aa5713b379`  
		Last Modified: Thu, 09 Apr 2026 23:16:51 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ada17e67a2b8190c5ac767c624624eb0b3cd81bc90a7318004c8577fed19786`  
		Last Modified: Thu, 09 Apr 2026 23:16:51 GMT  
		Size: 351.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b82d784bc0a760554978f3e0cdf9506a5d48ddd14c0275722e2db6a8c6c3f6f8`  
		Last Modified: Thu, 09 Apr 2026 23:16:52 GMT  
		Size: 6.0 MB (6048923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8cf4d8da79a35b9c18aae34f281d14c7b94ad424fe6bfa398623b916b87f370`  
		Last Modified: Thu, 09 Apr 2026 23:16:52 GMT  
		Size: 2.1 KB (2092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71f4bdf3596b53d18f7238b081d0a9f0e642475f959f74cb22c284a5d7f234b1`  
		Last Modified: Thu, 09 Apr 2026 23:16:53 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:658e4223c96f26e0a5d7fff5b25816093b1f696fee3439caba312a2df7f428b9`  
		Last Modified: Thu, 09 Apr 2026 23:16:53 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9c9d2e08c1dffd32c6cf52fdb0403e024a941eda5f723b36138c9a93f45795b`  
		Last Modified: Thu, 09 Apr 2026 23:16:53 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6af4cb4760e83267bfeffd9f407558aa3a3ce9d89d68c2f7dd4030f0b953f9ad`  
		Last Modified: Thu, 09 Apr 2026 23:16:53 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:latest` - unknown; unknown

```console
$ docker pull yourls@sha256:c610678043ca48f6553da0fb655cc19219b0c0c1d9883e1a30887b1836f5ee22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.6 KB (47579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62d16386b1b48df2ef504547039f4f6a632dc9aaca42f76506dee0e513dec27c`

```dockerfile
```

-	Layers:
	-	`sha256:87e3ad16ab253fbed10369f2696db0550c572a026b2a47d4cf3fbcebc2df494b`  
		Last Modified: Thu, 09 Apr 2026 23:16:51 GMT  
		Size: 47.6 KB (47579 bytes)  
		MIME: application/vnd.in-toto+json
