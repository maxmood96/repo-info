## `mediawiki:lts`

```console
$ docker pull mediawiki@sha256:e19ed917ab3b9f63169cd5dd735c387a24a8c25ccb7cb28d17a68c88e0dcb573
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

### `mediawiki:lts` - linux; amd64

```console
$ docker pull mediawiki@sha256:2f223d410519651d860afa730232796d3773966105100650856a6cdd2d2dc615
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.1 MB (325078610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40dc99ea6daf0e3a83a1f5afeff99862c2819d041ca41e25e56e6efbe9ccff1b`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 10 Apr 2025 18:10:22 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 10 Apr 2025 18:10:22 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 10 Apr 2025 18:10:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 10 Apr 2025 18:10:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 10 Apr 2025 18:10:22 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Thu, 10 Apr 2025 18:10:22 GMT
ENV PHP_VERSION=8.1.32
# Thu, 10 Apr 2025 18:10:22 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.32.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.32.tar.xz.asc
# Thu, 10 Apr 2025 18:10:22 GMT
ENV PHP_SHA256=c582ac682a280bbc69bc2186c21eb7e3313cc73099be61a6bc1d2cd337cbf383
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 10 Apr 2025 18:10:22 GMT
STOPSIGNAL SIGWINCH
# Thu, 10 Apr 2025 18:10:22 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
WORKDIR /var/www/html
# Thu, 10 Apr 2025 18:10:22 GMT
EXPOSE map[80/tcp:{}]
# Thu, 10 Apr 2025 18:10:22 GMT
CMD ["apache2-foreground"]
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 		apt-get update; 	apt-get install -y --no-install-recommends 		git 		librsvg2-bin 		imagemagick 		python3 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libicu-dev 		libonig-dev 		liblua5.1-0-dev 	; 		docker-php-ext-install -j "$(nproc)" 		calendar 		intl 		mbstring 		mysqli 		opcache 	; 		pecl install APCu-5.1.24; 	pecl install LuaSandbox-4.1.2; 	docker-php-ext-enable 		apcu 		luasandbox 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 	a2enmod rewrite; 	{ 		echo "<Directory /var/www/html>"; 		echo "  RewriteEngine On"; 		echo "  RewriteCond %{REQUEST_FILENAME} !-f"; 		echo "  RewriteCond %{REQUEST_FILENAME} !-d"; 		echo "  RewriteRule ^ %{DOCUMENT_ROOT}/index.php [L]"; 		echo "</Directory>"; 	} > "$APACHE_CONFDIR/conf-available/short-url.conf"; 	a2enconf short-url # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
RUN sed -i "s/<\/VirtualHost>/\tAllowEncodedSlashes NoDecode\n<\/VirtualHost>/" "$APACHE_CONFDIR/sites-available/000-default.conf" # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 	mkdir -p /var/www/data; 	chown -R www-data:www-data /var/www/data # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
ENV MEDIAWIKI_MAJOR_VERSION=1.43
# Thu, 10 Apr 2025 18:10:22 GMT
ENV MEDIAWIKI_VERSION=1.43.1
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 	fetchDeps=" 		gnupg 		dirmngr 	"; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 		curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz" -o mediawiki.tar.gz; 	curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz.sig" -o mediawiki.tar.gz.sig; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 		D7D6767D135A514BEB86E9BA75682B08E8A3FEC4 		441276E9CCD15F44F6D97D18C119E1A64D70938E 		F7F780D82EBFB8A56556E7EE82403E59F9F8CD79 		1D98867E82982C8FE0ABC25F9B69B3109D3BB7B0 		E059C034E7A430583C252F4AA8F734246D73B586 	; 	gpg --batch --verify mediawiki.tar.gz.sig mediawiki.tar.gz; 	tar -x --strip-components=1 -f mediawiki.tar.gz; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" mediawiki.tar.gz.sig mediawiki.tar.gz; 	chown -R www-data:www-data extensions skins cache images; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:3da95a905ed546f99c4564407923a681757d89651a388ec3f1f5e9bf5ed0b39d`  
		Last Modified: Tue, 01 Jul 2025 01:14:43 GMT  
		Size: 28.2 MB (28230143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6bf4d214d15b5f890a53698401fff8a87781cdb3952aab13887dbea07dd8782`  
		Last Modified: Tue, 01 Jul 2025 02:25:04 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2ddaca1f6b2df46dc446a8cc2167e72c4a8cd6a20670cd95b83cd72b48e5a13`  
		Last Modified: Tue, 01 Jul 2025 02:25:09 GMT  
		Size: 104.3 MB (104331368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49eeb50e90fd709791a866a53d399c7465780ed9324d2bbf625a4ef498763184`  
		Last Modified: Tue, 01 Jul 2025 02:25:04 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d78d181e746276f4335d47aec08ec2c775020c2be543686979588f63eee54bf`  
		Last Modified: Tue, 01 Jul 2025 02:25:06 GMT  
		Size: 20.1 MB (20123821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2530dd1f3fdea824cd1901cfc9dc78b70e746a487b1f0a94b9ce4b64001fd8de`  
		Last Modified: Tue, 01 Jul 2025 02:25:04 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f37b58092b5318a63fec1873f10481adc03b478bf4a9be3da369729b1b6f9183`  
		Last Modified: Tue, 01 Jul 2025 02:25:04 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52dfd51e84662d5670bf942a0d8e19f92beef8910e7ef884946f5d6c11a6a8c1`  
		Last Modified: Tue, 01 Jul 2025 02:25:05 GMT  
		Size: 12.0 MB (12022471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84a8951f2917d8fcd7e9d2a57cb43a70f1f199ec27a1ca3ab90ec0ec62e95224`  
		Last Modified: Tue, 01 Jul 2025 02:25:04 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fac1fda75e78175a12e9e50416682386f1b8442fb48e48e6426520ebaa20721`  
		Last Modified: Tue, 01 Jul 2025 02:25:05 GMT  
		Size: 11.2 MB (11159515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cf3c0b17219932a7e2da006b8b7c955378b77c9be84f368119954ca3820213d`  
		Last Modified: Tue, 01 Jul 2025 02:25:04 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aba1b0a2781a3960deb488a297a83156797c8d853f0b7c79bbd230ecf0de225`  
		Last Modified: Tue, 01 Jul 2025 02:25:04 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3abaca9a6e41846dc7ac14c15e16b8a394f1f301015d82c14b294eeb7ae07a1`  
		Last Modified: Tue, 01 Jul 2025 02:25:04 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c67ad0fc64f10e7532dfc5245e60ce23c61f983f68b6766ae7646dd8c187876`  
		Last Modified: Tue, 01 Jul 2025 02:25:04 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:807449ad47c65e1ca3a926a22c7ac9fa60a5b72a23aec668aac31d472c0c3ad8`  
		Last Modified: Tue, 01 Jul 2025 05:03:11 GMT  
		Size: 53.9 MB (53894052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d48c54767d88f33838989bcf2d4b33515bef26975a0ec52332999cfd3daf3a95`  
		Last Modified: Tue, 01 Jul 2025 03:26:30 GMT  
		Size: 2.1 MB (2079808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ed40c172a59b89eeab3705212e99aa3b747d8a58d99a5e8f8760bc677a236cc`  
		Last Modified: Tue, 01 Jul 2025 03:26:30 GMT  
		Size: 577.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e3207021f7ac1e05d59e7ca40914478a592e262465303702808d1d2a52103a4`  
		Last Modified: Tue, 01 Jul 2025 03:26:30 GMT  
		Size: 904.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a0dad15ae075f02014d5b12a3bf6e792bbd8974ad9c1b964311a0d6e1e6df6`  
		Last Modified: Tue, 01 Jul 2025 03:26:30 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e289696d9e3d15d60d3a21b4eed5e1610c9ab2fd373fe623c2cd2c6190a4c3ca`  
		Last Modified: Tue, 01 Jul 2025 03:26:30 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c2a4fac87e9ac4c1be99be3e6b4f8c303247c77844d14ed4fa40dbcfcff3914`  
		Last Modified: Tue, 01 Jul 2025 03:26:44 GMT  
		Size: 93.2 MB (93229770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mediawiki:lts` - unknown; unknown

```console
$ docker pull mediawiki@sha256:d768bff7bf11e3cc687ae3c550a86a70d5f214072820b42b6f85e50bd5f62426
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 KB (49399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2d1e2f69f64c90388f52d0b44db8177aa77a8eb0945d0a6ccbfe11f1c25ed43`

```dockerfile
```

-	Layers:
	-	`sha256:2851cfad0cc147f015cbfd338d9dcc89652cf6c1cc60f1bec7531dfc8ff378d2`  
		Last Modified: Tue, 01 Jul 2025 06:17:24 GMT  
		Size: 49.4 KB (49399 bytes)  
		MIME: application/vnd.in-toto+json

### `mediawiki:lts` - linux; arm variant v5

```console
$ docker pull mediawiki@sha256:c2c3bfc75365c9a66a68c1175584e18b28d0f3aeba55edd3209362907a4890a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.6 MB (293571114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c4b6da95e48cdde84b6111fd7585f5bbd7ef9b6b6e37dea636ea7561a3e2f79`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 10 Apr 2025 18:10:22 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1751241600'
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 10 Apr 2025 18:10:22 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 10 Apr 2025 18:10:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 10 Apr 2025 18:10:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 10 Apr 2025 18:10:22 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Thu, 10 Apr 2025 18:10:22 GMT
ENV PHP_VERSION=8.1.32
# Thu, 10 Apr 2025 18:10:22 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.32.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.32.tar.xz.asc
# Thu, 10 Apr 2025 18:10:22 GMT
ENV PHP_SHA256=c582ac682a280bbc69bc2186c21eb7e3313cc73099be61a6bc1d2cd337cbf383
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 10 Apr 2025 18:10:22 GMT
STOPSIGNAL SIGWINCH
# Thu, 10 Apr 2025 18:10:22 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
WORKDIR /var/www/html
# Thu, 10 Apr 2025 18:10:22 GMT
EXPOSE map[80/tcp:{}]
# Thu, 10 Apr 2025 18:10:22 GMT
CMD ["apache2-foreground"]
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 		apt-get update; 	apt-get install -y --no-install-recommends 		git 		librsvg2-bin 		imagemagick 		python3 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libicu-dev 		libonig-dev 		liblua5.1-0-dev 	; 		docker-php-ext-install -j "$(nproc)" 		calendar 		intl 		mbstring 		mysqli 		opcache 	; 		pecl install APCu-5.1.24; 	pecl install LuaSandbox-4.1.2; 	docker-php-ext-enable 		apcu 		luasandbox 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 	a2enmod rewrite; 	{ 		echo "<Directory /var/www/html>"; 		echo "  RewriteEngine On"; 		echo "  RewriteCond %{REQUEST_FILENAME} !-f"; 		echo "  RewriteCond %{REQUEST_FILENAME} !-d"; 		echo "  RewriteRule ^ %{DOCUMENT_ROOT}/index.php [L]"; 		echo "</Directory>"; 	} > "$APACHE_CONFDIR/conf-available/short-url.conf"; 	a2enconf short-url # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
RUN sed -i "s/<\/VirtualHost>/\tAllowEncodedSlashes NoDecode\n<\/VirtualHost>/" "$APACHE_CONFDIR/sites-available/000-default.conf" # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 	mkdir -p /var/www/data; 	chown -R www-data:www-data /var/www/data # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
ENV MEDIAWIKI_MAJOR_VERSION=1.43
# Thu, 10 Apr 2025 18:10:22 GMT
ENV MEDIAWIKI_VERSION=1.43.1
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 	fetchDeps=" 		gnupg 		dirmngr 	"; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 		curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz" -o mediawiki.tar.gz; 	curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz.sig" -o mediawiki.tar.gz.sig; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 		D7D6767D135A514BEB86E9BA75682B08E8A3FEC4 		441276E9CCD15F44F6D97D18C119E1A64D70938E 		F7F780D82EBFB8A56556E7EE82403E59F9F8CD79 		1D98867E82982C8FE0ABC25F9B69B3109D3BB7B0 		E059C034E7A430583C252F4AA8F734246D73B586 	; 	gpg --batch --verify mediawiki.tar.gz.sig mediawiki.tar.gz; 	tar -x --strip-components=1 -f mediawiki.tar.gz; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" mediawiki.tar.gz.sig mediawiki.tar.gz; 	chown -R www-data:www-data extensions skins cache images; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
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
	-	`sha256:780cba89858c1a34fe4e74d9063257d9e4c9441978133dc8eb13d9b4d535d7e1`  
		Last Modified: Tue, 01 Jul 2025 04:19:56 GMT  
		Size: 12.0 MB (12020461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:383768e37d11b94273d6e55d827ae3c91e8ba000a409819fc035fc22526d26ec`  
		Last Modified: Tue, 01 Jul 2025 04:19:54 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d25ab8c7e98d20f648852f0ab07763823924aa20637ef0f9edee2599c14d8932`  
		Last Modified: Tue, 01 Jul 2025 04:19:55 GMT  
		Size: 10.1 MB (10119154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ae6744e97fafae8478bbc8f40bd763ff0459f4cd116dbde407862045d8cbd42`  
		Last Modified: Tue, 01 Jul 2025 04:19:54 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b181808f923a46ad87351c44b7c83db6f793dae6648a9dc79162f354d5d3da7`  
		Last Modified: Tue, 01 Jul 2025 04:19:54 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c23e55cb39696b349df339353ad028786baaa51baf5061c3513b852ab2a7c7d`  
		Last Modified: Tue, 01 Jul 2025 04:19:54 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1a8e9da41ad46efe370ef4cc8bbd8800c7747429ed02f5d4d875d666dc84257`  
		Last Modified: Tue, 01 Jul 2025 04:19:54 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e457b0cb8a7e007ec75cc565c8d3fe81a9b65cf7941cb123742e07903283278a`  
		Last Modified: Tue, 01 Jul 2025 10:22:56 GMT  
		Size: 49.4 MB (49412346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d93b26313d096408db50e3a8787cefcaca744834619dbffb6fa06a1b9facd4b1`  
		Last Modified: Tue, 01 Jul 2025 10:22:55 GMT  
		Size: 1.6 MB (1632465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:893cafa13479b5d4a744d1c02fed0a9425bd25f9b87aa2bbe766e0296e69deaa`  
		Last Modified: Tue, 01 Jul 2025 10:22:54 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6333252b64937de3c5def4cf183fbf44e1efcd892ee4d1fefb05bd97f2c63f3f`  
		Last Modified: Tue, 01 Jul 2025 10:22:55 GMT  
		Size: 905.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47c6868dac6633d1bfea1788df4b0973248951c8daccb96469786a220e638bae`  
		Last Modified: Tue, 01 Jul 2025 10:22:55 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b57df9cdf207cf0babd6938e9dd618a9352358aca6f5a1cf1ca8db419c1d6209`  
		Last Modified: Tue, 01 Jul 2025 10:22:55 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15b67d3c682fe51300e57cc7235a0bb53c8133a381e8669daf72a1762bac3625`  
		Last Modified: Tue, 01 Jul 2025 10:23:02 GMT  
		Size: 93.2 MB (93224793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mediawiki:lts` - unknown; unknown

```console
$ docker pull mediawiki@sha256:f7857257039a196327c7c7439e4745d5df12751555c346e0c455e0f21dbcf70b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 KB (49553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0237a31331ccf09c92fea75e59f306fbae76fe982f911cbe236ce1642ec9fea4`

```dockerfile
```

-	Layers:
	-	`sha256:0a18349a3ebdf7f1535e775ea50c2449a8fbbc9df7588dc5046e9c5628e76047`  
		Last Modified: Tue, 01 Jul 2025 12:17:07 GMT  
		Size: 49.6 KB (49553 bytes)  
		MIME: application/vnd.in-toto+json

### `mediawiki:lts` - linux; arm variant v7

```console
$ docker pull mediawiki@sha256:3f0e609d215961442f1cd5712d3d69088c9842f25f5a3cb6c7966582722f34c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.4 MB (281350192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:367b18cf9d914ed34b6094efb72ba37143d4c701e241553b83f5cd4679120d1d`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 10 Apr 2025 18:10:22 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1751241600'
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 10 Apr 2025 18:10:22 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 10 Apr 2025 18:10:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 10 Apr 2025 18:10:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 10 Apr 2025 18:10:22 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Thu, 10 Apr 2025 18:10:22 GMT
ENV PHP_VERSION=8.1.32
# Thu, 10 Apr 2025 18:10:22 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.32.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.32.tar.xz.asc
# Thu, 10 Apr 2025 18:10:22 GMT
ENV PHP_SHA256=c582ac682a280bbc69bc2186c21eb7e3313cc73099be61a6bc1d2cd337cbf383
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 10 Apr 2025 18:10:22 GMT
STOPSIGNAL SIGWINCH
# Thu, 10 Apr 2025 18:10:22 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
WORKDIR /var/www/html
# Thu, 10 Apr 2025 18:10:22 GMT
EXPOSE map[80/tcp:{}]
# Thu, 10 Apr 2025 18:10:22 GMT
CMD ["apache2-foreground"]
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 		apt-get update; 	apt-get install -y --no-install-recommends 		git 		librsvg2-bin 		imagemagick 		python3 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libicu-dev 		libonig-dev 		liblua5.1-0-dev 	; 		docker-php-ext-install -j "$(nproc)" 		calendar 		intl 		mbstring 		mysqli 		opcache 	; 		pecl install APCu-5.1.24; 	pecl install LuaSandbox-4.1.2; 	docker-php-ext-enable 		apcu 		luasandbox 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 	a2enmod rewrite; 	{ 		echo "<Directory /var/www/html>"; 		echo "  RewriteEngine On"; 		echo "  RewriteCond %{REQUEST_FILENAME} !-f"; 		echo "  RewriteCond %{REQUEST_FILENAME} !-d"; 		echo "  RewriteRule ^ %{DOCUMENT_ROOT}/index.php [L]"; 		echo "</Directory>"; 	} > "$APACHE_CONFDIR/conf-available/short-url.conf"; 	a2enconf short-url # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
RUN sed -i "s/<\/VirtualHost>/\tAllowEncodedSlashes NoDecode\n<\/VirtualHost>/" "$APACHE_CONFDIR/sites-available/000-default.conf" # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 	mkdir -p /var/www/data; 	chown -R www-data:www-data /var/www/data # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
ENV MEDIAWIKI_MAJOR_VERSION=1.43
# Thu, 10 Apr 2025 18:10:22 GMT
ENV MEDIAWIKI_VERSION=1.43.1
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 	fetchDeps=" 		gnupg 		dirmngr 	"; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 		curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz" -o mediawiki.tar.gz; 	curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz.sig" -o mediawiki.tar.gz.sig; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 		D7D6767D135A514BEB86E9BA75682B08E8A3FEC4 		441276E9CCD15F44F6D97D18C119E1A64D70938E 		F7F780D82EBFB8A56556E7EE82403E59F9F8CD79 		1D98867E82982C8FE0ABC25F9B69B3109D3BB7B0 		E059C034E7A430583C252F4AA8F734246D73B586 	; 	gpg --batch --verify mediawiki.tar.gz.sig mediawiki.tar.gz; 	tar -x --strip-components=1 -f mediawiki.tar.gz; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" mediawiki.tar.gz.sig mediawiki.tar.gz; 	chown -R www-data:www-data extensions skins cache images; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
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
	-	`sha256:a06be49c2e7b18b404ff775e62c49998d62231d62660988faf65f345f34ab735`  
		Last Modified: Tue, 01 Jul 2025 19:54:51 GMT  
		Size: 93.2 MB (93225146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mediawiki:lts` - unknown; unknown

```console
$ docker pull mediawiki@sha256:1741b759250f456f1926af14308e3e07b7bd5d023830bd50268bdef0143b18a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 KB (49545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1693b887d590afc10a0bc3c0248fbfcfe13d1c28a11b5f54d7f5a666e5805948`

```dockerfile
```

-	Layers:
	-	`sha256:d75ed5784631556f13c5854a4c1a760348a9378db2649c552a49b60a9dcf6a0c`  
		Last Modified: Tue, 01 Jul 2025 21:17:04 GMT  
		Size: 49.5 KB (49545 bytes)  
		MIME: application/vnd.in-toto+json

### `mediawiki:lts` - linux; arm64 variant v8

```console
$ docker pull mediawiki@sha256:cf8853d87f5d102fafa472aa9a7a35c9eabd17d4a0824d5792842d4ceccf58d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.2 MB (316216119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f13032c9a4ef69a2e903cddc9c0c3fe5490ad8f4ac8bd4baab625f7eadee7e1`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 10 Apr 2025 18:10:22 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 10 Apr 2025 18:10:22 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 10 Apr 2025 18:10:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 10 Apr 2025 18:10:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 10 Apr 2025 18:10:22 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Thu, 10 Apr 2025 18:10:22 GMT
ENV PHP_VERSION=8.1.32
# Thu, 10 Apr 2025 18:10:22 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.32.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.32.tar.xz.asc
# Thu, 10 Apr 2025 18:10:22 GMT
ENV PHP_SHA256=c582ac682a280bbc69bc2186c21eb7e3313cc73099be61a6bc1d2cd337cbf383
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 10 Apr 2025 18:10:22 GMT
STOPSIGNAL SIGWINCH
# Thu, 10 Apr 2025 18:10:22 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
WORKDIR /var/www/html
# Thu, 10 Apr 2025 18:10:22 GMT
EXPOSE map[80/tcp:{}]
# Thu, 10 Apr 2025 18:10:22 GMT
CMD ["apache2-foreground"]
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 		apt-get update; 	apt-get install -y --no-install-recommends 		git 		librsvg2-bin 		imagemagick 		python3 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libicu-dev 		libonig-dev 		liblua5.1-0-dev 	; 		docker-php-ext-install -j "$(nproc)" 		calendar 		intl 		mbstring 		mysqli 		opcache 	; 		pecl install APCu-5.1.24; 	pecl install LuaSandbox-4.1.2; 	docker-php-ext-enable 		apcu 		luasandbox 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 	a2enmod rewrite; 	{ 		echo "<Directory /var/www/html>"; 		echo "  RewriteEngine On"; 		echo "  RewriteCond %{REQUEST_FILENAME} !-f"; 		echo "  RewriteCond %{REQUEST_FILENAME} !-d"; 		echo "  RewriteRule ^ %{DOCUMENT_ROOT}/index.php [L]"; 		echo "</Directory>"; 	} > "$APACHE_CONFDIR/conf-available/short-url.conf"; 	a2enconf short-url # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
RUN sed -i "s/<\/VirtualHost>/\tAllowEncodedSlashes NoDecode\n<\/VirtualHost>/" "$APACHE_CONFDIR/sites-available/000-default.conf" # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 	mkdir -p /var/www/data; 	chown -R www-data:www-data /var/www/data # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
ENV MEDIAWIKI_MAJOR_VERSION=1.43
# Thu, 10 Apr 2025 18:10:22 GMT
ENV MEDIAWIKI_VERSION=1.43.1
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 	fetchDeps=" 		gnupg 		dirmngr 	"; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 		curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz" -o mediawiki.tar.gz; 	curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz.sig" -o mediawiki.tar.gz.sig; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 		D7D6767D135A514BEB86E9BA75682B08E8A3FEC4 		441276E9CCD15F44F6D97D18C119E1A64D70938E 		F7F780D82EBFB8A56556E7EE82403E59F9F8CD79 		1D98867E82982C8FE0ABC25F9B69B3109D3BB7B0 		E059C034E7A430583C252F4AA8F734246D73B586 	; 	gpg --batch --verify mediawiki.tar.gz.sig mediawiki.tar.gz; 	tar -x --strip-components=1 -f mediawiki.tar.gz; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" mediawiki.tar.gz.sig mediawiki.tar.gz; 	chown -R www-data:www-data extensions skins cache images; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
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
	-	`sha256:6cf115f1691a033d055bf769db7c8d7d870a290cb226208e88664285d128b1db`  
		Last Modified: Tue, 01 Jul 2025 15:19:11 GMT  
		Size: 51.1 MB (51096006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f71faa2ee56662b129f856876295d0274df79edfc90497ea2f4c4edc2359a2b`  
		Last Modified: Tue, 01 Jul 2025 15:18:56 GMT  
		Size: 2.3 MB (2337054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0694242b60264dc441df7ccdbd9adfc30ad2fcc32b20ad517b8c3af83caeede3`  
		Last Modified: Tue, 01 Jul 2025 15:18:56 GMT  
		Size: 576.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae84cdda95100f1e5760f75a8268325a8e46b178e327e95192d1d70b1a44d7c0`  
		Last Modified: Tue, 01 Jul 2025 15:18:56 GMT  
		Size: 905.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28aefabe29160e14bb9c7940c05d89c726c2aa78609cc758952294b0185dc3e7`  
		Last Modified: Tue, 01 Jul 2025 15:18:56 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7dd03afe92c5c541600422883d1ac98e5b81d035a95aeccc8c13ab546bdd69a`  
		Last Modified: Tue, 01 Jul 2025 15:18:56 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a56fede3cf0d69ae1597d7d0137381577871aa4f1cd19b06db26c876cd2ec22b`  
		Last Modified: Tue, 01 Jul 2025 15:19:06 GMT  
		Size: 93.2 MB (93229970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mediawiki:lts` - unknown; unknown

```console
$ docker pull mediawiki@sha256:80b23432dd3617c2aec2d6f345143f6f88379cce7b757e47c84a77730c260118
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 KB (49597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dff3d2eef78ea90547b7e42b872b13b26f013eed27f87d3d5a89047a1cf2be63`

```dockerfile
```

-	Layers:
	-	`sha256:c5067c25143d2150c93e484d366455f9d320256414a71035109a433edd43b1dc`  
		Last Modified: Tue, 01 Jul 2025 18:17:06 GMT  
		Size: 49.6 KB (49597 bytes)  
		MIME: application/vnd.in-toto+json

### `mediawiki:lts` - linux; 386

```console
$ docker pull mediawiki@sha256:5f4d6e7ef01047b585a1284be6e01cde805eb504b0cabf745901712fbb962ff6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.5 MB (325517367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20add654971ec98a2b6e193b4345c25588af289e5da45ef2b4a464b4a224110d`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 10 Apr 2025 18:10:22 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1751241600'
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 10 Apr 2025 18:10:22 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 10 Apr 2025 18:10:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 10 Apr 2025 18:10:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 10 Apr 2025 18:10:22 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Thu, 10 Apr 2025 18:10:22 GMT
ENV PHP_VERSION=8.1.32
# Thu, 10 Apr 2025 18:10:22 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.32.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.32.tar.xz.asc
# Thu, 10 Apr 2025 18:10:22 GMT
ENV PHP_SHA256=c582ac682a280bbc69bc2186c21eb7e3313cc73099be61a6bc1d2cd337cbf383
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 10 Apr 2025 18:10:22 GMT
STOPSIGNAL SIGWINCH
# Thu, 10 Apr 2025 18:10:22 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
WORKDIR /var/www/html
# Thu, 10 Apr 2025 18:10:22 GMT
EXPOSE map[80/tcp:{}]
# Thu, 10 Apr 2025 18:10:22 GMT
CMD ["apache2-foreground"]
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 		apt-get update; 	apt-get install -y --no-install-recommends 		git 		librsvg2-bin 		imagemagick 		python3 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libicu-dev 		libonig-dev 		liblua5.1-0-dev 	; 		docker-php-ext-install -j "$(nproc)" 		calendar 		intl 		mbstring 		mysqli 		opcache 	; 		pecl install APCu-5.1.24; 	pecl install LuaSandbox-4.1.2; 	docker-php-ext-enable 		apcu 		luasandbox 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 	a2enmod rewrite; 	{ 		echo "<Directory /var/www/html>"; 		echo "  RewriteEngine On"; 		echo "  RewriteCond %{REQUEST_FILENAME} !-f"; 		echo "  RewriteCond %{REQUEST_FILENAME} !-d"; 		echo "  RewriteRule ^ %{DOCUMENT_ROOT}/index.php [L]"; 		echo "</Directory>"; 	} > "$APACHE_CONFDIR/conf-available/short-url.conf"; 	a2enconf short-url # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
RUN sed -i "s/<\/VirtualHost>/\tAllowEncodedSlashes NoDecode\n<\/VirtualHost>/" "$APACHE_CONFDIR/sites-available/000-default.conf" # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 	mkdir -p /var/www/data; 	chown -R www-data:www-data /var/www/data # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
ENV MEDIAWIKI_MAJOR_VERSION=1.43
# Thu, 10 Apr 2025 18:10:22 GMT
ENV MEDIAWIKI_VERSION=1.43.1
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 	fetchDeps=" 		gnupg 		dirmngr 	"; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 		curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz" -o mediawiki.tar.gz; 	curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz.sig" -o mediawiki.tar.gz.sig; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 		D7D6767D135A514BEB86E9BA75682B08E8A3FEC4 		441276E9CCD15F44F6D97D18C119E1A64D70938E 		F7F780D82EBFB8A56556E7EE82403E59F9F8CD79 		1D98867E82982C8FE0ABC25F9B69B3109D3BB7B0 		E059C034E7A430583C252F4AA8F734246D73B586 	; 	gpg --batch --verify mediawiki.tar.gz.sig mediawiki.tar.gz; 	tar -x --strip-components=1 -f mediawiki.tar.gz; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" mediawiki.tar.gz.sig mediawiki.tar.gz; 	chown -R www-data:www-data extensions skins cache images; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:88e96ee0cb4c7106f4d6a5cdeaeb171ec22a2484245e406cb5267b2be095937c`  
		Last Modified: Tue, 01 Jul 2025 01:14:33 GMT  
		Size: 29.2 MB (29212432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28f0cbfe5341a865f21dcaf5419ee08b3494a79998ccfe82b482d2f094f2a08a`  
		Last Modified: Tue, 01 Jul 2025 02:24:53 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:231f9c7e12b760e3639fa9e8a1326e592579781aaa352373eb70c53d62771306`  
		Last Modified: Tue, 01 Jul 2025 02:25:01 GMT  
		Size: 101.5 MB (101515209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74815ec74a0322a3f42f4ad1f00dc43c4e4c2680eb2b7309df0cc5f1ac317423`  
		Last Modified: Tue, 01 Jul 2025 02:24:53 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:154f386e0b62be11ca48e49355723ee13d81029e5f4d0cafed46333b8adf3cb7`  
		Last Modified: Tue, 01 Jul 2025 02:24:54 GMT  
		Size: 20.6 MB (20638487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50e9a852850b9e016a087b2fcc7d8775f6bba960a7b295a46100a83973fd0d9f`  
		Last Modified: Tue, 01 Jul 2025 02:24:53 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20562b5d3fd60c4119fbbf656172017d63f8ec2046b2b931d9ef48312ac2b7bf`  
		Last Modified: Tue, 01 Jul 2025 02:24:53 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48890a5a376e41016076ea2cf645d53951aa7fdf9540e7f6ac646394febb71f9`  
		Last Modified: Tue, 01 Jul 2025 02:24:57 GMT  
		Size: 12.0 MB (12021384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4799ce35139589473a392ee8a8cd6983929e633ecde1e02da35da59745a3ac7e`  
		Last Modified: Tue, 01 Jul 2025 02:24:53 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b88a0c5a9fc43c8c5dc32cba28cad3b4fca94232fb9c2b7625cccf4ecfbca01e`  
		Last Modified: Tue, 01 Jul 2025 02:24:54 GMT  
		Size: 11.4 MB (11384090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c845e9525ef0bad6a3026a440252648c64aee3664080f584dd2506cb0720752`  
		Last Modified: Tue, 01 Jul 2025 02:24:53 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba4fa8e112687638a2cab20185313a9fcbd653ae50574cd5ee024a4526bc410c`  
		Last Modified: Tue, 01 Jul 2025 02:24:57 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ea6f92f08603db1f8ef940c2c778b64fca7407f6b3b07445a0599c5aa1e059b`  
		Last Modified: Tue, 01 Jul 2025 02:24:57 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b68f3d9a4d9af65546a52e0bc0f0a0c1a59c5edd53198039f090d39e7f9af6c1`  
		Last Modified: Tue, 01 Jul 2025 02:24:56 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9509060468f893d1113cd7da8ed626e7dfcf2d44b24d6f99f7da9a68fab8920b`  
		Last Modified: Tue, 01 Jul 2025 03:25:17 GMT  
		Size: 55.4 MB (55430342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9434bf2cc2f1688abe49e3e63fe2b81b2de9e30a2bc425f82696b149dca8cd5`  
		Last Modified: Tue, 01 Jul 2025 03:25:14 GMT  
		Size: 2.1 MB (2080122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e102980f578c44c6d79c8568474180b103ace86e669d073ccbf91b88a66b3b8d`  
		Last Modified: Tue, 01 Jul 2025 03:25:13 GMT  
		Size: 574.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32d9ca238073d68d18cfa1de7ed529ac6a7e604a1379d3a5ecd6e88d732091b3`  
		Last Modified: Tue, 01 Jul 2025 03:25:13 GMT  
		Size: 902.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d755104c3cb0451858858c636aa40194bd5396532c168b97d81e4748e93474d`  
		Last Modified: Tue, 01 Jul 2025 03:25:13 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:937073689d5949034776d32a74ad4ee4090eb6710470b2bc90f7d8e766efe793`  
		Last Modified: Tue, 01 Jul 2025 03:25:14 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6631d8ed8d85ac413d4a94ecf60bd6fdfcf5ab75f630ba4d7742aa6fc76f487`  
		Last Modified: Tue, 01 Jul 2025 03:25:24 GMT  
		Size: 93.2 MB (93227650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mediawiki:lts` - unknown; unknown

```console
$ docker pull mediawiki@sha256:7ae0df529eddda9da36b07b6a8f39612bb06cf1a59cdca2040978be4d0ac84d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 KB (49350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07fdcd3cdaf79fc101537d6cffa5fc1dc566d797ee7f1d239420a358e4245b17`

```dockerfile
```

-	Layers:
	-	`sha256:3babbb35a55df35924cc53186def3e7c2d93cbca874581d49e7ce0c173dbaaba`  
		Last Modified: Tue, 01 Jul 2025 06:17:36 GMT  
		Size: 49.4 KB (49350 bytes)  
		MIME: application/vnd.in-toto+json

### `mediawiki:lts` - linux; ppc64le

```console
$ docker pull mediawiki@sha256:2057baeb186a38e820ac8f1decabe3844d6350ef55063d1f276ff4a545aae87e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **333.4 MB (333410548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5e77a1a5fb526356f4cd2401a6c7e6c480c33885c6f5be003ba6351cc00589a`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 10 Apr 2025 18:10:22 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1751241600'
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 10 Apr 2025 18:10:22 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 10 Apr 2025 18:10:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 10 Apr 2025 18:10:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 10 Apr 2025 18:10:22 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Thu, 10 Apr 2025 18:10:22 GMT
ENV PHP_VERSION=8.1.32
# Thu, 10 Apr 2025 18:10:22 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.32.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.32.tar.xz.asc
# Thu, 10 Apr 2025 18:10:22 GMT
ENV PHP_SHA256=c582ac682a280bbc69bc2186c21eb7e3313cc73099be61a6bc1d2cd337cbf383
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 10 Apr 2025 18:10:22 GMT
STOPSIGNAL SIGWINCH
# Thu, 10 Apr 2025 18:10:22 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
WORKDIR /var/www/html
# Thu, 10 Apr 2025 18:10:22 GMT
EXPOSE map[80/tcp:{}]
# Thu, 10 Apr 2025 18:10:22 GMT
CMD ["apache2-foreground"]
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 		apt-get update; 	apt-get install -y --no-install-recommends 		git 		librsvg2-bin 		imagemagick 		python3 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libicu-dev 		libonig-dev 		liblua5.1-0-dev 	; 		docker-php-ext-install -j "$(nproc)" 		calendar 		intl 		mbstring 		mysqli 		opcache 	; 		pecl install APCu-5.1.24; 	pecl install LuaSandbox-4.1.2; 	docker-php-ext-enable 		apcu 		luasandbox 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 	a2enmod rewrite; 	{ 		echo "<Directory /var/www/html>"; 		echo "  RewriteEngine On"; 		echo "  RewriteCond %{REQUEST_FILENAME} !-f"; 		echo "  RewriteCond %{REQUEST_FILENAME} !-d"; 		echo "  RewriteRule ^ %{DOCUMENT_ROOT}/index.php [L]"; 		echo "</Directory>"; 	} > "$APACHE_CONFDIR/conf-available/short-url.conf"; 	a2enconf short-url # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
RUN sed -i "s/<\/VirtualHost>/\tAllowEncodedSlashes NoDecode\n<\/VirtualHost>/" "$APACHE_CONFDIR/sites-available/000-default.conf" # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 	mkdir -p /var/www/data; 	chown -R www-data:www-data /var/www/data # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
ENV MEDIAWIKI_MAJOR_VERSION=1.43
# Thu, 10 Apr 2025 18:10:22 GMT
ENV MEDIAWIKI_VERSION=1.43.1
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 	fetchDeps=" 		gnupg 		dirmngr 	"; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 		curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz" -o mediawiki.tar.gz; 	curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz.sig" -o mediawiki.tar.gz.sig; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 		D7D6767D135A514BEB86E9BA75682B08E8A3FEC4 		441276E9CCD15F44F6D97D18C119E1A64D70938E 		F7F780D82EBFB8A56556E7EE82403E59F9F8CD79 		1D98867E82982C8FE0ABC25F9B69B3109D3BB7B0 		E059C034E7A430583C252F4AA8F734246D73B586 	; 	gpg --batch --verify mediawiki.tar.gz.sig mediawiki.tar.gz; 	tar -x --strip-components=1 -f mediawiki.tar.gz; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" mediawiki.tar.gz.sig mediawiki.tar.gz; 	chown -R www-data:www-data extensions skins cache images; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:c5884d20b08634214a92bd5de559876bf30e6c5453807c3014f5480eeba20662`  
		Last Modified: Tue, 01 Jul 2025 01:15:20 GMT  
		Size: 32.1 MB (32072820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceff3d73088eb90a29a3888d344cedd86858df29b36df7932d3fe0d16eda4e7d`  
		Last Modified: Tue, 01 Jul 2025 02:58:07 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08259e2c7cacc0405f0da4ea7142f0be36234c1b63d584779538944c8319235f`  
		Last Modified: Tue, 01 Jul 2025 02:58:21 GMT  
		Size: 103.3 MB (103326709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2fcb5df575fa0806e458d09147e66250dc80c744fe65c46881d5d2395c98374`  
		Last Modified: Tue, 01 Jul 2025 02:58:07 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4ed49ba7119690733e3d6ea549f616e27a3c2373536949c5f815f3016ee36d7`  
		Last Modified: Tue, 01 Jul 2025 03:02:55 GMT  
		Size: 21.3 MB (21308312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:479685b6a0f37fa82ae54089bd94827adabd1a9762de07bf56c1d446529ccf77`  
		Last Modified: Tue, 01 Jul 2025 03:02:53 GMT  
		Size: 436.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bf6d05d1ea304b3577242e86313ab57d4487f5a6b60d212401488afbc705451`  
		Last Modified: Tue, 01 Jul 2025 03:02:54 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55c09437723243328c332b2f7572b4de0e98a0143027bbe2c9238f1acd48e135`  
		Last Modified: Tue, 01 Jul 2025 04:20:35 GMT  
		Size: 12.0 MB (12021812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b93173a0a53d84e4fba2747ad4e5bef9eb552b8c17e44fc0f3aafb92322a543`  
		Last Modified: Tue, 01 Jul 2025 04:20:34 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:247e143c15c69791fb8918b79fdb638b619205d9f1ec597460b94990cb79e5ed`  
		Last Modified: Tue, 01 Jul 2025 04:20:35 GMT  
		Size: 11.5 MB (11529874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:812de45984de3786c0a514ddfa5c9432d5448600ab716cc184293bfd465f5821`  
		Last Modified: Tue, 01 Jul 2025 04:20:34 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee2e3246960573e15c2c4d6b104af1eb8dd5e4dc9a0c278339e9fa6139ceb539`  
		Last Modified: Tue, 01 Jul 2025 04:20:34 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:851be740bb7aef17c807447dfd10a78e17ddd4db7cca8dac2f1033d3d3b43a8c`  
		Last Modified: Tue, 01 Jul 2025 04:20:34 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0bbcb992d280187c8971c93932c711b2b91e18420622bf32c0f255a2782feef`  
		Last Modified: Tue, 01 Jul 2025 04:20:34 GMT  
		Size: 887.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b15f1ba3cf5cf4471bcfc47f594c5401aaf591667759a7c27d0217a6cad5088b`  
		Last Modified: Tue, 01 Jul 2025 12:41:05 GMT  
		Size: 58.1 MB (58103806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfd030b0e4a0890c44d71acf44f9ff4911a13a1927ad908c0e3a98d3b27dc9f9`  
		Last Modified: Tue, 01 Jul 2025 12:40:57 GMT  
		Size: 1.8 MB (1809826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:700bba8f333fa38ab7116aa471e04c04c419d799ac3b75d3ac435779561f91ea`  
		Last Modified: Tue, 01 Jul 2025 12:40:57 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9bfc1a416a0714befdbb069b9b9648ec01b2093d9e34eb9e3a650cd44495753`  
		Last Modified: Tue, 01 Jul 2025 12:40:56 GMT  
		Size: 905.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d5c58665b1046bda9a01ff7b326842b0db8a093b496ce63619ffe88b15003be`  
		Last Modified: Tue, 01 Jul 2025 12:40:56 GMT  
		Size: 309.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d87463e9a47569c68fadbefe80b5b248485de07ca245506586ec728bba785eb`  
		Last Modified: Tue, 01 Jul 2025 12:40:57 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de522f7dfb917d801e0bdf4b8c2a65942a5f12c22a456d15a02bcb39cea9847e`  
		Last Modified: Tue, 01 Jul 2025 12:41:09 GMT  
		Size: 93.2 MB (93229740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mediawiki:lts` - unknown; unknown

```console
$ docker pull mediawiki@sha256:033799c57a85e5bb014b321cd7a2ab33c3ffb4fd50a3ef211170187974762cab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 KB (49461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d934930d04bc4afdf4996f19d679d29559706cf40e4deceb16da82fbdb7cde6`

```dockerfile
```

-	Layers:
	-	`sha256:5fed104952d8282e66bfc8a45c84b5a416267c96d43b3d393d8677d797b8e0c3`  
		Last Modified: Tue, 01 Jul 2025 15:17:09 GMT  
		Size: 49.5 KB (49461 bytes)  
		MIME: application/vnd.in-toto+json
