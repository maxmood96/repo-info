## `mediawiki:stable`

```console
$ docker pull mediawiki@sha256:4ecdc3ab36cac14cf392c3653f5524a76b289503f194640fbf511576b9dd0d63
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
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

### `mediawiki:stable` - linux; amd64

```console
$ docker pull mediawiki@sha256:b58fd0ddb08ddbca4b620a3c25bf2ecf1df615cdb4469785b39de487c6ca8bfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.4 MB (326352883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfebd5aa2a034df31d2e4273c77e46dfc0bc85e61073dfcd2eeb53e7598b1e41`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 30 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Wed, 02 Jul 2025 21:52:08 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 02 Jul 2025 21:52:08 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 02 Jul 2025 21:52:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Jul 2025 21:52:08 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 02 Jul 2025 21:52:08 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 02 Jul 2025 21:52:08 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 02 Jul 2025 21:52:08 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 02 Jul 2025 21:52:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 02 Jul 2025 21:52:08 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 02 Jul 2025 21:52:08 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 02 Jul 2025 21:52:08 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 02 Jul 2025 21:52:08 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 02 Jul 2025 21:52:08 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 02 Jul 2025 21:52:08 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 02 Jul 2025 21:52:08 GMT
ENV PHP_VERSION=8.1.33
# Wed, 02 Jul 2025 21:52:08 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.33.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.33.tar.xz.asc
# Wed, 02 Jul 2025 21:52:08 GMT
ENV PHP_SHA256=9db83bf4590375562bc1a10b353cccbcf9fcfc56c58b7c8fb814e6865bb928d1
# Wed, 02 Jul 2025 21:52:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 02 Jul 2025 21:52:08 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 02 Jul 2025 21:52:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 02 Jul 2025 21:52:08 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 02 Jul 2025 21:52:08 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 02 Jul 2025 21:52:08 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 02 Jul 2025 21:52:08 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 02 Jul 2025 21:52:08 GMT
STOPSIGNAL SIGWINCH
# Wed, 02 Jul 2025 21:52:08 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 02 Jul 2025 21:52:08 GMT
WORKDIR /var/www/html
# Wed, 02 Jul 2025 21:52:08 GMT
EXPOSE map[80/tcp:{}]
# Wed, 02 Jul 2025 21:52:08 GMT
CMD ["apache2-foreground"]
# Wed, 02 Jul 2025 21:52:08 GMT
RUN set -eux; 		apt-get update; 	apt-get install -y --no-install-recommends 		git 		librsvg2-bin 		imagemagick 		python3 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Jul 2025 21:52:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libicu-dev 		libonig-dev 		liblua5.1-0-dev 	; 		docker-php-ext-install -j "$(nproc)" 		calendar 		intl 		mbstring 		mysqli 		opcache 	; 		pecl install APCu-5.1.24; 	pecl install LuaSandbox-4.1.2; 	docker-php-ext-enable 		apcu 		luasandbox 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Jul 2025 21:52:08 GMT
RUN set -eux; 	a2enmod rewrite; 	{ 		echo "<Directory /var/www/html>"; 		echo "  RewriteEngine On"; 		echo "  RewriteCond %{REQUEST_FILENAME} !-f"; 		echo "  RewriteCond %{REQUEST_FILENAME} !-d"; 		echo "  RewriteRule ^ %{DOCUMENT_ROOT}/index.php [L]"; 		echo "</Directory>"; 	} > "$APACHE_CONFDIR/conf-available/short-url.conf"; 	a2enconf short-url # buildkit
# Wed, 02 Jul 2025 21:52:08 GMT
RUN sed -i "s/<\/VirtualHost>/\tAllowEncodedSlashes NoDecode\n<\/VirtualHost>/" "$APACHE_CONFDIR/sites-available/000-default.conf" # buildkit
# Wed, 02 Jul 2025 21:52:08 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 02 Jul 2025 21:52:08 GMT
RUN set -eux; 	mkdir -p /var/www/data; 	chown -R www-data:www-data /var/www/data # buildkit
# Wed, 02 Jul 2025 21:52:08 GMT
ENV MEDIAWIKI_MAJOR_VERSION=1.44
# Wed, 02 Jul 2025 21:52:08 GMT
ENV MEDIAWIKI_VERSION=1.44.0
# Wed, 02 Jul 2025 21:52:08 GMT
RUN set -eux; 	fetchDeps=" 		gnupg 		dirmngr 	"; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 		curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz" -o mediawiki.tar.gz; 	curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz.sig" -o mediawiki.tar.gz.sig; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 		D7D6767D135A514BEB86E9BA75682B08E8A3FEC4 		441276E9CCD15F44F6D97D18C119E1A64D70938E 		F7F780D82EBFB8A56556E7EE82403E59F9F8CD79 		1D98867E82982C8FE0ABC25F9B69B3109D3BB7B0 		E059C034E7A430583C252F4AA8F734246D73B586 	; 	gpg --batch --verify mediawiki.tar.gz.sig mediawiki.tar.gz; 	tar -x --strip-components=1 -f mediawiki.tar.gz; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" mediawiki.tar.gz.sig mediawiki.tar.gz; 	chown -R www-data:www-data extensions skins cache images; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Jul 2025 21:52:08 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:3da95a905ed546f99c4564407923a681757d89651a388ec3f1f5e9bf5ed0b39d`  
		Last Modified: Tue, 01 Jul 2025 01:14:43 GMT  
		Size: 28.2 MB (28230143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd80672d6b45bd21268b018ee45930631ab31aaf2e3aba6665c7e262b98a014`  
		Last Modified: Thu, 03 Jul 2025 23:09:29 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f90d7cb2cbae0842ba415bc0a183f35beb66ca67bbb5672d179132768f8a2cd`  
		Last Modified: Fri, 04 Jul 2025 00:11:00 GMT  
		Size: 104.3 MB (104331195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eb567fb626e398352ebaeba3117cc5c1e6d7900ea17cf05488e4241c0a20947`  
		Last Modified: Thu, 03 Jul 2025 23:09:30 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a041ea15491fc46539cf8448b5b9a32599fa66837da558bb2b2a05d15475b370`  
		Last Modified: Thu, 03 Jul 2025 23:09:33 GMT  
		Size: 20.1 MB (20123806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b53313722a28a37fcf362c544cf3f7d373aec9208516d23db137f1716f2f6595`  
		Last Modified: Thu, 03 Jul 2025 23:09:31 GMT  
		Size: 431.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1660f89bd2c2fc7e54452c43d168e8c5eb69a6e421a9f95a56fc2d6e4c3f310c`  
		Last Modified: Thu, 03 Jul 2025 23:09:31 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41f34298e3d069fb6091d421046702726fe5cf614ced1f369ec1e9dc56c03e7b`  
		Last Modified: Thu, 03 Jul 2025 23:09:34 GMT  
		Size: 12.0 MB (12027775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfa4126235b78d5e12ca7de5e5807e3f407df479930ec41d3d45c80e02edbff4`  
		Last Modified: Thu, 03 Jul 2025 23:09:32 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88cd14855df225f3db04a9c93aae63acc43bcc99b5b2df5b874d30f259f4c6dd`  
		Last Modified: Thu, 03 Jul 2025 23:09:35 GMT  
		Size: 11.2 MB (11159691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:225778fdeccf587adc61e79895e290ba7e44c8467087cd3798cf92cab360ebd3`  
		Last Modified: Thu, 03 Jul 2025 23:09:32 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89476a2bbbd0cee95c56573267404434d22b06b23c3535a161d7769cdca18ccd`  
		Last Modified: Thu, 03 Jul 2025 23:09:27 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1215c71937e9f773a96e809bc796d591445f2857d1cac1c752dda8c89814c654`  
		Last Modified: Thu, 03 Jul 2025 23:09:27 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed34658578590935feb9715f96f087741a6371e2a475c0475757e9b05d1484f`  
		Last Modified: Thu, 03 Jul 2025 23:09:27 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4f0919ffc9cd7635d8080ff7bab0a0e24debbc7b6ee3626f1faf042f4968990`  
		Last Modified: Fri, 04 Jul 2025 00:18:29 GMT  
		Size: 53.9 MB (53893901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:706244e6e54e288a4d872f48c4121eb6b0f59b5c900822f5eb5e1c976b644fa9`  
		Last Modified: Fri, 04 Jul 2025 00:18:26 GMT  
		Size: 2.1 MB (2079714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd509e7455fe2470ecd8d833c93986dc7fbfac7369e3d2534df38130b14d501b`  
		Last Modified: Fri, 04 Jul 2025 00:18:25 GMT  
		Size: 574.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d4fcb8fed240eafdfe73e972b5a63c9a06592f55a59e3ef31375e034c51dec3`  
		Last Modified: Fri, 04 Jul 2025 00:18:25 GMT  
		Size: 902.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:217117a96b58e990ce0db6914b9f8533494be8156ffc2e9a147aeb1780f46960`  
		Last Modified: Fri, 04 Jul 2025 00:18:25 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd9b9ed06fa80b243df720060d4eb2212efaf5fb79d8e13ef099e0dd1f239415`  
		Last Modified: Fri, 04 Jul 2025 00:18:25 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2749021bcf17c37be03d1a3422c4721249a0f395f1d84637020ae56a8d318000`  
		Last Modified: Fri, 04 Jul 2025 00:18:35 GMT  
		Size: 94.5 MB (94498997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mediawiki:stable` - unknown; unknown

```console
$ docker pull mediawiki@sha256:208f974ea4236f657cab1a454676d8f4739bd60626784c57b738404d95a16c57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 KB (49101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2145504134669df29de96b6ff81d1a45d13050523a31e0416f90ab1b3812a495`

```dockerfile
```

-	Layers:
	-	`sha256:04dc845f5aab53175123c4df78316b9f06706bfa4363486ea3a3efc4ccfa8259`  
		Last Modified: Fri, 04 Jul 2025 03:18:19 GMT  
		Size: 49.1 KB (49101 bytes)  
		MIME: application/vnd.in-toto+json

### `mediawiki:stable` - linux; arm variant v5

```console
$ docker pull mediawiki@sha256:2fc8a0e9895ab6dc083275707616115b2848eafdbc77a7d9aed718b53ebbe0cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.8 MB (294849210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa21460798e8893dc94ecf1d3ac80173337b154a9f0a0cbb1ef12bb9f218c895`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 30 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1751241600'
# Wed, 02 Jul 2025 21:52:08 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 02 Jul 2025 21:52:08 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 02 Jul 2025 21:52:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Jul 2025 21:52:08 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 02 Jul 2025 21:52:08 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 02 Jul 2025 21:52:08 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 02 Jul 2025 21:52:08 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 02 Jul 2025 21:52:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 02 Jul 2025 21:52:08 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 02 Jul 2025 21:52:08 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 02 Jul 2025 21:52:08 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 02 Jul 2025 21:52:08 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 02 Jul 2025 21:52:08 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 02 Jul 2025 21:52:08 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 02 Jul 2025 21:52:08 GMT
ENV PHP_VERSION=8.1.33
# Wed, 02 Jul 2025 21:52:08 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.33.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.33.tar.xz.asc
# Wed, 02 Jul 2025 21:52:08 GMT
ENV PHP_SHA256=9db83bf4590375562bc1a10b353cccbcf9fcfc56c58b7c8fb814e6865bb928d1
# Wed, 02 Jul 2025 21:52:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 02 Jul 2025 21:52:08 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 02 Jul 2025 21:52:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 02 Jul 2025 21:52:08 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 02 Jul 2025 21:52:08 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 02 Jul 2025 21:52:08 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 02 Jul 2025 21:52:08 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 02 Jul 2025 21:52:08 GMT
STOPSIGNAL SIGWINCH
# Wed, 02 Jul 2025 21:52:08 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 02 Jul 2025 21:52:08 GMT
WORKDIR /var/www/html
# Wed, 02 Jul 2025 21:52:08 GMT
EXPOSE map[80/tcp:{}]
# Wed, 02 Jul 2025 21:52:08 GMT
CMD ["apache2-foreground"]
# Wed, 02 Jul 2025 21:52:08 GMT
RUN set -eux; 		apt-get update; 	apt-get install -y --no-install-recommends 		git 		librsvg2-bin 		imagemagick 		python3 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Jul 2025 21:52:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libicu-dev 		libonig-dev 		liblua5.1-0-dev 	; 		docker-php-ext-install -j "$(nproc)" 		calendar 		intl 		mbstring 		mysqli 		opcache 	; 		pecl install APCu-5.1.24; 	pecl install LuaSandbox-4.1.2; 	docker-php-ext-enable 		apcu 		luasandbox 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Jul 2025 21:52:08 GMT
RUN set -eux; 	a2enmod rewrite; 	{ 		echo "<Directory /var/www/html>"; 		echo "  RewriteEngine On"; 		echo "  RewriteCond %{REQUEST_FILENAME} !-f"; 		echo "  RewriteCond %{REQUEST_FILENAME} !-d"; 		echo "  RewriteRule ^ %{DOCUMENT_ROOT}/index.php [L]"; 		echo "</Directory>"; 	} > "$APACHE_CONFDIR/conf-available/short-url.conf"; 	a2enconf short-url # buildkit
# Wed, 02 Jul 2025 21:52:08 GMT
RUN sed -i "s/<\/VirtualHost>/\tAllowEncodedSlashes NoDecode\n<\/VirtualHost>/" "$APACHE_CONFDIR/sites-available/000-default.conf" # buildkit
# Wed, 02 Jul 2025 21:52:08 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 02 Jul 2025 21:52:08 GMT
RUN set -eux; 	mkdir -p /var/www/data; 	chown -R www-data:www-data /var/www/data # buildkit
# Wed, 02 Jul 2025 21:52:08 GMT
ENV MEDIAWIKI_MAJOR_VERSION=1.44
# Wed, 02 Jul 2025 21:52:08 GMT
ENV MEDIAWIKI_VERSION=1.44.0
# Wed, 02 Jul 2025 21:52:08 GMT
RUN set -eux; 	fetchDeps=" 		gnupg 		dirmngr 	"; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 		curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz" -o mediawiki.tar.gz; 	curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz.sig" -o mediawiki.tar.gz.sig; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 		D7D6767D135A514BEB86E9BA75682B08E8A3FEC4 		441276E9CCD15F44F6D97D18C119E1A64D70938E 		F7F780D82EBFB8A56556E7EE82403E59F9F8CD79 		1D98867E82982C8FE0ABC25F9B69B3109D3BB7B0 		E059C034E7A430583C252F4AA8F734246D73B586 	; 	gpg --batch --verify mediawiki.tar.gz.sig mediawiki.tar.gz; 	tar -x --strip-components=1 -f mediawiki.tar.gz; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" mediawiki.tar.gz.sig mediawiki.tar.gz; 	chown -R www-data:www-data extensions skins cache images; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Jul 2025 21:52:08 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:57a7872a7ce75b95d171f720f215d4e72b887ae709c5c0b319f93f704bd71e07`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 25.8 MB (25762460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69b05322491f7f224fdb6afd1a4feb0c269fe0910bd44e82e37a846aec3e465c`  
		Last Modified: Tue, 01 Jul 2025 03:03:10 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e58b493a89b33667d984de07320c027ba0599d73427f434c8ec42c944a6bd4aa`  
		Last Modified: Tue, 01 Jul 2025 03:03:27 GMT  
		Size: 82.0 MB (81973614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eef43b7ed80f2af53848f0179316741b5f6d73203876a5f0f62b038d570f6c8`  
		Last Modified: Tue, 01 Jul 2025 03:03:10 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1601706ea1ce67f559cb97c579c16dd941d3841c0536aea9a41a8892de970a15`  
		Last Modified: Tue, 01 Jul 2025 03:07:29 GMT  
		Size: 19.4 MB (19418152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddc8e91d03bdddc0ecb98561647c397edd946b0e408f3e4b937dd86f102157fe`  
		Last Modified: Tue, 01 Jul 2025 03:07:28 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8793820eb88ba267b7037f6242d4786a223433f5744eebb87088af136b6b8015`  
		Last Modified: Tue, 01 Jul 2025 03:07:28 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df5834aa9a2830197e5f7e931596084aa1dfd98437ec18ff098891a791f73473`  
		Last Modified: Fri, 04 Jul 2025 00:13:42 GMT  
		Size: 12.0 MB (12025882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed5a5be7767a2b322780f2eec40c791b9f305831b2a218d9d2adc9bd9bc72058`  
		Last Modified: Fri, 04 Jul 2025 00:13:40 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28379ad16ee7ce7e5eea7fe290dfeec82db848c922a979da89f85023cbe146d4`  
		Last Modified: Fri, 04 Jul 2025 00:13:42 GMT  
		Size: 10.1 MB (10119261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdbdb12207b8434ff125d53362da7cc0f2b3b2cbcda76059a4e1fc64f52007de`  
		Last Modified: Fri, 04 Jul 2025 00:13:39 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:257e3d24dbc2f2e88c2f76da63fc6fd68db62c4a02f83022d258376b68024a7d`  
		Last Modified: Fri, 04 Jul 2025 00:13:39 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5139620b83bf64655358b40c854560c1d5fc37b6edc16fd0c06fb9a2a599259`  
		Last Modified: Fri, 04 Jul 2025 00:13:40 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:788b001662eabc317ca3384fa95b216568d8c3fcba533c1b7d9cb74db2b24e89`  
		Last Modified: Fri, 04 Jul 2025 00:13:41 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbe3e7110ea3b31aa74de84c47413abea0892bd5d4e008713595bb1f573d85ef`  
		Last Modified: Fri, 04 Jul 2025 02:39:09 GMT  
		Size: 49.4 MB (49412265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44776a9f818f55ccec5247676d076bd08acb9b2041b6a2baef49671e6a2c0dda`  
		Last Modified: Fri, 04 Jul 2025 02:38:44 GMT  
		Size: 1.6 MB (1632875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:943da11e23df1fb4cc452fd8d29c93df1a1dd765984dab11fc3505ba2a09a993`  
		Last Modified: Fri, 04 Jul 2025 02:38:43 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00b1d26917072de1e2f0dbe13833f946d5afb2da67ca51f3d2eb901a041733de`  
		Last Modified: Fri, 04 Jul 2025 02:38:43 GMT  
		Size: 904.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65b87938d8f6c5f57439f120f8221cfe0ce804d14e6cf01656dbaf9ae8f22630`  
		Last Modified: Fri, 04 Jul 2025 02:38:44 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5d85a0a0c93328a6aaa4f61d7b7db0ea588a3379be5f13a9d37e3746574e7fa`  
		Last Modified: Fri, 04 Jul 2025 02:38:44 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac578cb1f15b59c81e51f960c84c984356fc931c173462ad12098a90d09b8d48`  
		Last Modified: Fri, 04 Jul 2025 03:18:56 GMT  
		Size: 94.5 MB (94497035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mediawiki:stable` - unknown; unknown

```console
$ docker pull mediawiki@sha256:1bc8bc68e05ae9467e7e433043fca6e2594a97c2b180e3091c5ed6a76a913e77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 KB (49246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4edead4854086e0bd4a3006b8a570875361bfd6e2b7ae76808d3f0735611afb8`

```dockerfile
```

-	Layers:
	-	`sha256:095f3eae3122b2fbf11ddc86cfc46a82423cee592f21ad110b60657122b11f69`  
		Last Modified: Fri, 04 Jul 2025 03:18:22 GMT  
		Size: 49.2 KB (49246 bytes)  
		MIME: application/vnd.in-toto+json

### `mediawiki:stable` - linux; arm variant v7

```console
$ docker pull mediawiki@sha256:159a89b208be797c84030a3fe6d95be87a85d9dae522c2b8ba671e15e229d4ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.6 MB (282621856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6d11373724e2a5dbed45358fa644b2c35eba19daf48f2ebcecba964c7b9d265`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 25 Jun 2025 09:56:45 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1751241600'
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
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_VERSION=8.1.32
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.32.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.32.tar.xz.asc
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_SHA256=c582ac682a280bbc69bc2186c21eb7e3313cc73099be61a6bc1d2cd337cbf383
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
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
# Wed, 02 Jul 2025 21:52:08 GMT
RUN set -eux; 		apt-get update; 	apt-get install -y --no-install-recommends 		git 		librsvg2-bin 		imagemagick 		python3 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Jul 2025 21:52:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libicu-dev 		libonig-dev 		liblua5.1-0-dev 	; 		docker-php-ext-install -j "$(nproc)" 		calendar 		intl 		mbstring 		mysqli 		opcache 	; 		pecl install APCu-5.1.24; 	pecl install LuaSandbox-4.1.2; 	docker-php-ext-enable 		apcu 		luasandbox 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Jul 2025 21:52:08 GMT
RUN set -eux; 	a2enmod rewrite; 	{ 		echo "<Directory /var/www/html>"; 		echo "  RewriteEngine On"; 		echo "  RewriteCond %{REQUEST_FILENAME} !-f"; 		echo "  RewriteCond %{REQUEST_FILENAME} !-d"; 		echo "  RewriteRule ^ %{DOCUMENT_ROOT}/index.php [L]"; 		echo "</Directory>"; 	} > "$APACHE_CONFDIR/conf-available/short-url.conf"; 	a2enconf short-url # buildkit
# Wed, 02 Jul 2025 21:52:08 GMT
RUN sed -i "s/<\/VirtualHost>/\tAllowEncodedSlashes NoDecode\n<\/VirtualHost>/" "$APACHE_CONFDIR/sites-available/000-default.conf" # buildkit
# Wed, 02 Jul 2025 21:52:08 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 02 Jul 2025 21:52:08 GMT
RUN set -eux; 	mkdir -p /var/www/data; 	chown -R www-data:www-data /var/www/data # buildkit
# Wed, 02 Jul 2025 21:52:08 GMT
ENV MEDIAWIKI_MAJOR_VERSION=1.44
# Wed, 02 Jul 2025 21:52:08 GMT
ENV MEDIAWIKI_VERSION=1.44.0
# Wed, 02 Jul 2025 21:52:08 GMT
RUN set -eux; 	fetchDeps=" 		gnupg 		dirmngr 	"; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 		curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz" -o mediawiki.tar.gz; 	curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz.sig" -o mediawiki.tar.gz.sig; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 		D7D6767D135A514BEB86E9BA75682B08E8A3FEC4 		441276E9CCD15F44F6D97D18C119E1A64D70938E 		F7F780D82EBFB8A56556E7EE82403E59F9F8CD79 		1D98867E82982C8FE0ABC25F9B69B3109D3BB7B0 		E059C034E7A430583C252F4AA8F734246D73B586 	; 	gpg --batch --verify mediawiki.tar.gz.sig mediawiki.tar.gz; 	tar -x --strip-components=1 -f mediawiki.tar.gz; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" mediawiki.tar.gz.sig mediawiki.tar.gz; 	chown -R www-data:www-data extensions skins cache images; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Jul 2025 21:52:08 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:aa4115c1f73522274017cc9ef4668eb7be9359f354969cd6ffca48411714e948`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef237a39acf4f8b50140ea0e65e44fb78759dd5c3014dea07a2e868cbaea5448`  
		Last Modified: Tue, 01 Jul 2025 02:37:03 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95d1f66f2aaac83b6eaf2006cda16a0feae7d183fb4de3fc7f021a3b94f4d2f5`  
		Last Modified: Tue, 01 Jul 2025 02:37:09 GMT  
		Size: 76.1 MB (76149625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:834cb9f18ec360ae1dafdba9049fa98c9a4c9dff8f407122be76f6644c8deb27`  
		Last Modified: Tue, 01 Jul 2025 02:37:03 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f48e36c51ca567e00204b7602dd2f3197ed65c785e21a191aec888d5acbe886`  
		Last Modified: Tue, 01 Jul 2025 02:40:42 GMT  
		Size: 18.9 MB (18855730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:739500a213db554802bf5a3a6ea64baa201f9a9e42247c34a186877ff2824052`  
		Last Modified: Tue, 01 Jul 2025 02:40:41 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a65a3ecd90f92c07f97694692d2624d48f057c9b5aa300524021d73c2c682a3`  
		Last Modified: Tue, 01 Jul 2025 02:40:41 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f52928ab11c23874665bc4ac8a638eede68492a415de1df657c8ee229113132`  
		Last Modified: Tue, 01 Jul 2025 05:18:35 GMT  
		Size: 12.0 MB (12020425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c3afb4c9975d5995a562ea7d863d8dcd3d1d369e41ad2c674f1499d6a777ad`  
		Last Modified: Tue, 01 Jul 2025 05:18:34 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33cd1eb0ce017cce8c2c8ba3772940856fa61aa2853610245d4c25833fe40e5f`  
		Last Modified: Tue, 01 Jul 2025 05:18:34 GMT  
		Size: 9.6 MB (9584888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8c3c6d1cff6d50079727a69d3df819820f3936d37999807cc0dc077b8ca646`  
		Last Modified: Tue, 01 Jul 2025 05:18:33 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c26fa3f1d7c9024a4c023a2f7f4e62a7fcd45928d33c37aaa02a1ea43f10de76`  
		Last Modified: Tue, 01 Jul 2025 05:18:34 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1bceb6547985bf940132b390d75468bda728bf64f7a7a73a1a5b1ad309e4a0a`  
		Last Modified: Tue, 01 Jul 2025 05:18:34 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa3836cd658916e88bd07a521a155514745692b391b7ab137e89c6b2403ea905`  
		Last Modified: Tue, 01 Jul 2025 05:18:34 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66abc117a95db571e832426fe52471de42c6f8ca03d3716ad546af53ec6fb52d`  
		Last Modified: Tue, 01 Jul 2025 19:54:47 GMT  
		Size: 46.0 MB (45993541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4a6def07c4042335bd4eafcba3bf43085dd89234204b685c6924b7fb5c03e65`  
		Last Modified: Tue, 01 Jul 2025 19:54:43 GMT  
		Size: 1.6 MB (1574426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c95096f59ab8a07e5fb3dfc791258066aa056035bb3c3ac641ae2b09d52075f6`  
		Last Modified: Tue, 01 Jul 2025 19:54:43 GMT  
		Size: 575.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee3038b5c4d1e858b669252d8af817cfa1ced7096bbf2e789b5b96743fa0443`  
		Last Modified: Tue, 01 Jul 2025 19:54:43 GMT  
		Size: 906.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d11dc67da2e7e7bbeb0fafe62055dd73958e42b65e9aa003cb9450564f0fd01`  
		Last Modified: Tue, 01 Jul 2025 19:54:43 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e44deddbe68398d5e40fe7a9752b528881711ff01e331df458ec43995999d024`  
		Last Modified: Tue, 01 Jul 2025 19:54:43 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81962395abbdc771f9413f278dbc3b53b2715899e5f29c45eec996d40d09c0d0`  
		Last Modified: Wed, 02 Jul 2025 22:21:08 GMT  
		Size: 94.5 MB (94496810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mediawiki:stable` - unknown; unknown

```console
$ docker pull mediawiki@sha256:5775b0a7dfdb836cfec3ccad9c3dd963171948ce1e4e0e1156577d7dc68c68e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 KB (49239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:616bd79abf98b56322705f6b2cd01e49d7c6ba49191668e885b081f721fa6c86`

```dockerfile
```

-	Layers:
	-	`sha256:06efbdb3a51e60812c5237215be308ad0fca5d129c523302b57451db085f1aed`  
		Last Modified: Thu, 03 Jul 2025 00:17:01 GMT  
		Size: 49.2 KB (49239 bytes)  
		MIME: application/vnd.in-toto+json

### `mediawiki:stable` - linux; arm64 variant v8

```console
$ docker pull mediawiki@sha256:c37b53e26016534e1025989a43a67a832443aa4ec6375f01ed6257a9805c4aa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.5 MB (317484938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a906d0d50f44c2dfb111e2ffd477cc2046afa7455bd05ce8a1b0ac90c0ca81ee`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 25 Jun 2025 09:56:45 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
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
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_VERSION=8.1.32
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.32.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.32.tar.xz.asc
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_SHA256=c582ac682a280bbc69bc2186c21eb7e3313cc73099be61a6bc1d2cd337cbf383
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
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
# Wed, 02 Jul 2025 21:52:08 GMT
RUN set -eux; 		apt-get update; 	apt-get install -y --no-install-recommends 		git 		librsvg2-bin 		imagemagick 		python3 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Jul 2025 21:52:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libicu-dev 		libonig-dev 		liblua5.1-0-dev 	; 		docker-php-ext-install -j "$(nproc)" 		calendar 		intl 		mbstring 		mysqli 		opcache 	; 		pecl install APCu-5.1.24; 	pecl install LuaSandbox-4.1.2; 	docker-php-ext-enable 		apcu 		luasandbox 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Jul 2025 21:52:08 GMT
RUN set -eux; 	a2enmod rewrite; 	{ 		echo "<Directory /var/www/html>"; 		echo "  RewriteEngine On"; 		echo "  RewriteCond %{REQUEST_FILENAME} !-f"; 		echo "  RewriteCond %{REQUEST_FILENAME} !-d"; 		echo "  RewriteRule ^ %{DOCUMENT_ROOT}/index.php [L]"; 		echo "</Directory>"; 	} > "$APACHE_CONFDIR/conf-available/short-url.conf"; 	a2enconf short-url # buildkit
# Wed, 02 Jul 2025 21:52:08 GMT
RUN sed -i "s/<\/VirtualHost>/\tAllowEncodedSlashes NoDecode\n<\/VirtualHost>/" "$APACHE_CONFDIR/sites-available/000-default.conf" # buildkit
# Wed, 02 Jul 2025 21:52:08 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 02 Jul 2025 21:52:08 GMT
RUN set -eux; 	mkdir -p /var/www/data; 	chown -R www-data:www-data /var/www/data # buildkit
# Wed, 02 Jul 2025 21:52:08 GMT
ENV MEDIAWIKI_MAJOR_VERSION=1.44
# Wed, 02 Jul 2025 21:52:08 GMT
ENV MEDIAWIKI_VERSION=1.44.0
# Wed, 02 Jul 2025 21:52:08 GMT
RUN set -eux; 	fetchDeps=" 		gnupg 		dirmngr 	"; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 		curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz" -o mediawiki.tar.gz; 	curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz.sig" -o mediawiki.tar.gz.sig; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 		D7D6767D135A514BEB86E9BA75682B08E8A3FEC4 		441276E9CCD15F44F6D97D18C119E1A64D70938E 		F7F780D82EBFB8A56556E7EE82403E59F9F8CD79 		1D98867E82982C8FE0ABC25F9B69B3109D3BB7B0 		E059C034E7A430583C252F4AA8F734246D73B586 	; 	gpg --batch --verify mediawiki.tar.gz.sig mediawiki.tar.gz; 	tar -x --strip-components=1 -f mediawiki.tar.gz; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" mediawiki.tar.gz.sig mediawiki.tar.gz; 	chown -R www-data:www-data extensions skins cache images; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Jul 2025 21:52:08 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:37259e7330667afd74c3386d3ed869f06bd9b7714370c78e3065f4e28607cc02`  
		Last Modified: Tue, 01 Jul 2025 01:15:09 GMT  
		Size: 28.1 MB (28077678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d11709a68ca8c2093073c9a1d4b656c3cf0443563f219a68b0b4d26313c3ea1`  
		Last Modified: Tue, 01 Jul 2025 03:15:53 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af5584d1cd13b2f94aca836225a1f54b5de7c1c9943fe27f25088a0be3a7059a`  
		Last Modified: Tue, 01 Jul 2025 03:16:04 GMT  
		Size: 98.1 MB (98130658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e73f9696b074c2e8b1d467becd89db85a06286c5c522e385d7dfe3d5c3e8c565`  
		Last Modified: Tue, 01 Jul 2025 03:15:54 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0338344fbbdf3fd875b6282992d879c84330f79444f2b26fa06fd262d91f5b66`  
		Last Modified: Tue, 01 Jul 2025 03:19:33 GMT  
		Size: 20.1 MB (20136183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ac6599ba91eea05ea5485c293321ec9fb98775e592c2b807fb3728dd999380d`  
		Last Modified: Tue, 01 Jul 2025 03:19:30 GMT  
		Size: 433.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b38126f76137940856be8dca967826d804d2ea33b4661b247ce1768d9a21aed1`  
		Last Modified: Tue, 01 Jul 2025 03:19:31 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:065f24729b4ad57698938397345d92a4e4dfb2b9f1aab871fea50841021116e5`  
		Last Modified: Tue, 01 Jul 2025 05:44:56 GMT  
		Size: 12.0 MB (12022188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a4bf62a7b7415aff24a95226e2dba2a5204d80df03a9e8e1a921ce09dbf96b5`  
		Last Modified: Tue, 01 Jul 2025 05:44:55 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ece5a82707dd27b2ad3e663098f619a5016065a65474277b98733dcd65012369`  
		Last Modified: Tue, 01 Jul 2025 05:44:56 GMT  
		Size: 11.2 MB (11178728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71882934289a4251e3dd9f41ece9f6e3c873cde3349fff7e4fe9f3930bcfc5b8`  
		Last Modified: Tue, 01 Jul 2025 05:44:55 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:465b0c37d97d03674b7ef8351d3a610648f18e09332360d200cf80fcd7efaf4d`  
		Last Modified: Tue, 01 Jul 2025 05:44:54 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74192070fc2bdd67f55b6f88a4c16acdb54a6392d8a0260d11f44bf6d80da366`  
		Last Modified: Tue, 01 Jul 2025 05:44:55 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d2af8ce2b1e72fd0ba0779a1ad08b445f1ec2f76f358275581b1c9b732afba6`  
		Last Modified: Tue, 01 Jul 2025 05:44:55 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fc1b5dfc5c6078be616f77551787bf7e222a8b1c946cc8d0c080527f1f8afef`  
		Last Modified: Wed, 02 Jul 2025 22:31:02 GMT  
		Size: 51.1 MB (51096025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:311125a04bfe1a3bbab361c24dcad8ddd97fa4207e5d718090bb8def9b3b53c5`  
		Last Modified: Wed, 02 Jul 2025 22:31:00 GMT  
		Size: 2.3 MB (2337042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf7825289d796bde67cf1f1db34be71ba3bf992b95b949ccb0a23d3d7e4da48c`  
		Last Modified: Wed, 02 Jul 2025 22:31:00 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26e5d5d811d547614b7d1dcc54815a185441d51f62132ed96c08a3c1a7295849`  
		Last Modified: Wed, 02 Jul 2025 22:31:00 GMT  
		Size: 905.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b72a36efafe828b44d659eeec413d79dd2bfb7139f4e045c12b99ac567703b1`  
		Last Modified: Wed, 02 Jul 2025 22:31:00 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ffb95d1a97bc64c1f4db4d4aa7c9605d099ed8d512cc6f265b4d8ac940f4ee6`  
		Last Modified: Wed, 02 Jul 2025 22:31:00 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:720c698739a89dafb2d38d4aa78e4bca78b0e0a6e9daf4222fedf31b42392f28`  
		Last Modified: Wed, 02 Jul 2025 22:31:05 GMT  
		Size: 94.5 MB (94498776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mediawiki:stable` - unknown; unknown

```console
$ docker pull mediawiki@sha256:2cf2d9134ab19ea561e243908ccf66fa6dac3b479b59404c4dbf8be767fa5708
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 KB (49287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:179259c871e5629f8c59fb514995e3146dcf7df77dd75b245d659cd3b08629a5`

```dockerfile
```

-	Layers:
	-	`sha256:b7f8162241db174b8a364cfed3208bb724de610f1c74e6fd206be4fd02986eb1`  
		Last Modified: Thu, 03 Jul 2025 00:17:05 GMT  
		Size: 49.3 KB (49287 bytes)  
		MIME: application/vnd.in-toto+json

### `mediawiki:stable` - linux; 386

```console
$ docker pull mediawiki@sha256:f84d4a434ba3c7ad4716798bc324f0a7a17435bf5543603b98efbd0b224d904f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.8 MB (326794620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29df81a2ebda71456c34ecc1d52ce9763cec01dc130a7960e2e6ec17f6296e4a`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 30 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1751241600'
# Wed, 02 Jul 2025 21:52:08 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 02 Jul 2025 21:52:08 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 02 Jul 2025 21:52:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Jul 2025 21:52:08 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 02 Jul 2025 21:52:08 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 02 Jul 2025 21:52:08 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 02 Jul 2025 21:52:08 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 02 Jul 2025 21:52:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 02 Jul 2025 21:52:08 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 02 Jul 2025 21:52:08 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 02 Jul 2025 21:52:08 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 02 Jul 2025 21:52:08 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 02 Jul 2025 21:52:08 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 02 Jul 2025 21:52:08 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 02 Jul 2025 21:52:08 GMT
ENV PHP_VERSION=8.1.33
# Wed, 02 Jul 2025 21:52:08 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.33.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.33.tar.xz.asc
# Wed, 02 Jul 2025 21:52:08 GMT
ENV PHP_SHA256=9db83bf4590375562bc1a10b353cccbcf9fcfc56c58b7c8fb814e6865bb928d1
# Wed, 02 Jul 2025 21:52:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 02 Jul 2025 21:52:08 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 02 Jul 2025 21:52:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 02 Jul 2025 21:52:08 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 02 Jul 2025 21:52:08 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 02 Jul 2025 21:52:08 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 02 Jul 2025 21:52:08 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 02 Jul 2025 21:52:08 GMT
STOPSIGNAL SIGWINCH
# Wed, 02 Jul 2025 21:52:08 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 02 Jul 2025 21:52:08 GMT
WORKDIR /var/www/html
# Wed, 02 Jul 2025 21:52:08 GMT
EXPOSE map[80/tcp:{}]
# Wed, 02 Jul 2025 21:52:08 GMT
CMD ["apache2-foreground"]
# Wed, 02 Jul 2025 21:52:08 GMT
RUN set -eux; 		apt-get update; 	apt-get install -y --no-install-recommends 		git 		librsvg2-bin 		imagemagick 		python3 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Jul 2025 21:52:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libicu-dev 		libonig-dev 		liblua5.1-0-dev 	; 		docker-php-ext-install -j "$(nproc)" 		calendar 		intl 		mbstring 		mysqli 		opcache 	; 		pecl install APCu-5.1.24; 	pecl install LuaSandbox-4.1.2; 	docker-php-ext-enable 		apcu 		luasandbox 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Jul 2025 21:52:08 GMT
RUN set -eux; 	a2enmod rewrite; 	{ 		echo "<Directory /var/www/html>"; 		echo "  RewriteEngine On"; 		echo "  RewriteCond %{REQUEST_FILENAME} !-f"; 		echo "  RewriteCond %{REQUEST_FILENAME} !-d"; 		echo "  RewriteRule ^ %{DOCUMENT_ROOT}/index.php [L]"; 		echo "</Directory>"; 	} > "$APACHE_CONFDIR/conf-available/short-url.conf"; 	a2enconf short-url # buildkit
# Wed, 02 Jul 2025 21:52:08 GMT
RUN sed -i "s/<\/VirtualHost>/\tAllowEncodedSlashes NoDecode\n<\/VirtualHost>/" "$APACHE_CONFDIR/sites-available/000-default.conf" # buildkit
# Wed, 02 Jul 2025 21:52:08 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 02 Jul 2025 21:52:08 GMT
RUN set -eux; 	mkdir -p /var/www/data; 	chown -R www-data:www-data /var/www/data # buildkit
# Wed, 02 Jul 2025 21:52:08 GMT
ENV MEDIAWIKI_MAJOR_VERSION=1.44
# Wed, 02 Jul 2025 21:52:08 GMT
ENV MEDIAWIKI_VERSION=1.44.0
# Wed, 02 Jul 2025 21:52:08 GMT
RUN set -eux; 	fetchDeps=" 		gnupg 		dirmngr 	"; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 		curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz" -o mediawiki.tar.gz; 	curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz.sig" -o mediawiki.tar.gz.sig; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 		D7D6767D135A514BEB86E9BA75682B08E8A3FEC4 		441276E9CCD15F44F6D97D18C119E1A64D70938E 		F7F780D82EBFB8A56556E7EE82403E59F9F8CD79 		1D98867E82982C8FE0ABC25F9B69B3109D3BB7B0 		E059C034E7A430583C252F4AA8F734246D73B586 	; 	gpg --batch --verify mediawiki.tar.gz.sig mediawiki.tar.gz; 	tar -x --strip-components=1 -f mediawiki.tar.gz; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" mediawiki.tar.gz.sig mediawiki.tar.gz; 	chown -R www-data:www-data extensions skins cache images; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Jul 2025 21:52:08 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:88e96ee0cb4c7106f4d6a5cdeaeb171ec22a2484245e406cb5267b2be095937c`  
		Last Modified: Tue, 01 Jul 2025 01:14:33 GMT  
		Size: 29.2 MB (29212432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c1bfca268301eade00362af7aaf901cc61abf5af6f2f17efbff545717d2d62a`  
		Last Modified: Thu, 03 Jul 2025 23:11:05 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c66ea1d216304a50ea14854c11145b2c9bd1b78f6c56b1e0fcfbe31ad301b224`  
		Last Modified: Thu, 03 Jul 2025 23:11:06 GMT  
		Size: 101.5 MB (101515436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5d50a1035a2453b9de3c026c36e93d8047dd640ed172395d29d59854de18668`  
		Last Modified: Thu, 03 Jul 2025 23:09:47 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b06e1882990195f7b247caa007c3b1f04260dd6884c309027ab063704e4235e4`  
		Last Modified: Thu, 03 Jul 2025 23:11:02 GMT  
		Size: 20.6 MB (20638453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a57b4eb5946d64de643ff342e88cd5dfd09e5d7351c6c806ca8d4cdaf1411227`  
		Last Modified: Thu, 03 Jul 2025 23:11:00 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f2a6930dbd40115d98256ccc57d12a04ab72a22727eeed416a3250d84080bd`  
		Last Modified: Thu, 03 Jul 2025 23:11:00 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43616a63c9cc9bf76bc68d9a76daf3b06d22831c7305757bf285b484e2026987`  
		Last Modified: Thu, 03 Jul 2025 23:11:01 GMT  
		Size: 12.0 MB (12026828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fd43a0405a5f4a05c37172425bec11ebb4a3c5a26a13b6ccd1cd59b36ac62c6`  
		Last Modified: Thu, 03 Jul 2025 23:11:01 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f496f4cca64fe4985b12730ca2d4352ae823c7e2243a0907c99cd8e59dec5c6c`  
		Last Modified: Thu, 03 Jul 2025 23:11:02 GMT  
		Size: 11.4 MB (11384023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54467727f07e6a04893ab5d87e9455cc983f7e3e913c1bb784b2ba85fc787634`  
		Last Modified: Thu, 03 Jul 2025 23:11:01 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b94a40f4ac922edf1badbbfb500f76882ae7ea619185d4a8e8218d18cca91aa6`  
		Last Modified: Thu, 03 Jul 2025 23:11:01 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a6336d56ddc37dd73c6ce8283b4b797a2368cb9bd26ebd6e62350ff9b8d2e9f`  
		Last Modified: Thu, 03 Jul 2025 23:11:01 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50def80b8c47e0eaa0348b64198ae733c038172e86a701a8e95e38fc676f9312`  
		Last Modified: Thu, 03 Jul 2025 23:11:01 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7592d0bff6e4293b17629fba1c2f50c8b7c271e741ce998297e475cf25b94fd6`  
		Last Modified: Fri, 04 Jul 2025 00:17:49 GMT  
		Size: 55.4 MB (55430970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5956def310dbee1e3a7aeb68588283f352145176c81a9dedcf8727eb994d9851`  
		Last Modified: Fri, 04 Jul 2025 00:17:46 GMT  
		Size: 2.1 MB (2080167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22a803e843fb40e5b53767d2437fb3650d49bb30832b673a843c3a8b6be8916a`  
		Last Modified: Fri, 04 Jul 2025 00:17:45 GMT  
		Size: 577.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d34c979734c85cddaf7b8663ed5651734e7a162c5a4109d93f59d1b987f20d6b`  
		Last Modified: Fri, 04 Jul 2025 00:17:45 GMT  
		Size: 902.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b2d8771b4c67a080afce4368d64801de11b9508bb27cc23599fb0c09742775f`  
		Last Modified: Fri, 04 Jul 2025 00:17:45 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a27d7fc99b4ba4fd33e9f87edd7e4771266bccd50c2d99839b3918a959bebff3`  
		Last Modified: Fri, 04 Jul 2025 00:17:45 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eeb021187f0dbc8468e50fdd41d6a5ac346dcdb0b34762317ad5022bb204883`  
		Last Modified: Fri, 04 Jul 2025 00:17:53 GMT  
		Size: 94.5 MB (94498651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mediawiki:stable` - unknown; unknown

```console
$ docker pull mediawiki@sha256:80bc71e92019176eb6daa33ada74470a41256cdffe4c12a561331f88c4823145
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 KB (49057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cc3d3e3189c5b9cd8c4a2bd010d8f47e10f84ea9556c478034d05fbdcc39664`

```dockerfile
```

-	Layers:
	-	`sha256:1d3f808f16432d1222548829dec0e9a2310f9f31871632787da364751259390d`  
		Last Modified: Fri, 04 Jul 2025 03:18:30 GMT  
		Size: 49.1 KB (49057 bytes)  
		MIME: application/vnd.in-toto+json

### `mediawiki:stable` - linux; ppc64le

```console
$ docker pull mediawiki@sha256:11829f50ab3f4b867f233a47fe207b5ec70efa2085ef9eaa42d736ce33be189b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.7 MB (334686951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a106a9812fbebbddce1d3f75bde3686a0227b4b6fe86be08c691936a890df19`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 30 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1751241600'
# Wed, 02 Jul 2025 21:52:08 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 02 Jul 2025 21:52:08 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 02 Jul 2025 21:52:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Jul 2025 21:52:08 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 02 Jul 2025 21:52:08 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 02 Jul 2025 21:52:08 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 02 Jul 2025 21:52:08 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 02 Jul 2025 21:52:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 02 Jul 2025 21:52:08 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 02 Jul 2025 21:52:08 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 02 Jul 2025 21:52:08 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 02 Jul 2025 21:52:08 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 02 Jul 2025 21:52:08 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 02 Jul 2025 21:52:08 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 02 Jul 2025 21:52:08 GMT
ENV PHP_VERSION=8.1.33
# Wed, 02 Jul 2025 21:52:08 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.33.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.33.tar.xz.asc
# Wed, 02 Jul 2025 21:52:08 GMT
ENV PHP_SHA256=9db83bf4590375562bc1a10b353cccbcf9fcfc56c58b7c8fb814e6865bb928d1
# Wed, 02 Jul 2025 21:52:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 02 Jul 2025 21:52:08 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 02 Jul 2025 21:52:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 02 Jul 2025 21:52:08 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 02 Jul 2025 21:52:08 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 02 Jul 2025 21:52:08 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 02 Jul 2025 21:52:08 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 02 Jul 2025 21:52:08 GMT
STOPSIGNAL SIGWINCH
# Wed, 02 Jul 2025 21:52:08 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 02 Jul 2025 21:52:08 GMT
WORKDIR /var/www/html
# Wed, 02 Jul 2025 21:52:08 GMT
EXPOSE map[80/tcp:{}]
# Wed, 02 Jul 2025 21:52:08 GMT
CMD ["apache2-foreground"]
# Wed, 02 Jul 2025 21:52:08 GMT
RUN set -eux; 		apt-get update; 	apt-get install -y --no-install-recommends 		git 		librsvg2-bin 		imagemagick 		python3 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Jul 2025 21:52:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libicu-dev 		libonig-dev 		liblua5.1-0-dev 	; 		docker-php-ext-install -j "$(nproc)" 		calendar 		intl 		mbstring 		mysqli 		opcache 	; 		pecl install APCu-5.1.24; 	pecl install LuaSandbox-4.1.2; 	docker-php-ext-enable 		apcu 		luasandbox 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Jul 2025 21:52:08 GMT
RUN set -eux; 	a2enmod rewrite; 	{ 		echo "<Directory /var/www/html>"; 		echo "  RewriteEngine On"; 		echo "  RewriteCond %{REQUEST_FILENAME} !-f"; 		echo "  RewriteCond %{REQUEST_FILENAME} !-d"; 		echo "  RewriteRule ^ %{DOCUMENT_ROOT}/index.php [L]"; 		echo "</Directory>"; 	} > "$APACHE_CONFDIR/conf-available/short-url.conf"; 	a2enconf short-url # buildkit
# Wed, 02 Jul 2025 21:52:08 GMT
RUN sed -i "s/<\/VirtualHost>/\tAllowEncodedSlashes NoDecode\n<\/VirtualHost>/" "$APACHE_CONFDIR/sites-available/000-default.conf" # buildkit
# Wed, 02 Jul 2025 21:52:08 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 02 Jul 2025 21:52:08 GMT
RUN set -eux; 	mkdir -p /var/www/data; 	chown -R www-data:www-data /var/www/data # buildkit
# Wed, 02 Jul 2025 21:52:08 GMT
ENV MEDIAWIKI_MAJOR_VERSION=1.44
# Wed, 02 Jul 2025 21:52:08 GMT
ENV MEDIAWIKI_VERSION=1.44.0
# Wed, 02 Jul 2025 21:52:08 GMT
RUN set -eux; 	fetchDeps=" 		gnupg 		dirmngr 	"; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 		curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz" -o mediawiki.tar.gz; 	curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz.sig" -o mediawiki.tar.gz.sig; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 		D7D6767D135A514BEB86E9BA75682B08E8A3FEC4 		441276E9CCD15F44F6D97D18C119E1A64D70938E 		F7F780D82EBFB8A56556E7EE82403E59F9F8CD79 		1D98867E82982C8FE0ABC25F9B69B3109D3BB7B0 		E059C034E7A430583C252F4AA8F734246D73B586 	; 	gpg --batch --verify mediawiki.tar.gz.sig mediawiki.tar.gz; 	tar -x --strip-components=1 -f mediawiki.tar.gz; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" mediawiki.tar.gz.sig mediawiki.tar.gz; 	chown -R www-data:www-data extensions skins cache images; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Jul 2025 21:52:08 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:c5884d20b08634214a92bd5de559876bf30e6c5453807c3014f5480eeba20662`  
		Last Modified: Tue, 01 Jul 2025 01:15:20 GMT  
		Size: 32.1 MB (32072820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e36b68bed4d5c4fdbbd3f66cf1ee62569453e6d1dea00500a229578b96f8f6c3`  
		Last Modified: Thu, 03 Jul 2025 22:59:07 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c94ede1a54d9ac4e13b34ad1cd441b94ad5436ccfacbf6f1e5deb2957a47257`  
		Last Modified: Thu, 03 Jul 2025 22:59:12 GMT  
		Size: 103.3 MB (103326831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f83487f2c5b5e9a02c2d3911052a6efe6e28cc68c5a06b7a0080d8ff6f6a2c72`  
		Last Modified: Thu, 03 Jul 2025 22:59:08 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c35c67000e323388d19a55a9c5add154479cfc0fadfc7b08718851d38436f10c`  
		Last Modified: Thu, 03 Jul 2025 23:03:58 GMT  
		Size: 21.3 MB (21308277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e429ee02968ccf407fd388a5e7fdbbc3cbf9ee2fbcb868224604ee73fcebab7`  
		Last Modified: Thu, 03 Jul 2025 23:03:51 GMT  
		Size: 432.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c1eb613b404f93974eadc63042d47613e9a7c597ba569a0d16dbd3788380a77`  
		Last Modified: Thu, 03 Jul 2025 23:03:53 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d453f42a12fffd69e76ec76997478a68d17edbc2978ed8f05950c9b6a526296`  
		Last Modified: Fri, 04 Jul 2025 00:58:19 GMT  
		Size: 12.0 MB (12027253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48aae8ef3d630302db3545f027584e75219fc512098014ceb4eb9d93c0cd32c3`  
		Last Modified: Fri, 04 Jul 2025 00:58:17 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32f8095bd731d4f24e6d145f0d360f054053f223a9db465a03a6b483c3bb38ec`  
		Last Modified: Fri, 04 Jul 2025 00:58:18 GMT  
		Size: 11.5 MB (11530284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ff1ceb3e0c9cc7c3fa65f2e7a5762b9e30dd5bed1b7bab65adbdb7b07dd425a`  
		Last Modified: Fri, 04 Jul 2025 00:58:17 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62943e46eadb626507eadfb95109fb494e9fa510b4c6fc21ebba9bb018229140`  
		Last Modified: Fri, 04 Jul 2025 00:58:17 GMT  
		Size: 253.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a17a2e00248c149bdab9df381b1621850bfa540c94d5bafd643673cce5225fb`  
		Last Modified: Fri, 04 Jul 2025 00:58:17 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494437ccbc11c44873a801e8a7accccf99e7742f28a7b4ed8fcdc13d466595e0`  
		Last Modified: Fri, 04 Jul 2025 00:58:17 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01c0922dbcacba502a312bc95a7c19a14ad6507dc09abe0cbaa12ebd7f7088c6`  
		Last Modified: Fri, 04 Jul 2025 05:05:39 GMT  
		Size: 58.1 MB (58105001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d921bbf2ed755cf06a641a8b07c9bbdbfba63c21cefec02b13c3bae8a24aa61d`  
		Last Modified: Fri, 04 Jul 2025 05:05:21 GMT  
		Size: 1.8 MB (1809868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fa325262567da110ce1a4f821b7571f96c716a82386be2b7a34cc33c1c31ff8`  
		Last Modified: Fri, 04 Jul 2025 05:05:20 GMT  
		Size: 576.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:673dde50174c2be99247184199070549aeaf0e9f1b9c4ce88e128dbd7e67e739`  
		Last Modified: Fri, 04 Jul 2025 05:05:20 GMT  
		Size: 903.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:271a2b12300b87e4883107bdcb9e45a303613dac046f5f469beb12ba75b99b5c`  
		Last Modified: Fri, 04 Jul 2025 05:05:19 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07dc7f705ff24b5238bc21de51f6053ec19e00030ec850cf0dbcce669eb245e7`  
		Last Modified: Fri, 04 Jul 2025 05:05:20 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:485ac4ec1dd50479f92b1ad82408b29aaccd35f4b707f3f4cc8c16429aea6cb0`  
		Last Modified: Fri, 04 Jul 2025 06:17:21 GMT  
		Size: 94.5 MB (94498941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mediawiki:stable` - unknown; unknown

```console
$ docker pull mediawiki@sha256:9d450a2366268302d067713cd1daffcaf5daa5e6f572334923d158524367f491
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 KB (49157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:621349351a6a77c2e13a56c460fabf1ad6dc89f37c7f078553b53c3e983a293c`

```dockerfile
```

-	Layers:
	-	`sha256:aceab0a6d7c118401c2df1d202890e719d5624c4a08ce7903d037b1abd260274`  
		Last Modified: Fri, 04 Jul 2025 06:17:06 GMT  
		Size: 49.2 KB (49157 bytes)  
		MIME: application/vnd.in-toto+json
