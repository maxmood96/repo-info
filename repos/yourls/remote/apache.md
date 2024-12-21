## `yourls:apache`

```console
$ docker pull yourls@sha256:4557ab63f448042086ead73aec65b7d8d3fde2828a149325894928bfe964297c
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

### `yourls:apache` - linux; amd64

```console
$ docker pull yourls@sha256:00b2104ec34fbe1d958ccc256a2d507b6fce8b6094545ea1905cdf97aab99954
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.4 MB (181414998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0337fff79d6277417aabd1f1cfd386f4edf3dc754b98a459dd13c0e59dbb837`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 18 Apr 2024 21:17:33 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 18 Apr 2024 21:17:33 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Apr 2024 21:17:33 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_VERSION=8.3.14
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.14.tar.xz.asc
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_SHA256=58b4cb9019bf70c0cbcdb814c7df79b9065059d14cf7dbf48d971f8e56ae9be7
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 18 Apr 2024 21:17:33 GMT
STOPSIGNAL SIGWINCH
# Thu, 18 Apr 2024 21:17:33 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
WORKDIR /var/www/html
# Thu, 18 Apr 2024 21:17:33 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Apr 2024 21:17:33 GMT
CMD ["apache2-foreground"]
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN a2enmod rewrite expires # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ARG YOURLS_VERSION=1.9.2
# Thu, 18 Apr 2024 21:17:33 GMT
ARG YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
# Thu, 18 Apr 2024 21:17:33 GMT
ENV YOURLS_VERSION=1.9.2
# Thu, 18 Apr 2024 21:17:33 GMT
ENV YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
# Thu, 18 Apr 2024 21:17:33 GMT
# ARGS: YOURLS_VERSION=1.9.2 YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY .htaccess /usr/src/yourls/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Thu, 18 Apr 2024 21:17:33 GMT
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
	-	`sha256:5d34002fff6b227b3fef60292cbe2dae076360dbebbffc071144d8deede2ce07`  
		Last Modified: Tue, 03 Dec 2024 03:17:37 GMT  
		Size: 527.0 KB (526950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89bf16b4e516967a6a435da5fcb3f5e8d3bdf3d6f4c930d3b110112eea8a144b`  
		Last Modified: Tue, 03 Dec 2024 03:17:37 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c403ba6cd6292cdafd4aa8f671b8ce7727358b83f67aff766bd425a416d7f04`  
		Last Modified: Tue, 03 Dec 2024 03:17:37 GMT  
		Size: 345.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcc878e6c6ded4596db74b568383bf9ca2c6cb6a991b772590d761e3229b49be`  
		Last Modified: Tue, 03 Dec 2024 03:17:37 GMT  
		Size: 4.1 MB (4073352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ab579d8c5e5ed3374490fd481c8b74f5722d1636654315c061c14d9af9fb8f8`  
		Last Modified: Tue, 03 Dec 2024 03:17:37 GMT  
		Size: 2.0 KB (2050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e98ff4635219dc750ce9fbb329367791d7e77d3bcee92157d7904c9d8e4d8b35`  
		Last Modified: Tue, 03 Dec 2024 03:17:37 GMT  
		Size: 1.7 KB (1694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f0590858e47dee54608d5207e473284211f0fb14a4ada2a83fa255bbec21688`  
		Last Modified: Tue, 03 Dec 2024 03:17:38 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:apache` - unknown; unknown

```console
$ docker pull yourls@sha256:b4d558a01e8218d5c117ebfecdb079958c34d3f3a1972a30a715b355fe187b40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.0 KB (38980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc7d0f33d484b1a0d4465cc0cfc153047b743b03eb071c9cbbd2e9a58776c1b0`

```dockerfile
```

-	Layers:
	-	`sha256:6176b7cc49037386f77d61b33fa01c92a56fd5b4dffd308393851768fabcd572`  
		Last Modified: Tue, 03 Dec 2024 03:17:36 GMT  
		Size: 39.0 KB (38980 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:apache` - linux; arm variant v5

```console
$ docker pull yourls@sha256:eeeba385b159834bdc4bf6d0b143f7a27eb513c317bcfd6e27715fb8e9f7e465
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.5 MB (154484882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e24979875e124874fd3a57e7995502e0d40d9d8be20fb9cfd720404a0bae478f`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 18 Apr 2024 21:17:33 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1733097600'
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 18 Apr 2024 21:17:33 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Apr 2024 21:17:33 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_VERSION=8.3.15
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.15.tar.xz.asc
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_SHA256=3df5d45637283f759eef8fc3ce03de829ded3e200c3da278936a684955d2f94f
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 18 Apr 2024 21:17:33 GMT
STOPSIGNAL SIGWINCH
# Thu, 18 Apr 2024 21:17:33 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
WORKDIR /var/www/html
# Thu, 18 Apr 2024 21:17:33 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Apr 2024 21:17:33 GMT
CMD ["apache2-foreground"]
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN a2enmod rewrite expires # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ARG YOURLS_VERSION=1.9.2
# Thu, 18 Apr 2024 21:17:33 GMT
ARG YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
# Thu, 18 Apr 2024 21:17:33 GMT
ENV YOURLS_VERSION=1.9.2
# Thu, 18 Apr 2024 21:17:33 GMT
ENV YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
# Thu, 18 Apr 2024 21:17:33 GMT
# ARGS: YOURLS_VERSION=1.9.2 YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY .htaccess /usr/src/yourls/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Thu, 18 Apr 2024 21:17:33 GMT
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
	-	`sha256:ee69b59c25d9ef7160325ada4814f43f750ef00d5508783fab3c795a53d0fd57`  
		Last Modified: Fri, 20 Dec 2024 22:05:27 GMT  
		Size: 12.7 MB (12651271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7767fbd56dd24df4ccaa1e48a9c5c0137100fe729e877184aaf4533c438f31ec`  
		Last Modified: Fri, 20 Dec 2024 22:05:26 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eba568b5c12606915df49b23d06c1665e3ce4aaf7124a032f9deab725112a7dc`  
		Last Modified: Fri, 20 Dec 2024 22:05:27 GMT  
		Size: 10.6 MB (10622545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ae36a267958e17a9f4fa59bc3c359192d77bfa8a5c7cb7696c88bbee738cd26`  
		Last Modified: Fri, 20 Dec 2024 22:05:26 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c18711fd5aa09b7a507242330c5164ae3deb0aef9a1453e2e46b79c0064cf50c`  
		Last Modified: Fri, 20 Dec 2024 22:05:27 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8043e02ca03422d26cb58b890861be8cff1ee0b97caa2f0dd58a88a8427edd91`  
		Last Modified: Fri, 20 Dec 2024 22:05:27 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:341bc819c5d6f214c37a5baa358e881586ea5f0641df5c5e455879612a0ee34a`  
		Last Modified: Fri, 20 Dec 2024 22:50:05 GMT  
		Size: 154.3 KB (154328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:399f697d2c461346d418e5fead5981212766669a975cf9ac88d60ab2ad4c70cb`  
		Last Modified: Fri, 20 Dec 2024 22:50:05 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d83edda8df3cdbfcf1d0e97f7fe62e2cecacadebb97424ab570cd5a2dbb709`  
		Last Modified: Fri, 20 Dec 2024 22:50:05 GMT  
		Size: 353.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f69c2e985cf200784b5bf8f6ea5d9ce4ef8b55422bf98a297c136d86a12282af`  
		Last Modified: Fri, 20 Dec 2024 22:50:06 GMT  
		Size: 4.1 MB (4073358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc201b3fde51873d09b95e7e1887ce1c1b931b9acf6f8ce6a87c04f49576fef`  
		Last Modified: Fri, 20 Dec 2024 22:50:06 GMT  
		Size: 2.1 KB (2052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20410f7a550f575ec1319b8f6b252ca9e83fe2223b6dc1ec9ee7116af0ed63d1`  
		Last Modified: Fri, 20 Dec 2024 22:50:06 GMT  
		Size: 1.7 KB (1694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f26f4922b4df85a94f4485481a9c5a253138849fc8c99578f6f75428c62971f9`  
		Last Modified: Fri, 20 Dec 2024 22:50:07 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:apache` - unknown; unknown

```console
$ docker pull yourls@sha256:26d9cde92fc16d73853d801406b9abd84c81fab9e081d9f87beac10d3b51d474
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.1 KB (39119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:641429cdf4bb15f368d2b80559ee5d48979d555ac24c80b69f9b4d10397b1c06`

```dockerfile
```

-	Layers:
	-	`sha256:da62089762e94deebffd6a91d9b8f7f7c60e3071e40e285f3456f65a051f284c`  
		Last Modified: Fri, 20 Dec 2024 22:50:05 GMT  
		Size: 39.1 KB (39119 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:apache` - linux; arm variant v7

```console
$ docker pull yourls@sha256:edfbf0b65a551c63d705107fee0850b17185aa638ee46882bad0d31738218693
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.7 MB (145671341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4a93b3ba1f96ce22ee8708f49f5b70d553e5b9fa4664fd63c4ed74ea05968b4`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 18 Apr 2024 21:17:33 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1733097600'
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 18 Apr 2024 21:17:33 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Apr 2024 21:17:33 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_VERSION=8.3.14
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.14.tar.xz.asc
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_SHA256=58b4cb9019bf70c0cbcdb814c7df79b9065059d14cf7dbf48d971f8e56ae9be7
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 18 Apr 2024 21:17:33 GMT
STOPSIGNAL SIGWINCH
# Thu, 18 Apr 2024 21:17:33 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
WORKDIR /var/www/html
# Thu, 18 Apr 2024 21:17:33 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Apr 2024 21:17:33 GMT
CMD ["apache2-foreground"]
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN a2enmod rewrite expires # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ARG YOURLS_VERSION=1.9.2
# Thu, 18 Apr 2024 21:17:33 GMT
ARG YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
# Thu, 18 Apr 2024 21:17:33 GMT
ENV YOURLS_VERSION=1.9.2
# Thu, 18 Apr 2024 21:17:33 GMT
ENV YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
# Thu, 18 Apr 2024 21:17:33 GMT
# ARGS: YOURLS_VERSION=1.9.2 YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY .htaccess /usr/src/yourls/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Thu, 18 Apr 2024 21:17:33 GMT
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
	-	`sha256:b93206b2a1002e4f1ea0bd42813f632942dd082a42a55a6d9674788ca2b201d5`  
		Last Modified: Tue, 03 Dec 2024 17:14:29 GMT  
		Size: 141.6 KB (141617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:937a8bec8ce92a63b890498dcd2a6de9b34aa252fe82b3b94a73cb758a9dae8e`  
		Last Modified: Tue, 03 Dec 2024 17:14:29 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2e0ce9a63e3ec84424982939897922ca33e8b7bd62cde46d0b97a780eb44888`  
		Last Modified: Tue, 03 Dec 2024 17:14:29 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feefd8a5e2d73d0487e936ca28c6fdeb95ddf4c74c3b117a2074df5ef021f3c3`  
		Last Modified: Tue, 03 Dec 2024 17:14:30 GMT  
		Size: 4.1 MB (4073352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0387cef9d8076e1e6bef6daef2f3996cd02d09f5d16916e820bebaf520e8ecdb`  
		Last Modified: Tue, 03 Dec 2024 17:14:30 GMT  
		Size: 2.0 KB (2049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f36dcbb89151fcbbe8a6dc2d9edd8d470f90b34a6c59e68d2e913ffb4762c1`  
		Last Modified: Tue, 03 Dec 2024 17:14:30 GMT  
		Size: 1.7 KB (1693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5abd1603f2270db3d9ef7fbe789ac51eb41a198391cf5afd7f518d17e8caac6`  
		Last Modified: Tue, 03 Dec 2024 17:14:30 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:apache` - unknown; unknown

```console
$ docker pull yourls@sha256:ab7d97091daa95f2d4460f29dea56cbc53e9826a82a2c9b6e9e3a6003956b509
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.1 KB (39119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d15fc95e9bf1a35a0965a04dd91f7e1720554273badd6849127dd24a22f305b`

```dockerfile
```

-	Layers:
	-	`sha256:02f59c44556f2e43d28257781957b8fb2d2810b009a3315427e34cfd8f3c4109`  
		Last Modified: Tue, 03 Dec 2024 17:14:29 GMT  
		Size: 39.1 KB (39119 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:apache` - linux; arm64 variant v8

```console
$ docker pull yourls@sha256:3f671f3a81a56cc5b8a989122c964d99eed62ac216f23c61f46f6fb41efbc14d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.3 MB (175282471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e52faa5ec8be174a70e21a495fe51b887a2e8c85ae24a4a3e9ce90dd9cc9020`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 18 Apr 2024 21:17:33 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 18 Apr 2024 21:17:33 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Apr 2024 21:17:33 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_VERSION=8.3.14
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.14.tar.xz.asc
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_SHA256=58b4cb9019bf70c0cbcdb814c7df79b9065059d14cf7dbf48d971f8e56ae9be7
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 18 Apr 2024 21:17:33 GMT
STOPSIGNAL SIGWINCH
# Thu, 18 Apr 2024 21:17:33 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
WORKDIR /var/www/html
# Thu, 18 Apr 2024 21:17:33 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Apr 2024 21:17:33 GMT
CMD ["apache2-foreground"]
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN a2enmod rewrite expires # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ARG YOURLS_VERSION=1.9.2
# Thu, 18 Apr 2024 21:17:33 GMT
ARG YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
# Thu, 18 Apr 2024 21:17:33 GMT
ENV YOURLS_VERSION=1.9.2
# Thu, 18 Apr 2024 21:17:33 GMT
ENV YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
# Thu, 18 Apr 2024 21:17:33 GMT
# ARGS: YOURLS_VERSION=1.9.2 YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY .htaccess /usr/src/yourls/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Thu, 18 Apr 2024 21:17:33 GMT
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
	-	`sha256:5cebe73832253b14f27f1abfe82ea47d2df50e50a7f7ea61121ebb7e4ca36e36`  
		Last Modified: Tue, 03 Dec 2024 11:45:56 GMT  
		Size: 794.3 KB (794341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca6aa92185859f23c93f6049358a25ff01b073f2ccb2a2b70e58e866344d7ca7`  
		Last Modified: Tue, 03 Dec 2024 11:45:56 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66e7f6450a6cdbbfe18b1120d51e259146cc014050f2ebf0fe8b83032bef7e05`  
		Last Modified: Tue, 03 Dec 2024 11:45:56 GMT  
		Size: 347.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:205d92a41964037c2b47a0515becf7d87a4dfbc9223ce88f1482bf7e9be144b4`  
		Last Modified: Tue, 03 Dec 2024 11:45:56 GMT  
		Size: 4.1 MB (4073351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0af576c7129392c1c5879d060cd6013e6d8ab0f332131610403d1aceffe6a0a5`  
		Last Modified: Tue, 03 Dec 2024 11:45:56 GMT  
		Size: 2.0 KB (2050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c230488e3e45890ec0a61cfa007c8b9373a4d9fa8dc25d2487d713e009630a7`  
		Last Modified: Tue, 03 Dec 2024 11:45:57 GMT  
		Size: 1.7 KB (1694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7306dc6c7e46ea127423400dfeb7be26668591c41ebfaee11d724a319e0bc4c9`  
		Last Modified: Tue, 03 Dec 2024 11:45:57 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:apache` - unknown; unknown

```console
$ docker pull yourls@sha256:03aa942d7b96547c4dfca5822108351e9fd15f334eebc65bff3e14f0ec64f384
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.2 KB (39169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e72fecac530851e18c0d71513d86ae730ecc7e31becddcc59029fd7ecb3b16f6`

```dockerfile
```

-	Layers:
	-	`sha256:a3d1019eda13eeb97834b44ab942a5fa5b9bdc9face4066b6f0d8ad94aaaa1db`  
		Last Modified: Tue, 03 Dec 2024 11:45:55 GMT  
		Size: 39.2 KB (39169 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:apache` - linux; 386

```console
$ docker pull yourls@sha256:f1b80bebcf8e2bcd7bd14feab20bc66b5a9c55653427f72986f1cedd7e2b2570
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.3 MB (180276081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e92f991441e561e025a0e5591993ee1bbc7f3785900bff23f3a9cd1cd1f25c37`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 18 Apr 2024 21:17:33 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1733097600'
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 18 Apr 2024 21:17:33 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Apr 2024 21:17:33 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_VERSION=8.3.15
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.15.tar.xz.asc
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_SHA256=3df5d45637283f759eef8fc3ce03de829ded3e200c3da278936a684955d2f94f
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 18 Apr 2024 21:17:33 GMT
STOPSIGNAL SIGWINCH
# Thu, 18 Apr 2024 21:17:33 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
WORKDIR /var/www/html
# Thu, 18 Apr 2024 21:17:33 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Apr 2024 21:17:33 GMT
CMD ["apache2-foreground"]
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN a2enmod rewrite expires # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ARG YOURLS_VERSION=1.9.2
# Thu, 18 Apr 2024 21:17:33 GMT
ARG YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
# Thu, 18 Apr 2024 21:17:33 GMT
ENV YOURLS_VERSION=1.9.2
# Thu, 18 Apr 2024 21:17:33 GMT
ENV YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
# Thu, 18 Apr 2024 21:17:33 GMT
# ARGS: YOURLS_VERSION=1.9.2 YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY .htaccess /usr/src/yourls/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Thu, 18 Apr 2024 21:17:33 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:ae6c80ee852fcccae85579165042a3767dcd1190112e87c9f22fa3e76a624c73`  
		Last Modified: Tue, 03 Dec 2024 01:27:10 GMT  
		Size: 29.2 MB (29205487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6d82e9ea3fa65bf8333714b3d9c338b367699c802196732ef90d4b64e367ccd`  
		Last Modified: Fri, 20 Dec 2024 21:35:20 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f933ca6170dab526f92787b71b4cc43a28e8d5c3c311d20f4e4d684bbca19eeb`  
		Last Modified: Fri, 20 Dec 2024 21:35:23 GMT  
		Size: 101.3 MB (101320480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17692ccafa790be39d41cbc7135bc3a12b7671591daae236723e6a09ef3fd653`  
		Last Modified: Fri, 20 Dec 2024 21:34:56 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06f100f1e2887b097466868797db13955baac0d02e598190d74331d22e37283a`  
		Last Modified: Fri, 20 Dec 2024 21:35:20 GMT  
		Size: 20.6 MB (20638499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0495f17ccfc59f1d154dd1c3b597b9a9ac7635b9a7ec6542c443a3b1afb0772`  
		Last Modified: Fri, 20 Dec 2024 21:35:20 GMT  
		Size: 427.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df46ff5a1d55ca593381da11c45faba4564ec005c038a08577943720d8e81c25`  
		Last Modified: Fri, 20 Dec 2024 21:35:20 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6828a771d5d34b23d22124744bfb7be424fa90b4661985fccfcaa432d644fb98`  
		Last Modified: Fri, 20 Dec 2024 21:35:21 GMT  
		Size: 12.7 MB (12652223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d986177f32841f6258ae750064b7cd61549b7864d9f7eb9a191d431dab097a5`  
		Last Modified: Fri, 20 Dec 2024 21:35:21 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54d813f5cee583f5bcdc04c8fa096b928927d232d0c790a7288925b2146330bf`  
		Last Modified: Fri, 20 Dec 2024 21:35:22 GMT  
		Size: 11.9 MB (11868857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6709d5f84b506fdf80cbfc0fcb4ca9bdfb0eb531a7607d788be039facf6b3df`  
		Last Modified: Fri, 20 Dec 2024 21:35:22 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf164e001273c28776d5c4a28151bd616e7d8fab75e3faed7cf28103057ad4d9`  
		Last Modified: Fri, 20 Dec 2024 21:35:22 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:948e948ad837c72ab523d810a161d6f4d9caad65038ac92524b844226a9ff54b`  
		Last Modified: Fri, 20 Dec 2024 21:35:22 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2faba772fb8b7c3616166dc528bb84b73b77680166a313bd150e005f464cc660`  
		Last Modified: Fri, 20 Dec 2024 22:30:50 GMT  
		Size: 507.0 KB (506954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb6520b8c146629a3ac1caa85cb0fda59fb695e5f6eace08b058d2ab83cbe3d5`  
		Last Modified: Fri, 20 Dec 2024 22:30:50 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2391fbab168d4fc1b1b441da8071862c075af2a5d32b9f40f90c02f42e95cd17`  
		Last Modified: Fri, 20 Dec 2024 22:30:50 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a0c538cec4774275cc504ad8aaf01474ad56a7ab08e24bf176100c8213c8cbb`  
		Last Modified: Fri, 20 Dec 2024 22:30:50 GMT  
		Size: 4.1 MB (4073358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5defcb940850fe0666a44c6be0c5e8b5a291adc1703b4a462bc49ea687cdcbe`  
		Last Modified: Fri, 20 Dec 2024 22:30:50 GMT  
		Size: 2.1 KB (2055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a12f33390d88e33636be49d741c567f195bd240edff84ddfda6bb10f521781c`  
		Last Modified: Fri, 20 Dec 2024 22:30:50 GMT  
		Size: 1.7 KB (1694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93999550a05c70c51dc0577c4157846616336e6b2fd37724a87366de7b37e188`  
		Last Modified: Fri, 20 Dec 2024 22:30:51 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:apache` - unknown; unknown

```console
$ docker pull yourls@sha256:0e56eb6d836ecef5e224d3801784beedb71ea5093edf563104fe46f4b6c93b6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 KB (38922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fefec9eb4591634b4c10aa1297ad2a7c7324b67b2bbc09770aad0bafe8b46b43`

```dockerfile
```

-	Layers:
	-	`sha256:08e279dd76534cfd91c7cf15fba9f42c91d0869240536edaaa22df9fe2a16165`  
		Last Modified: Fri, 20 Dec 2024 22:30:49 GMT  
		Size: 38.9 KB (38922 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:apache` - linux; mips64le

```console
$ docker pull yourls@sha256:0cae2d7cb204d029a30ecc9fd72260a49ca91f0d19d375f1260e2f15539a3258
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.7 MB (156656365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:905c819f4276a07fb10e46f5201d5902c6887605363fb005ce40993641b4b41b`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 18 Apr 2024 21:17:33 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1733097600'
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 18 Apr 2024 21:17:33 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Apr 2024 21:17:33 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_VERSION=8.3.14
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.14.tar.xz.asc
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_SHA256=58b4cb9019bf70c0cbcdb814c7df79b9065059d14cf7dbf48d971f8e56ae9be7
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 18 Apr 2024 21:17:33 GMT
STOPSIGNAL SIGWINCH
# Thu, 18 Apr 2024 21:17:33 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
WORKDIR /var/www/html
# Thu, 18 Apr 2024 21:17:33 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Apr 2024 21:17:33 GMT
CMD ["apache2-foreground"]
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN a2enmod rewrite expires # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ARG YOURLS_VERSION=1.9.2
# Thu, 18 Apr 2024 21:17:33 GMT
ARG YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
# Thu, 18 Apr 2024 21:17:33 GMT
ENV YOURLS_VERSION=1.9.2
# Thu, 18 Apr 2024 21:17:33 GMT
ENV YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
# Thu, 18 Apr 2024 21:17:33 GMT
# ARGS: YOURLS_VERSION=1.9.2 YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY .htaccess /usr/src/yourls/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Thu, 18 Apr 2024 21:17:33 GMT
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
	-	`sha256:3a103a16847df4b1eff5aeb8a62a7592103f9345f1ab5003e5b64254d51fdee0`  
		Last Modified: Tue, 03 Dec 2024 23:17:20 GMT  
		Size: 153.0 KB (152983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6aa88130235dcaeaf30e0a61bbbfd055c120a2a1dea13f93d467cc8f16026a7`  
		Last Modified: Tue, 03 Dec 2024 23:17:20 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc30a9fd9ae623acc2ec5612de92e1e5771fb7999ec83d7b02d712152ef8838d`  
		Last Modified: Tue, 03 Dec 2024 23:17:20 GMT  
		Size: 350.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d16c0ac8689d7d6e596842ffc62c4fb9f4f9671aac0d97d58d0be40a7941816c`  
		Last Modified: Tue, 03 Dec 2024 23:17:21 GMT  
		Size: 4.1 MB (4073352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83d0854ae2b23df1585c2500294989905c15b13ec90e2741d76dbb3bfee80ddb`  
		Last Modified: Tue, 03 Dec 2024 23:17:21 GMT  
		Size: 2.1 KB (2054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f94d194dfcfd4c087be4c07dad0a43cf716a0957d352a772958de0d55d1710fe`  
		Last Modified: Tue, 03 Dec 2024 23:17:21 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74a6eb4f11fb53a94163f3d27a0e3ade7c4dc10a05a86e388f4b3104c03687a1`  
		Last Modified: Tue, 03 Dec 2024 23:17:21 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:apache` - unknown; unknown

```console
$ docker pull yourls@sha256:8ed5911bb3f67dfa4b529bc1fdd6c0afdf44980f2224da467765d61de22a6da5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.1 KB (39083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a13a7647eb3b6dbc5121c6ad4c1154b042dac9a57643c63b2c6038d9443688e`

```dockerfile
```

-	Layers:
	-	`sha256:1025b6d12ba7695fc7055778af107ade2193b79424be8eee434455b39c0a83ac`  
		Last Modified: Tue, 03 Dec 2024 23:17:19 GMT  
		Size: 39.1 KB (39083 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:apache` - linux; ppc64le

```console
$ docker pull yourls@sha256:1d824cb8812ef0db8979fe7d22022e9949a77010483dd7d8a8edeef6f9cfbec1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.5 MB (185484584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fed2919226273973df4de04d0f62844fc6368c993423b2688c798944fd6a75e4`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 18 Apr 2024 21:17:33 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1733097600'
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 18 Apr 2024 21:17:33 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Apr 2024 21:17:33 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_VERSION=8.3.14
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.14.tar.xz.asc
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_SHA256=58b4cb9019bf70c0cbcdb814c7df79b9065059d14cf7dbf48d971f8e56ae9be7
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 18 Apr 2024 21:17:33 GMT
STOPSIGNAL SIGWINCH
# Thu, 18 Apr 2024 21:17:33 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
WORKDIR /var/www/html
# Thu, 18 Apr 2024 21:17:33 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Apr 2024 21:17:33 GMT
CMD ["apache2-foreground"]
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN a2enmod rewrite expires # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ARG YOURLS_VERSION=1.9.2
# Thu, 18 Apr 2024 21:17:33 GMT
ARG YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
# Thu, 18 Apr 2024 21:17:33 GMT
ENV YOURLS_VERSION=1.9.2
# Thu, 18 Apr 2024 21:17:33 GMT
ENV YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
# Thu, 18 Apr 2024 21:17:33 GMT
# ARGS: YOURLS_VERSION=1.9.2 YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY .htaccess /usr/src/yourls/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Thu, 18 Apr 2024 21:17:33 GMT
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
	-	`sha256:f5c06061527121add5cb306fa4d145f2fb00f6b295c7da084864893efc8e04ad`  
		Last Modified: Tue, 03 Dec 2024 09:39:33 GMT  
		Size: 188.6 KB (188647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd0c7d054c0edbd985a519e052701ad7c43cbd0abe2cce4a3cde3ae6fd60ca50`  
		Last Modified: Tue, 03 Dec 2024 09:39:32 GMT  
		Size: 323.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:673001dd488fff00dec6cce5a3ad2a6d13531f4eb44a4e1b31da7af1e892113f`  
		Last Modified: Tue, 03 Dec 2024 09:39:32 GMT  
		Size: 344.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf44c4170a6e134e321ec8fbc89f2a4cfd6011cd0874233c661f02e5048209df`  
		Last Modified: Tue, 03 Dec 2024 09:39:33 GMT  
		Size: 4.1 MB (4073351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d2522fbe355872cc0b0aaa033063282a3da435b1cd2e5c5077e3ba082f97a5f`  
		Last Modified: Tue, 03 Dec 2024 09:39:33 GMT  
		Size: 2.1 KB (2053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9af25c55c5759672ea19299f46f7621c4f02d94c5122582fbfa0571c85021b87`  
		Last Modified: Tue, 03 Dec 2024 09:39:33 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb554860a1b758d24f96be2080d136c62af47553073ceb9b47fa2780cf51004`  
		Last Modified: Tue, 03 Dec 2024 09:39:33 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:apache` - unknown; unknown

```console
$ docker pull yourls@sha256:0148032333946fb7a18644aaf1ff02875daa25c797728cf88f074d4666e5e7eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.1 KB (39054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:216d81307af349ad5bb9c67764f5eddbbb3621afe0728149dd53c58612483635`

```dockerfile
```

-	Layers:
	-	`sha256:0d413ee21bbc328ddb43b6f8c130c64c3dca0b6c8d002b08d44373ecd59e3590`  
		Last Modified: Tue, 03 Dec 2024 09:39:32 GMT  
		Size: 39.1 KB (39054 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:apache` - linux; s390x

```console
$ docker pull yourls@sha256:ed07c4d915480393781bf39ae70954b1907ca4b1401ec44d954bf4af1c87578e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.2 MB (155158249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5875cf1cfdcb2ca804df7071cdfba97e97214c6588c85cf6081a560d5d1d38b4`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 18 Apr 2024 21:17:33 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1733097600'
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 18 Apr 2024 21:17:33 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Apr 2024 21:17:33 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_VERSION=8.3.14
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.14.tar.xz.asc
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_SHA256=58b4cb9019bf70c0cbcdb814c7df79b9065059d14cf7dbf48d971f8e56ae9be7
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 18 Apr 2024 21:17:33 GMT
STOPSIGNAL SIGWINCH
# Thu, 18 Apr 2024 21:17:33 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
WORKDIR /var/www/html
# Thu, 18 Apr 2024 21:17:33 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Apr 2024 21:17:33 GMT
CMD ["apache2-foreground"]
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN a2enmod rewrite expires # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ARG YOURLS_VERSION=1.9.2
# Thu, 18 Apr 2024 21:17:33 GMT
ARG YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
# Thu, 18 Apr 2024 21:17:33 GMT
ENV YOURLS_VERSION=1.9.2
# Thu, 18 Apr 2024 21:17:33 GMT
ENV YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
# Thu, 18 Apr 2024 21:17:33 GMT
# ARGS: YOURLS_VERSION=1.9.2 YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY .htaccess /usr/src/yourls/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Thu, 18 Apr 2024 21:17:33 GMT
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
	-	`sha256:6beb2c8b8b6fb0ee145a488677b3abbdf2adb9a072490eab10d3bb8296c3a213`  
		Last Modified: Tue, 03 Dec 2024 07:51:46 GMT  
		Size: 161.9 KB (161950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:752fb9e6175235873ad65ac9c720fd508591a2e1e4f8c10950a53f43d5a14668`  
		Last Modified: Tue, 03 Dec 2024 07:51:46 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:784499cb49957c51a8f8f7125d29312511e1afe757fd818f9ce88fffc262e90c`  
		Last Modified: Tue, 03 Dec 2024 07:51:46 GMT  
		Size: 345.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9171ee0c8009394f008f8a1fe8e9885faa3dd107b0baee8e96ecaab02e1818f`  
		Last Modified: Tue, 03 Dec 2024 07:51:46 GMT  
		Size: 4.1 MB (4073352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c2c159b6fd82d2c516d391556f4fbe4c37fbeb3c36c2f14f00f2788f05e4f1e`  
		Last Modified: Tue, 03 Dec 2024 07:51:46 GMT  
		Size: 2.1 KB (2051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adb7d5292ff2d8146c7e79d9bf97c53b579f9f2940b2661b968810b167cfd457`  
		Last Modified: Tue, 03 Dec 2024 07:51:47 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5f13e3abfe35ea51d455030c718311be7e3607fc870da53363babd5be57ab98`  
		Last Modified: Tue, 03 Dec 2024 07:51:47 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:apache` - unknown; unknown

```console
$ docker pull yourls@sha256:df7353c6fa88f3602177a2c1a0e20996e8c1195dc313ddf4b9562631f3d4fdfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.0 KB (38972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06a16ea6953fc9204ad29d8accf5f9a28b3ed17740a1d24e3bf265206a5948aa`

```dockerfile
```

-	Layers:
	-	`sha256:f30e3e201a3aeee3c74e251102977a683db00910e8d2141bb5ba774a54f85105`  
		Last Modified: Tue, 03 Dec 2024 07:51:45 GMT  
		Size: 39.0 KB (38972 bytes)  
		MIME: application/vnd.in-toto+json
