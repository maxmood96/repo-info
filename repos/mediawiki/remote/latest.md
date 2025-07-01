## `mediawiki:latest`

```console
$ docker pull mediawiki@sha256:7af26616f8204961850e9036dbcfa7388f1a604f8bcd9a90863e12fc548bf7d1
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

### `mediawiki:latest` - linux; amd64

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

### `mediawiki:latest` - unknown; unknown

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

### `mediawiki:latest` - linux; arm variant v5

```console
$ docker pull mediawiki@sha256:e2b885630c35e4ff84f3156f8540327dc723ef75eff90e81473a805fb553c5e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.6 MB (293569921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8004079b2e2088d4a4309dbbf8e8de4ed998673e008bfab60e0fb2ae017b4ab`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 10 Apr 2025 18:10:22 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1749513600'
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
	-	`sha256:750907abe8bb5d66304ed40261e1579b6575871f6848cfbd720888c20afd3b67`  
		Last Modified: Tue, 10 Jun 2025 22:47:31 GMT  
		Size: 25.8 MB (25762396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6a4bfa01c4278bce681525640ca665e4be1f8b06675ed34ca66730b92f9f234`  
		Last Modified: Wed, 11 Jun 2025 00:23:03 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:213535e381924aca2ea170c6d78dbba86bf653012096b96d22ac8636c2ac78b1`  
		Last Modified: Wed, 11 Jun 2025 00:23:08 GMT  
		Size: 82.0 MB (81970554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e73c797096a39ccf924b52255bfc0ffa99f5d43666673ad5a6492f079a9e1db0`  
		Last Modified: Wed, 11 Jun 2025 00:23:04 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7452f3df381859826ffc091392d386e53fba4bb0a453705af9b07499ef57813`  
		Last Modified: Wed, 11 Jun 2025 00:23:06 GMT  
		Size: 19.4 MB (19419490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02701d4843fe04a21f125f92ed80d6e697c8948b27ec9bc899ebde4a618d774d`  
		Last Modified: Wed, 11 Jun 2025 00:23:05 GMT  
		Size: 432.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fee0b1576994df154956fba912e1b433e031e5704c7161d7c1d0c490316fc5ed`  
		Last Modified: Wed, 11 Jun 2025 00:23:05 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a91fb67e321aa31f0d3c721225468da3f3027296a95ff05391ce5c0ad4303608`  
		Last Modified: Wed, 11 Jun 2025 01:23:07 GMT  
		Size: 12.0 MB (12020429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71944368069047a4e6bbe14ad0a3f754b2942d7b912f4c832af0131f6715d04d`  
		Last Modified: Wed, 11 Jun 2025 01:23:06 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:400e8af857d3b88d2119286fb4c9d74ee4defa33acaf59bd6a01c6506b9dac43`  
		Last Modified: Wed, 11 Jun 2025 01:23:07 GMT  
		Size: 10.1 MB (10119078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:191c2e2c47c8bc3ca9ad6b1ad56c845d5010139955c417e67a81eb06b1704b74`  
		Last Modified: Wed, 25 Jun 2025 19:33:28 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8d9009c8c32e25929af0ec2f9a305d8ea3247c451642f305488685f26c21e37`  
		Last Modified: Wed, 25 Jun 2025 19:33:31 GMT  
		Size: 253.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77d35d4e9c30057f2d45df4ef063fd68a289b4c12d9a9e07462c79866b3669b8`  
		Last Modified: Wed, 25 Jun 2025 19:33:35 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf604afb002c2c2d63a1637add8874088270a3cb7c808220556b311affa8a543`  
		Last Modified: Wed, 25 Jun 2025 19:33:38 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2df746572b0796ebd44560d79d2678c87f62d898293d9b06de340c21285a0ee`  
		Last Modified: Wed, 25 Jun 2025 21:23:32 GMT  
		Size: 49.4 MB (49412367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a3548f22ed31850f2f9392e1b9a6c79ab35c158bb2c0105f79496c16ac62d55`  
		Last Modified: Wed, 25 Jun 2025 21:23:28 GMT  
		Size: 1.6 MB (1632800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6256529ab05641c6d7683a650d6b81d25bf3b7d4a6ef22b73e8ec5c55ca8c30e`  
		Last Modified: Wed, 25 Jun 2025 21:23:28 GMT  
		Size: 576.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aca735816d2f83519a1dded7fef178322b8586df6cd45740571a55f6d61f4ff1`  
		Last Modified: Wed, 25 Jun 2025 21:23:29 GMT  
		Size: 902.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37845537e776f7befb1202aacebbbfd8a408c0730b8d9c5d50f3715350ac16bf`  
		Last Modified: Wed, 25 Jun 2025 21:23:30 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2bd9d7db76579e6d7a58f8bb6a63c792241051a7d3a3303408f20cf1c078aba`  
		Last Modified: Wed, 25 Jun 2025 21:23:30 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff0bc7fc8810ac46487da4386c139b38ffcc22865c4528ed337847279647aa52`  
		Last Modified: Wed, 25 Jun 2025 21:23:39 GMT  
		Size: 93.2 MB (93225141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mediawiki:latest` - unknown; unknown

```console
$ docker pull mediawiki@sha256:ecba7e226dae7ac9ef4c426620818f730cdbc33e522c74e7b557ae3e023ff339
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 KB (49553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c8bd9f7afd3ad3e5af2294eb57d2f650a175790a875d3b194812c5818008c7e`

```dockerfile
```

-	Layers:
	-	`sha256:3068f13b7f9e2b644314ffd337cdae05ddf0e247afbcbbe7ee89788418604759`  
		Last Modified: Thu, 26 Jun 2025 00:17:50 GMT  
		Size: 49.6 KB (49553 bytes)  
		MIME: application/vnd.in-toto+json

### `mediawiki:latest` - linux; arm variant v7

```console
$ docker pull mediawiki@sha256:2579129d1b0022a5a2fe6af1ad35c40aebde9bfce5622a2a920e1a69d17eb146
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.3 MB (281336090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5609beb9c6c1b77d0bc6e273b296f5dc46011fcec80da978026d7497eab6a460`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 10 Apr 2025 18:10:22 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1749513600'
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
	-	`sha256:2ef3992e7433479b3bc3925ed53605d8a67c047db4064f390ed72ce1c80eb7b1`  
		Last Modified: Wed, 11 Jun 2025 01:41:20 GMT  
		Size: 12.0 MB (12020454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9004d6ca50055284f6f9728a799a3e714f08c6307cc7b55b5f156039ae18b40c`  
		Last Modified: Wed, 11 Jun 2025 01:41:18 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7538e1571dc8865ca00aad965950fe9d568d7e53f4acc32afefdd7504712a07b`  
		Last Modified: Wed, 11 Jun 2025 01:41:23 GMT  
		Size: 9.6 MB (9584870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a44c98f8518962c9b50518c8d4c7414c78571e59ddf51a692b620dddc3423dd7`  
		Last Modified: Wed, 25 Jun 2025 20:36:09 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b06baab645baec38f31b045b5cebd1c08908365854d01bbd083bfd1f61834e5`  
		Last Modified: Wed, 25 Jun 2025 20:36:09 GMT  
		Size: 254.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a2a36845da8da5926bf6ab9435964c0b216e5499ff38eb8eff454b777d247a1`  
		Last Modified: Wed, 25 Jun 2025 20:36:10 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dcce065aed8d640401c3bff51a2c5479b5a6f831275ef09681e0ca0a099ad61`  
		Last Modified: Wed, 25 Jun 2025 20:36:10 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1de314ec961a4ab2fed307cf4429f85c3fc6fa42545170186775a3a3b1d7f29`  
		Last Modified: Wed, 25 Jun 2025 22:57:35 GMT  
		Size: 46.0 MB (45993688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:093630fb3c7985f7fbdecbdd8c5badf1ae937976e4dcafb68a0163ea5d3b3600`  
		Last Modified: Wed, 25 Jun 2025 22:57:32 GMT  
		Size: 1.6 MB (1574457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c88ed39d40c4bb35ce3f8fe7a9bfbfeba25f3d228cadcb350bac3f62d8d50715`  
		Last Modified: Wed, 25 Jun 2025 22:57:32 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae73f3358aff95ace04aa5dcd5df5a05371feda12cf96879a9d6e51cce90cbfd`  
		Last Modified: Wed, 25 Jun 2025 22:57:33 GMT  
		Size: 906.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8baf9d5c999a6f802f8aad2a6fe982a97b75c65522513eb9896aaa071a5d7fb7`  
		Last Modified: Wed, 25 Jun 2025 22:57:42 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2f39acc34010e80ed68cf3fbecca7be1af5c09a27a1c4722d6364b74c59e420`  
		Last Modified: Wed, 25 Jun 2025 22:57:43 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9c891f257b6f09b205e834c0643fd04c918beea2f652fad6362a8f4a7120c68`  
		Last Modified: Thu, 26 Jun 2025 00:18:16 GMT  
		Size: 93.2 MB (93225117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mediawiki:latest` - unknown; unknown

```console
$ docker pull mediawiki@sha256:6a8161c488174e294ca5e4100c4b97545d17da9c6e2af3697bffa90729558f9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 KB (49545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7920a122181e2467f6cd5999fa66ab73f44cd6e3f635bd8307bb79014c6ce06`

```dockerfile
```

-	Layers:
	-	`sha256:5d06e50c78d7303aaeadf39edef518675bcd1c2766d43e80c84ed1eb131e3b7b`  
		Last Modified: Thu, 26 Jun 2025 00:17:53 GMT  
		Size: 49.5 KB (49545 bytes)  
		MIME: application/vnd.in-toto+json

### `mediawiki:latest` - linux; arm64 variant v8

```console
$ docker pull mediawiki@sha256:e41d48aa3879913feb22a7e1b998c7c0488c2606a166043736e0e2c0cb2f10e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.0 MB (316967056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:017ee8a045f43d3fd7abfa587e30520262d21695057b1a52de87a760f8d5c0ef`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 10 Apr 2025 18:10:22 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
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
	-	`sha256:b08bf024847b0687b4eb460835b451eb576db026fd7523d0d41fba49a0f07cbe`  
		Last Modified: Wed, 25 Jun 2025 22:07:31 GMT  
		Size: 12.0 MB (12022171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78ced60c97fe16cb7bdc2ec6cfc7ec2281f384502d9fe225601312e476455632`  
		Last Modified: Wed, 25 Jun 2025 22:07:26 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f7f6fd7327020b1f45d8fb4e7d7235f50db536513f0afbe2ac54b713ff01976`  
		Last Modified: Wed, 25 Jun 2025 22:07:30 GMT  
		Size: 11.9 MB (11947567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e72bbf6f93a151714e9b12a257a946e1202c41d2aef8bcd70d171ac49a94ab06`  
		Last Modified: Wed, 25 Jun 2025 22:07:28 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b24a86e3a5e757447fecd3b78c796ef4bf661365f26ae6c027ce90adedc14c`  
		Last Modified: Wed, 25 Jun 2025 22:07:27 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d991ab92ebc61fcdac3d107fa366ac23441377a6e964797271a1c99f9b7993c`  
		Last Modified: Wed, 25 Jun 2025 22:07:27 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4a66d802ebad700fabc358af0c262a21995f2bfe97dac960eac6592eb6e1cac`  
		Last Modified: Wed, 25 Jun 2025 22:07:28 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56b2ee92d5462862cc3438146b915fee3edc13ce05b8ad71f55332ef502596a`  
		Last Modified: Thu, 26 Jun 2025 02:17:06 GMT  
		Size: 51.1 MB (51095988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9856740eea043df67ecd16031cede03d6707e85cca459f1cd09ec49c835edba9`  
		Last Modified: Thu, 26 Jun 2025 02:17:03 GMT  
		Size: 2.3 MB (2337122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:108bb046b70de548190bf6ab457d71335df138116ea976d9d150387ad85f974d`  
		Last Modified: Thu, 26 Jun 2025 02:17:03 GMT  
		Size: 576.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71bce6ac8c552c50e599b1045f682c38a4f4d3649eaa63942acd2a42a5f5a790`  
		Last Modified: Thu, 26 Jun 2025 02:17:03 GMT  
		Size: 904.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:538d505198fea81624f91f02fd95931b54371fd6b89d6b10c70678315f785be7`  
		Last Modified: Thu, 26 Jun 2025 02:17:03 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d1a1aa7b7de0046b514a61529c97d1c0f9d771da73b3ab967ec70ad5dc0b29a`  
		Last Modified: Thu, 26 Jun 2025 02:17:03 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:202330c824aba67856fe49e8e377da7a47a6501632b63c96df204c7918da074e`  
		Last Modified: Thu, 26 Jun 2025 02:17:09 GMT  
		Size: 93.2 MB (93229716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mediawiki:latest` - unknown; unknown

```console
$ docker pull mediawiki@sha256:ef84fd67010fd6333a2c0a3c4a80c33f0e4bdeb11c79f92e44b201aca2675370
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 KB (49596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e14b3665f79325af792145e3dc824416f6949ed4ef796e25b72038ff5d5745d1`

```dockerfile
```

-	Layers:
	-	`sha256:cb9bfac514e042a8cd65f7ac8c9b578a945d6fdea2e131072516c426ae7b47e5`  
		Last Modified: Thu, 26 Jun 2025 03:17:43 GMT  
		Size: 49.6 KB (49596 bytes)  
		MIME: application/vnd.in-toto+json

### `mediawiki:latest` - linux; 386

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

### `mediawiki:latest` - unknown; unknown

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

### `mediawiki:latest` - linux; ppc64le

```console
$ docker pull mediawiki@sha256:05014b4c3fff275b1e4179f21b8768442d4c550f4bb0f89d28e44f663ca117d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.3 MB (334323758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d9b9058ad6d6b4f3ffcc31963befa18a384fe359dd57d326732b72854013e4d`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 10 Apr 2025 18:10:22 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1749513600'
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
	-	`sha256:730da1d1736ccc2326da5cd7de01afa9a558996cd2dc50f7880f79cf78b341a0`  
		Last Modified: Thu, 26 Jun 2025 00:26:44 GMT  
		Size: 12.0 MB (12021837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e425bda9b85b706510f8f0904db348b1b5ba59a87b2754290e8ce4786042bd9`  
		Last Modified: Wed, 25 Jun 2025 21:08:24 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d97bcf7a61d5236babdace072143b08b2e3c3cfe77883fa788b89fc4d567664`  
		Last Modified: Thu, 26 Jun 2025 00:26:44 GMT  
		Size: 12.5 MB (12450786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ea960694a277ea2cdc2ac867249332c6c74d63e289f617b58fedd0f7fd75eb9`  
		Last Modified: Wed, 25 Jun 2025 21:08:27 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a0b904c9cbca32969151fb834b6f2b04153034fdf4b8855b086867a76899bec`  
		Last Modified: Wed, 25 Jun 2025 21:08:30 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcce5770f0517134f5ae327c5a6c17c5d81df212f148ca64251a970ff1b4c2c8`  
		Last Modified: Wed, 25 Jun 2025 21:08:33 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:930553ef1366afa4326e33df039696bef18f3b054cf4829e1e369a82175f0e78`  
		Last Modified: Wed, 25 Jun 2025 21:08:37 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d94b8c3179bcf6ea3df25a5c8ea5c8090d586467b6b823a4d4dca3dc148ad584`  
		Last Modified: Thu, 26 Jun 2025 00:47:11 GMT  
		Size: 58.1 MB (58104456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c4d3d3dad6add09d104b8207862c4122525929833a5835efceb4adba10e7b8b`  
		Last Modified: Thu, 26 Jun 2025 01:05:59 GMT  
		Size: 1.8 MB (1810029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a863058f42933c19114238c5f300f83d7580a0218b3faa18997c59455b226dc`  
		Last Modified: Thu, 26 Jun 2025 01:06:27 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:245f0559f3cf46e602b17efb8c32b2fb064749258b508952bb58632cd2393d3e`  
		Last Modified: Thu, 26 Jun 2025 01:06:29 GMT  
		Size: 901.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50256d8b021eb3f167a9d21788d4123e6645ea4e51f0de553d0b58f1ec1cb4f5`  
		Last Modified: Thu, 26 Jun 2025 01:06:32 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16173aba83c062a98267c0f657f144ac2856daa767f4f81ab625c2883cd71312`  
		Last Modified: Thu, 26 Jun 2025 01:06:35 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b03a4a43a3ad0e2944abb7d93449ae650a22641b234d05d8bff0c2ca4ed899`  
		Last Modified: Thu, 26 Jun 2025 03:18:05 GMT  
		Size: 93.2 MB (93229228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mediawiki:latest` - unknown; unknown

```console
$ docker pull mediawiki@sha256:864fe54b0df1f1228f6e5ebaeb8a3662e4b51d59c2c106ba1377f25ca6a1861f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 KB (49461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d56023f01f9402d628a643182f77e0ceb1635ffb566ab9a60457f0eca34e763`

```dockerfile
```

-	Layers:
	-	`sha256:efd7f203d6ab51a8e5ac0aad297d9691a074c7fea11d901af8647313c4a05add`  
		Last Modified: Thu, 26 Jun 2025 03:17:48 GMT  
		Size: 49.5 KB (49461 bytes)  
		MIME: application/vnd.in-toto+json
