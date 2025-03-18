## `mediawiki:legacy`

```console
$ docker pull mediawiki@sha256:3d136ab9b264ddcfe8f7b2a470e4def9d5a6dfd24113b8fbc23a49e7dceb6993
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

### `mediawiki:legacy` - linux; amd64

```console
$ docker pull mediawiki@sha256:37c3c7ddbfced632a8c42dd91f03b86bb96747d3b8a7adbe88d228e77cdcf463
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.4 MB (322437744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2833e0f67d0b1c10cf5cdfc63c8c4a3a946539660b29b3d12b18685094e53c87`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 04 Feb 2025 10:42:04 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
# Tue, 04 Feb 2025 10:42:04 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 04 Feb 2025 10:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 04 Feb 2025 10:42:04 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 04 Feb 2025 10:42:04 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 04 Feb 2025 10:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 04 Feb 2025 10:42:04 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 04 Feb 2025 10:42:04 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 04 Feb 2025 10:42:04 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Tue, 04 Feb 2025 10:42:04 GMT
ENV PHP_VERSION=8.1.32
# Tue, 04 Feb 2025 10:42:04 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.32.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.32.tar.xz.asc
# Tue, 04 Feb 2025 10:42:04 GMT
ENV PHP_SHA256=c582ac682a280bbc69bc2186c21eb7e3313cc73099be61a6bc1d2cd337cbf383
# Tue, 04 Feb 2025 10:42:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 04 Feb 2025 10:42:04 GMT
STOPSIGNAL SIGWINCH
# Tue, 04 Feb 2025 10:42:04 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
WORKDIR /var/www/html
# Tue, 04 Feb 2025 10:42:04 GMT
EXPOSE map[80/tcp:{}]
# Tue, 04 Feb 2025 10:42:04 GMT
CMD ["apache2-foreground"]
# Tue, 04 Feb 2025 10:42:04 GMT
RUN set -eux; 		apt-get update; 	apt-get install -y --no-install-recommends 		git 		librsvg2-bin 		imagemagick 		python3 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libicu-dev 		libonig-dev 		liblua5.1-0-dev 	; 		docker-php-ext-install -j "$(nproc)" 		calendar 		intl 		mbstring 		mysqli 		opcache 	; 		pecl install APCu-5.1.24; 	pecl install LuaSandbox-4.1.2; 	docker-php-ext-enable 		apcu 		luasandbox 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
RUN set -eux; 	a2enmod rewrite; 	{ 		echo "<Directory /var/www/html>"; 		echo "  RewriteEngine On"; 		echo "  RewriteCond %{REQUEST_FILENAME} !-f"; 		echo "  RewriteCond %{REQUEST_FILENAME} !-d"; 		echo "  RewriteRule ^ %{DOCUMENT_ROOT}/index.php [L]"; 		echo "</Directory>"; 	} > "$APACHE_CONFDIR/conf-available/short-url.conf"; 	a2enconf short-url # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
RUN sed -i "s/<\/VirtualHost>/\tAllowEncodedSlashes NoDecode\n<\/VirtualHost>/" "$APACHE_CONFDIR/sites-available/000-default.conf" # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
RUN set -eux; 	mkdir -p /var/www/data; 	chown -R www-data:www-data /var/www/data # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
ENV MEDIAWIKI_MAJOR_VERSION=1.42
# Tue, 04 Feb 2025 10:42:04 GMT
ENV MEDIAWIKI_VERSION=1.42.5
# Tue, 04 Feb 2025 10:42:04 GMT
RUN set -eux; 	fetchDeps=" 		gnupg 		dirmngr 	"; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 		curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz" -o mediawiki.tar.gz; 	curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz.sig" -o mediawiki.tar.gz.sig; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 		D7D6767D135A514BEB86E9BA75682B08E8A3FEC4 		441276E9CCD15F44F6D97D18C119E1A64D70938E 		F7F780D82EBFB8A56556E7EE82403E59F9F8CD79 		1D98867E82982C8FE0ABC25F9B69B3109D3BB7B0 		E059C034E7A430583C252F4AA8F734246D73B586 	; 	gpg --batch --verify mediawiki.tar.gz.sig mediawiki.tar.gz; 	tar -x --strip-components=1 -f mediawiki.tar.gz; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" mediawiki.tar.gz.sig mediawiki.tar.gz; 	chown -R www-data:www-data extensions skins cache images; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:6e909acdb790c5a1989d9cfc795fda5a246ad6664bb27b5c688e2b734b2c5fad`  
		Last Modified: Mon, 17 Mar 2025 22:17:24 GMT  
		Size: 28.2 MB (28204865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:548181fe0acec48cb43466227706c533034b712c9c0c94eb6ab73736ca51a3d1`  
		Last Modified: Mon, 17 Mar 2025 23:23:04 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f1bebd3060f7aaa2c2c77c76c0a8efc8236c8214403d4db42790ce87ff69a83`  
		Last Modified: Mon, 17 Mar 2025 23:23:08 GMT  
		Size: 104.3 MB (104329430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bb36efa12a215588862f419836c1c43ccf29d9fd8bf58817f3a980ff0a0cead`  
		Last Modified: Mon, 17 Mar 2025 23:23:04 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31e7fcdb40236fb46482f68dc7ddff078ba5a96284cfc374f9687e6bbf1ff858`  
		Last Modified: Mon, 17 Mar 2025 23:23:05 GMT  
		Size: 20.1 MB (20123775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e416d011d38e8f02eeab60381d74f845949a9e4f4fba6ad6ffc2bc8dedffc95`  
		Last Modified: Mon, 17 Mar 2025 23:23:05 GMT  
		Size: 436.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3747d7ee5a79f8ed273094e3d4e5d34b0d52355222f1a19f71887c1df3ba00ef`  
		Last Modified: Mon, 17 Mar 2025 23:23:05 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce451a7bc6af06a9a3a3efb9b26738c97c424bc575b013af94438bea72c9bfbc`  
		Last Modified: Mon, 17 Mar 2025 23:23:07 GMT  
		Size: 12.0 MB (12022278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37eefc950b5e93ccbdddb8139273936c6dd69204c3cf1e19722b641b769f412d`  
		Last Modified: Mon, 17 Mar 2025 23:23:06 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2941a761d5c9d2d12a7a6ff2030c713887d0223f51e1078af983f0e9080c79a`  
		Last Modified: Mon, 17 Mar 2025 23:23:07 GMT  
		Size: 11.2 MB (11159438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1917b668ccf0f816a8004ade2687eb2630db865a38999eecfd4247ab3b33efde`  
		Last Modified: Mon, 17 Mar 2025 23:23:08 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2707dafc7bdeb4d61c3c5be1f3624e16c00228fb90f6a4b33e174b92cc4fb4e0`  
		Last Modified: Mon, 17 Mar 2025 23:23:08 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4893c1a400c5331f80c2a38d56ce76d08f007a5e8d4551349bf8f35d82df83d7`  
		Last Modified: Mon, 17 Mar 2025 23:23:09 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd8c1a5bd3e0e5757294992028faccb47409f19ce151f024d1f17835e1227eef`  
		Last Modified: Tue, 18 Mar 2025 00:48:47 GMT  
		Size: 53.9 MB (53900795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0997ee4ae3ef3703f4db5f3cfd08f02490b9d3e8ae7349d8bb4239c3b7120043`  
		Last Modified: Tue, 18 Mar 2025 00:48:47 GMT  
		Size: 2.1 MB (2079612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b3b8704dc25b2584ced6451b2195419841b34fb53acf19f9b7f1fd867b7c1f3`  
		Last Modified: Tue, 18 Mar 2025 00:48:47 GMT  
		Size: 577.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d31fa6f7bb8198aa3f82498afe0cc20d2f3d2006c2db9bd62a010c8eb0469849`  
		Last Modified: Tue, 18 Mar 2025 00:48:47 GMT  
		Size: 908.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04f0c89d93c05d1c2030256892de04162b4bc4f2352efdd0c4839e63d0c75e3b`  
		Last Modified: Tue, 18 Mar 2025 00:48:47 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b255b580da25730047db5e6650f3cb52be3d1f24ff45e0aca955f0af452b6818`  
		Last Modified: Tue, 18 Mar 2025 00:48:47 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a365bc62f98ad3f946a15ca2f00104a3404b0ad208391ecdb31de9c3262630`  
		Last Modified: Tue, 18 Mar 2025 00:48:49 GMT  
		Size: 90.6 MB (90610134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mediawiki:legacy` - unknown; unknown

```console
$ docker pull mediawiki@sha256:8d585429e59994b0ccf090c6bc98cc83ee304cea9b710338f14f7313bea4c610
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.6 KB (47564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0641fbc1f940af40552116aaac27ba7ac5d667710834cf83a4e3d509fe506f0`

```dockerfile
```

-	Layers:
	-	`sha256:6ba18d136e742cfec16da6bacb1d633a32f3b82b1bb51ea529a7988d0ad0b5c2`  
		Last Modified: Tue, 18 Mar 2025 00:48:46 GMT  
		Size: 47.6 KB (47564 bytes)  
		MIME: application/vnd.in-toto+json

### `mediawiki:legacy` - linux; arm variant v5

```console
$ docker pull mediawiki@sha256:21ef0b300fa752a45754b65b111a15fc87e920f507114444483529c9cb853701
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.0 MB (290953085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6060333f2af8345c490126ccc36207c6619addf931f05a06c3c85fd749f3e30`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 04 Feb 2025 10:42:04 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1742169600'
# Tue, 04 Feb 2025 10:42:04 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 04 Feb 2025 10:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 04 Feb 2025 10:42:04 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 04 Feb 2025 10:42:04 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 04 Feb 2025 10:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 04 Feb 2025 10:42:04 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 04 Feb 2025 10:42:04 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 04 Feb 2025 10:42:04 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Tue, 04 Feb 2025 10:42:04 GMT
ENV PHP_VERSION=8.1.32
# Tue, 04 Feb 2025 10:42:04 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.32.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.32.tar.xz.asc
# Tue, 04 Feb 2025 10:42:04 GMT
ENV PHP_SHA256=c582ac682a280bbc69bc2186c21eb7e3313cc73099be61a6bc1d2cd337cbf383
# Tue, 04 Feb 2025 10:42:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 04 Feb 2025 10:42:04 GMT
STOPSIGNAL SIGWINCH
# Tue, 04 Feb 2025 10:42:04 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
WORKDIR /var/www/html
# Tue, 04 Feb 2025 10:42:04 GMT
EXPOSE map[80/tcp:{}]
# Tue, 04 Feb 2025 10:42:04 GMT
CMD ["apache2-foreground"]
# Tue, 04 Feb 2025 10:42:04 GMT
RUN set -eux; 		apt-get update; 	apt-get install -y --no-install-recommends 		git 		librsvg2-bin 		imagemagick 		python3 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libicu-dev 		libonig-dev 		liblua5.1-0-dev 	; 		docker-php-ext-install -j "$(nproc)" 		calendar 		intl 		mbstring 		mysqli 		opcache 	; 		pecl install APCu-5.1.24; 	pecl install LuaSandbox-4.1.2; 	docker-php-ext-enable 		apcu 		luasandbox 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
RUN set -eux; 	a2enmod rewrite; 	{ 		echo "<Directory /var/www/html>"; 		echo "  RewriteEngine On"; 		echo "  RewriteCond %{REQUEST_FILENAME} !-f"; 		echo "  RewriteCond %{REQUEST_FILENAME} !-d"; 		echo "  RewriteRule ^ %{DOCUMENT_ROOT}/index.php [L]"; 		echo "</Directory>"; 	} > "$APACHE_CONFDIR/conf-available/short-url.conf"; 	a2enconf short-url # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
RUN sed -i "s/<\/VirtualHost>/\tAllowEncodedSlashes NoDecode\n<\/VirtualHost>/" "$APACHE_CONFDIR/sites-available/000-default.conf" # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
RUN set -eux; 	mkdir -p /var/www/data; 	chown -R www-data:www-data /var/www/data # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
ENV MEDIAWIKI_MAJOR_VERSION=1.42
# Tue, 04 Feb 2025 10:42:04 GMT
ENV MEDIAWIKI_VERSION=1.42.5
# Tue, 04 Feb 2025 10:42:04 GMT
RUN set -eux; 	fetchDeps=" 		gnupg 		dirmngr 	"; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 		curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz" -o mediawiki.tar.gz; 	curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz.sig" -o mediawiki.tar.gz.sig; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 		D7D6767D135A514BEB86E9BA75682B08E8A3FEC4 		441276E9CCD15F44F6D97D18C119E1A64D70938E 		F7F780D82EBFB8A56556E7EE82403E59F9F8CD79 		1D98867E82982C8FE0ABC25F9B69B3109D3BB7B0 		E059C034E7A430583C252F4AA8F734246D73B586 	; 	gpg --batch --verify mediawiki.tar.gz.sig mediawiki.tar.gz; 	tar -x --strip-components=1 -f mediawiki.tar.gz; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" mediawiki.tar.gz.sig mediawiki.tar.gz; 	chown -R www-data:www-data extensions skins cache images; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:87c352465466fcf04c9686fee29c2541af5fc39172801545bb24d9faa8cdeabb`  
		Last Modified: Mon, 17 Mar 2025 22:17:36 GMT  
		Size: 25.7 MB (25735853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50392f60ef98ab502e7ed416d506883257fe8ed57158995e7e77f0bb4d3317f7`  
		Last Modified: Tue, 18 Mar 2025 01:17:31 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70faba6dfc75d37d904a2f4e790ed9afc8110c25721f14deb57e142ce509f203`  
		Last Modified: Tue, 18 Mar 2025 01:17:34 GMT  
		Size: 82.0 MB (81993797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2daffac9eca4d243722e527ddd815f9abe7f53272e743c7fd4b6c1177b0eb255`  
		Last Modified: Tue, 18 Mar 2025 01:17:31 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e40bc50036fecf94b15523ae01df144fd25cc29085c9b900167682966aea345`  
		Last Modified: Tue, 18 Mar 2025 04:03:50 GMT  
		Size: 19.4 MB (19419254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb9ef2e54bf4f16636556f311cb5285d5b86bac864da9ee836197f377a6cb776`  
		Last Modified: Tue, 18 Mar 2025 04:03:49 GMT  
		Size: 432.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ad3f9cc1ac78b8fb303beaac1f3eedbe45e57ac5c8760279395201640c6ddb`  
		Last Modified: Tue, 18 Mar 2025 04:03:50 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a4a2777421c631c0b7fabeeedc6a67e4a717cc97101af65d19c77546d97f354`  
		Last Modified: Tue, 18 Mar 2025 04:26:58 GMT  
		Size: 12.0 MB (12020409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab752bc61d72962c922898d038b767eee51504b267ffa38076f4d092989befc1`  
		Last Modified: Tue, 18 Mar 2025 04:26:58 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27d0e565c119db7c522122f839b6ae489813335f6d1b68da583e38dfacfa461f`  
		Last Modified: Tue, 18 Mar 2025 04:26:59 GMT  
		Size: 10.1 MB (10118887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:209aab2868341bc66de86b4aeca21eaf7b18c5d4d759b832da6c05d38fb8f22b`  
		Last Modified: Tue, 18 Mar 2025 04:26:58 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9655f35f6bb88b9191a8f62a6c9901b130b386e0f292cc0d5269df158901375c`  
		Last Modified: Tue, 18 Mar 2025 04:26:59 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5123de47168c70b145195d9c7bc94d4ab92d540d68c5419d2059ded5203f8640`  
		Last Modified: Tue, 18 Mar 2025 04:26:59 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c9965c64c0f1a8c52d65b91b15f3ae0bb2eac7ab5cdf5bded59dcf143eb4847`  
		Last Modified: Tue, 18 Mar 2025 07:38:40 GMT  
		Size: 49.4 MB (49414573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:525733f663956b25dcd1e2d261ffe4f53355595700b8370d1f7b75ceb44eaac7`  
		Last Modified: Tue, 18 Mar 2025 07:38:39 GMT  
		Size: 1.6 MB (1632669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62925be16c13bafb6ef4a6a800c54261a2fbfacdf96d24c7e4a974a76fb88726`  
		Last Modified: Tue, 18 Mar 2025 07:38:38 GMT  
		Size: 576.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6dd7902decfb6311827ac78b13322ef87ef0a99ec779c04a53e3007334fc156`  
		Last Modified: Tue, 18 Mar 2025 07:38:39 GMT  
		Size: 904.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90c249afcaa1cef422f92990df43b4c3833feebd067b686cbd669285057ce34f`  
		Last Modified: Tue, 18 Mar 2025 07:38:39 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c029750e9ead9de4a138bb0f0ca186ed4e348b7ef5b356ea6225dfc48b2f7ab9`  
		Last Modified: Tue, 18 Mar 2025 07:38:40 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e5acf2817d9c0eb6417bd41cf0d01e6f7a271f82962feb8c42ebb7db7a308c6`  
		Last Modified: Tue, 18 Mar 2025 07:40:39 GMT  
		Size: 90.6 MB (90610237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mediawiki:legacy` - unknown; unknown

```console
$ docker pull mediawiki@sha256:1ef7b5314257740a48a8f0b3a411cb0fee194d998fe566acd38c1d83a1e65145
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 KB (47703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5778b58185720d1da4473108c558b774b144ea4a250ad1b73bbb01fa045060e9`

```dockerfile
```

-	Layers:
	-	`sha256:4d61fb49abc076dbb25c359d0ea9555bb3f621bf036dd7bcd395e2fceb10ab28`  
		Last Modified: Tue, 18 Mar 2025 07:40:36 GMT  
		Size: 47.7 KB (47703 bytes)  
		MIME: application/vnd.in-toto+json

### `mediawiki:legacy` - linux; arm variant v7

```console
$ docker pull mediawiki@sha256:cc6b1a2cb237ff9dfa501f47c9d0d535453523598123130f759ccaad15e439bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.7 MB (278715366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf3fa073443d0771c03154c3276c79977253aa3f5c9f316100dad0620a88a6c7`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 04 Feb 2025 10:42:04 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1740355200'
# Tue, 04 Feb 2025 10:42:04 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 04 Feb 2025 10:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 04 Feb 2025 10:42:04 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 04 Feb 2025 10:42:04 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 04 Feb 2025 10:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 04 Feb 2025 10:42:04 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 04 Feb 2025 10:42:04 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 04 Feb 2025 10:42:04 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Tue, 04 Feb 2025 10:42:04 GMT
ENV PHP_VERSION=8.1.32
# Tue, 04 Feb 2025 10:42:04 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.32.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.32.tar.xz.asc
# Tue, 04 Feb 2025 10:42:04 GMT
ENV PHP_SHA256=c582ac682a280bbc69bc2186c21eb7e3313cc73099be61a6bc1d2cd337cbf383
# Tue, 04 Feb 2025 10:42:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 04 Feb 2025 10:42:04 GMT
STOPSIGNAL SIGWINCH
# Tue, 04 Feb 2025 10:42:04 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
WORKDIR /var/www/html
# Tue, 04 Feb 2025 10:42:04 GMT
EXPOSE map[80/tcp:{}]
# Tue, 04 Feb 2025 10:42:04 GMT
CMD ["apache2-foreground"]
# Tue, 04 Feb 2025 10:42:04 GMT
RUN set -eux; 		apt-get update; 	apt-get install -y --no-install-recommends 		git 		librsvg2-bin 		imagemagick 		python3 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libicu-dev 		libonig-dev 		liblua5.1-0-dev 	; 		docker-php-ext-install -j "$(nproc)" 		calendar 		intl 		mbstring 		mysqli 		opcache 	; 		pecl install APCu-5.1.24; 	pecl install LuaSandbox-4.1.2; 	docker-php-ext-enable 		apcu 		luasandbox 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
RUN set -eux; 	a2enmod rewrite; 	{ 		echo "<Directory /var/www/html>"; 		echo "  RewriteEngine On"; 		echo "  RewriteCond %{REQUEST_FILENAME} !-f"; 		echo "  RewriteCond %{REQUEST_FILENAME} !-d"; 		echo "  RewriteRule ^ %{DOCUMENT_ROOT}/index.php [L]"; 		echo "</Directory>"; 	} > "$APACHE_CONFDIR/conf-available/short-url.conf"; 	a2enconf short-url # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
RUN sed -i "s/<\/VirtualHost>/\tAllowEncodedSlashes NoDecode\n<\/VirtualHost>/" "$APACHE_CONFDIR/sites-available/000-default.conf" # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
RUN set -eux; 	mkdir -p /var/www/data; 	chown -R www-data:www-data /var/www/data # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
ENV MEDIAWIKI_MAJOR_VERSION=1.42
# Tue, 04 Feb 2025 10:42:04 GMT
ENV MEDIAWIKI_VERSION=1.42.5
# Tue, 04 Feb 2025 10:42:04 GMT
RUN set -eux; 	fetchDeps=" 		gnupg 		dirmngr 	"; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 		curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz" -o mediawiki.tar.gz; 	curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz.sig" -o mediawiki.tar.gz.sig; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 		D7D6767D135A514BEB86E9BA75682B08E8A3FEC4 		441276E9CCD15F44F6D97D18C119E1A64D70938E 		F7F780D82EBFB8A56556E7EE82403E59F9F8CD79 		1D98867E82982C8FE0ABC25F9B69B3109D3BB7B0 		E059C034E7A430583C252F4AA8F734246D73B586 	; 	gpg --batch --verify mediawiki.tar.gz.sig mediawiki.tar.gz; 	tar -x --strip-components=1 -f mediawiki.tar.gz; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" mediawiki.tar.gz.sig mediawiki.tar.gz; 	chown -R www-data:www-data extensions skins cache images; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:b47565bb13c54d9e609fa36aeddfc2e70b47de981bac54a6d090c2148f2f4fc4`  
		Last Modified: Tue, 25 Feb 2025 01:30:40 GMT  
		Size: 23.9 MB (23919734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81d7e09b1d1dfb9227526dbb14ab0477c0b3e235584b36c16282a130f9eb0f3c`  
		Last Modified: Tue, 25 Feb 2025 02:45:28 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:195d4e13a8d04cec48669402c294b437f110e69a04f231bf7f4fb038ce009feb`  
		Last Modified: Tue, 25 Feb 2025 02:45:31 GMT  
		Size: 76.2 MB (76162862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f86b4b4427af4c394c935ad45142cba4e205bc21eb933d83f2d2432a5bb3cb64`  
		Last Modified: Tue, 25 Feb 2025 02:45:28 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c9b346bd0d0d97918e8cf0f24429f88856b2aa9caf305b66eabeebc6aa67c68`  
		Last Modified: Tue, 25 Feb 2025 02:49:24 GMT  
		Size: 18.9 MB (18857331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dffc087e149899d6dd0d9896e9ad11e94fde980bb585468298c7ea4818bc83fa`  
		Last Modified: Tue, 25 Feb 2025 02:49:23 GMT  
		Size: 431.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b7d03bc48135c9bb3b0743190bd1e7146614e74be185bd6df7aefdde677f36`  
		Last Modified: Tue, 25 Feb 2025 02:49:23 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72a402730845463b925b8f4004bd053f5005a48434a3ddb796b858f7e1768fb5`  
		Last Modified: Fri, 14 Mar 2025 02:19:43 GMT  
		Size: 12.0 MB (12020357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6250490e648542b014428289376c4f9acc93b14cd76cdf514d9e2e148e16f08`  
		Last Modified: Fri, 14 Mar 2025 02:19:42 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2326b2a98cc981869ae24f3acae105aea0509702728c4f0a93ee41f8d69c5722`  
		Last Modified: Fri, 14 Mar 2025 02:19:43 GMT  
		Size: 9.6 MB (9584583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dfec2008ed3907f2737c216aeebb1422175d618052cc63f32dccd530e7770aa`  
		Last Modified: Fri, 14 Mar 2025 02:19:42 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5917f943fbc9993a1e9f7225aaf0e6dc85d8a3c44cc700c411938903dae8527a`  
		Last Modified: Fri, 14 Mar 2025 02:19:43 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b9db021c977ebf2eba1b0d0df7d91c505f34edea7ac9f2979b7296da9f80e29`  
		Last Modified: Fri, 14 Mar 2025 02:19:43 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cbbd2a5d1066059603383361d0c41b0e841010a8aa83c8f932a45827e42700c`  
		Last Modified: Fri, 14 Mar 2025 13:54:53 GMT  
		Size: 46.0 MB (45979290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b81ac0c6c6632bf95fcc9158e99269c63d9aa5196d06a2a564b1724f1c69f25`  
		Last Modified: Fri, 14 Mar 2025 13:54:52 GMT  
		Size: 1.6 MB (1574284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc0a43d52500a32223e3242af8f8a0fc783423f8596cee14ccf65d17e1e519b0`  
		Last Modified: Fri, 14 Mar 2025 13:54:52 GMT  
		Size: 577.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:925f34347c2af0a15137155e7d6dfccecb1e26fffd88afafc57e8e1832b491df`  
		Last Modified: Fri, 14 Mar 2025 13:54:52 GMT  
		Size: 904.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc1455c0a391f316da39c8f0ea01a345bce7fbfc6e73716d888714b70fbea7b0`  
		Last Modified: Fri, 14 Mar 2025 13:54:53 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:920e66020c47fc3802384f7ce16453769e2b0b35c2233fb5bc3d85331a58ba9a`  
		Last Modified: Fri, 14 Mar 2025 13:54:53 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d38adb7dfcf4bf283b5a877c7fa61735a38a54fa267594bed0fe42ed0afc30`  
		Last Modified: Fri, 14 Mar 2025 13:55:58 GMT  
		Size: 90.6 MB (90609509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mediawiki:legacy` - unknown; unknown

```console
$ docker pull mediawiki@sha256:fc78849ae4ada3e86309692c8e6ac4a8cfcce080d4547e914196d340bca60fc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 KB (47695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8b69d7cad799937d3b0b9c47bd1edea67cb509b5bf5f460543af2c670fbc339`

```dockerfile
```

-	Layers:
	-	`sha256:3a620c032eeb190ea2f75a6edee8906c0bfc4b1a1ce4a4c21cb04a73c2b3595f`  
		Last Modified: Fri, 14 Mar 2025 13:55:54 GMT  
		Size: 47.7 KB (47695 bytes)  
		MIME: application/vnd.in-toto+json

### `mediawiki:legacy` - linux; arm64 variant v8

```console
$ docker pull mediawiki@sha256:310686713abea879a5b3aaab85aa908d4963efa5a8431f17b1d6528d25fc34de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.5 MB (313531810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32f6556a9146719646688523c46bcac4308057dbc87f3f70d9d952b005e7be95`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 04 Feb 2025 10:42:04 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Tue, 04 Feb 2025 10:42:04 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 04 Feb 2025 10:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 04 Feb 2025 10:42:04 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 04 Feb 2025 10:42:04 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 04 Feb 2025 10:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 04 Feb 2025 10:42:04 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 04 Feb 2025 10:42:04 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 04 Feb 2025 10:42:04 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Tue, 04 Feb 2025 10:42:04 GMT
ENV PHP_VERSION=8.1.32
# Tue, 04 Feb 2025 10:42:04 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.32.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.32.tar.xz.asc
# Tue, 04 Feb 2025 10:42:04 GMT
ENV PHP_SHA256=c582ac682a280bbc69bc2186c21eb7e3313cc73099be61a6bc1d2cd337cbf383
# Tue, 04 Feb 2025 10:42:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 04 Feb 2025 10:42:04 GMT
STOPSIGNAL SIGWINCH
# Tue, 04 Feb 2025 10:42:04 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
WORKDIR /var/www/html
# Tue, 04 Feb 2025 10:42:04 GMT
EXPOSE map[80/tcp:{}]
# Tue, 04 Feb 2025 10:42:04 GMT
CMD ["apache2-foreground"]
# Tue, 04 Feb 2025 10:42:04 GMT
RUN set -eux; 		apt-get update; 	apt-get install -y --no-install-recommends 		git 		librsvg2-bin 		imagemagick 		python3 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libicu-dev 		libonig-dev 		liblua5.1-0-dev 	; 		docker-php-ext-install -j "$(nproc)" 		calendar 		intl 		mbstring 		mysqli 		opcache 	; 		pecl install APCu-5.1.24; 	pecl install LuaSandbox-4.1.2; 	docker-php-ext-enable 		apcu 		luasandbox 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
RUN set -eux; 	a2enmod rewrite; 	{ 		echo "<Directory /var/www/html>"; 		echo "  RewriteEngine On"; 		echo "  RewriteCond %{REQUEST_FILENAME} !-f"; 		echo "  RewriteCond %{REQUEST_FILENAME} !-d"; 		echo "  RewriteRule ^ %{DOCUMENT_ROOT}/index.php [L]"; 		echo "</Directory>"; 	} > "$APACHE_CONFDIR/conf-available/short-url.conf"; 	a2enconf short-url # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
RUN sed -i "s/<\/VirtualHost>/\tAllowEncodedSlashes NoDecode\n<\/VirtualHost>/" "$APACHE_CONFDIR/sites-available/000-default.conf" # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
RUN set -eux; 	mkdir -p /var/www/data; 	chown -R www-data:www-data /var/www/data # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
ENV MEDIAWIKI_MAJOR_VERSION=1.42
# Tue, 04 Feb 2025 10:42:04 GMT
ENV MEDIAWIKI_VERSION=1.42.5
# Tue, 04 Feb 2025 10:42:04 GMT
RUN set -eux; 	fetchDeps=" 		gnupg 		dirmngr 	"; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 		curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz" -o mediawiki.tar.gz; 	curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz.sig" -o mediawiki.tar.gz.sig; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 		D7D6767D135A514BEB86E9BA75682B08E8A3FEC4 		441276E9CCD15F44F6D97D18C119E1A64D70938E 		F7F780D82EBFB8A56556E7EE82403E59F9F8CD79 		1D98867E82982C8FE0ABC25F9B69B3109D3BB7B0 		E059C034E7A430583C252F4AA8F734246D73B586 	; 	gpg --batch --verify mediawiki.tar.gz.sig mediawiki.tar.gz; 	tar -x --strip-components=1 -f mediawiki.tar.gz; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" mediawiki.tar.gz.sig mediawiki.tar.gz; 	chown -R www-data:www-data extensions skins cache images; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31676cd976ed7c1a1f79275ef2602fefb67765b353e429d88aab3fd76863e399`  
		Last Modified: Tue, 25 Feb 2025 03:03:46 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e6e69341e71d07089c45827b72bbbf8ca0698042a25ca2375d9c71797edd77e`  
		Last Modified: Tue, 25 Feb 2025 03:03:49 GMT  
		Size: 98.1 MB (98130460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5ee28dda6888ebc4fc51f7f52c135986c07171dad8ce5a8fafed9d2f65d62ec`  
		Last Modified: Tue, 25 Feb 2025 03:03:47 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90ffecde8bd985cf96f0467d70fccc665026fdab770dcac3f793be1deba85a30`  
		Last Modified: Tue, 25 Feb 2025 03:07:28 GMT  
		Size: 20.1 MB (20120919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eab17c0b9534d8803a88e819a77b6257c8c52458e1501948f051ab897599e4bb`  
		Last Modified: Tue, 25 Feb 2025 03:07:27 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a72d58237634f94d2abae7d95c65d651fb63692600b04577a084ebafecdf4289`  
		Last Modified: Tue, 25 Feb 2025 03:07:27 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c6379226ce70d05ecd5f8e164d8249011c7c556086c3f8c48f8400957d12022`  
		Last Modified: Fri, 14 Mar 2025 04:24:05 GMT  
		Size: 12.0 MB (12022041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8af90cd6f309f95eb87382a3ccc29b9a8b2e04c711a3e0a1dcc895859ef9ae6`  
		Last Modified: Fri, 14 Mar 2025 04:24:04 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:895cfb42dde64038309804ddcf1448c7c4e7241115b83023a14ac8b6d01293bc`  
		Last Modified: Fri, 14 Mar 2025 04:24:05 GMT  
		Size: 11.2 MB (11160448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7a53e9a4c86177fac3f446047045084e7f582ac8ad0f6efda3d81498c0fbce8`  
		Last Modified: Fri, 14 Mar 2025 04:24:04 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be2b99dcd316e5866e87801b18434ce90b4aa27768981b6b98f9b074f7f06dc8`  
		Last Modified: Fri, 14 Mar 2025 04:24:05 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31b3511a0228ddfb17c9661372b95fece363d4422287a848e2430433f8f30498`  
		Last Modified: Fri, 14 Mar 2025 04:24:05 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdb4156528f626463d70ff515802ca57c6c76ddeb4d486d360d3ff21877afc18`  
		Last Modified: Fri, 14 Mar 2025 20:55:48 GMT  
		Size: 51.1 MB (51095795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab436ddce2d42cc048b457b2857be2d3226188fec90f435a8711ec8bf1e387d1`  
		Last Modified: Fri, 14 Mar 2025 20:55:46 GMT  
		Size: 2.3 MB (2335252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1726653cc9bdc9b7bd8177039dea5363a87a8bbe7648117e39b59e1e2a315752`  
		Last Modified: Fri, 14 Mar 2025 20:55:46 GMT  
		Size: 578.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfed2ed06a1e34460e2db10634ce036bcaa477723062b56d2384c3c6a0e976db`  
		Last Modified: Fri, 14 Mar 2025 20:55:46 GMT  
		Size: 907.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecaedb7b22900215ad2dccfcfcc0a91a80bab4b5e7e3f0acc15f4acb409a177b`  
		Last Modified: Fri, 14 Mar 2025 20:55:47 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:371152819e95f1a1e82c8f0b32cb378da335b9af41cdef6c312574c84a5ffa22`  
		Last Modified: Fri, 14 Mar 2025 20:55:47 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c87c174b876be4afa323e72707f1c1fa00ae614f8d7e9576a6fecc715d2865ac`  
		Last Modified: Fri, 14 Mar 2025 20:55:50 GMT  
		Size: 90.6 MB (90611052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mediawiki:legacy` - unknown; unknown

```console
$ docker pull mediawiki@sha256:a84d21f32d7e51fc887486a8710abb0dde246a60683b4fb673b889ab082e0169
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 KB (47739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e92f7bde4c04deb0bf6ce3fb29d62a7da30f8392fb89b89e3dc307a7d6a8df9`

```dockerfile
```

-	Layers:
	-	`sha256:246819135df99f04e23c25a36b38bf67241592cd2b8289e39fd41bf5f8cb21c3`  
		Last Modified: Fri, 14 Mar 2025 20:55:46 GMT  
		Size: 47.7 KB (47739 bytes)  
		MIME: application/vnd.in-toto+json

### `mediawiki:legacy` - linux; 386

```console
$ docker pull mediawiki@sha256:14188b5d75caf7295a8de6c03ff2408626b77b3e5b4100dbff865a76e1f075a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.9 MB (322874323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55f89311c8822b9c4879df53f631931bc12ff1c65b8613500bbbdca0b3bbb071`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 04 Feb 2025 10:42:04 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1742169600'
# Tue, 04 Feb 2025 10:42:04 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 04 Feb 2025 10:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 04 Feb 2025 10:42:04 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 04 Feb 2025 10:42:04 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 04 Feb 2025 10:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 04 Feb 2025 10:42:04 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 04 Feb 2025 10:42:04 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 04 Feb 2025 10:42:04 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Tue, 04 Feb 2025 10:42:04 GMT
ENV PHP_VERSION=8.1.32
# Tue, 04 Feb 2025 10:42:04 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.32.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.32.tar.xz.asc
# Tue, 04 Feb 2025 10:42:04 GMT
ENV PHP_SHA256=c582ac682a280bbc69bc2186c21eb7e3313cc73099be61a6bc1d2cd337cbf383
# Tue, 04 Feb 2025 10:42:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 04 Feb 2025 10:42:04 GMT
STOPSIGNAL SIGWINCH
# Tue, 04 Feb 2025 10:42:04 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
WORKDIR /var/www/html
# Tue, 04 Feb 2025 10:42:04 GMT
EXPOSE map[80/tcp:{}]
# Tue, 04 Feb 2025 10:42:04 GMT
CMD ["apache2-foreground"]
# Tue, 04 Feb 2025 10:42:04 GMT
RUN set -eux; 		apt-get update; 	apt-get install -y --no-install-recommends 		git 		librsvg2-bin 		imagemagick 		python3 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libicu-dev 		libonig-dev 		liblua5.1-0-dev 	; 		docker-php-ext-install -j "$(nproc)" 		calendar 		intl 		mbstring 		mysqli 		opcache 	; 		pecl install APCu-5.1.24; 	pecl install LuaSandbox-4.1.2; 	docker-php-ext-enable 		apcu 		luasandbox 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
RUN set -eux; 	a2enmod rewrite; 	{ 		echo "<Directory /var/www/html>"; 		echo "  RewriteEngine On"; 		echo "  RewriteCond %{REQUEST_FILENAME} !-f"; 		echo "  RewriteCond %{REQUEST_FILENAME} !-d"; 		echo "  RewriteRule ^ %{DOCUMENT_ROOT}/index.php [L]"; 		echo "</Directory>"; 	} > "$APACHE_CONFDIR/conf-available/short-url.conf"; 	a2enconf short-url # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
RUN sed -i "s/<\/VirtualHost>/\tAllowEncodedSlashes NoDecode\n<\/VirtualHost>/" "$APACHE_CONFDIR/sites-available/000-default.conf" # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
RUN set -eux; 	mkdir -p /var/www/data; 	chown -R www-data:www-data /var/www/data # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
ENV MEDIAWIKI_MAJOR_VERSION=1.42
# Tue, 04 Feb 2025 10:42:04 GMT
ENV MEDIAWIKI_VERSION=1.42.5
# Tue, 04 Feb 2025 10:42:04 GMT
RUN set -eux; 	fetchDeps=" 		gnupg 		dirmngr 	"; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 		curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz" -o mediawiki.tar.gz; 	curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz.sig" -o mediawiki.tar.gz.sig; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 		D7D6767D135A514BEB86E9BA75682B08E8A3FEC4 		441276E9CCD15F44F6D97D18C119E1A64D70938E 		F7F780D82EBFB8A56556E7EE82403E59F9F8CD79 		1D98867E82982C8FE0ABC25F9B69B3109D3BB7B0 		E059C034E7A430583C252F4AA8F734246D73B586 	; 	gpg --batch --verify mediawiki.tar.gz.sig mediawiki.tar.gz; 	tar -x --strip-components=1 -f mediawiki.tar.gz; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" mediawiki.tar.gz.sig mediawiki.tar.gz; 	chown -R www-data:www-data extensions skins cache images; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:bdeb081d427d7feac6a8c0bd36a2c34506a1aa38143fe43a5c5a8c162698a854`  
		Last Modified: Mon, 17 Mar 2025 22:17:35 GMT  
		Size: 29.2 MB (29189528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9a57c3c2f159c8521c9d3046b946eb0daa0d18d2c4f58e4d9c969e70bc53c6a`  
		Last Modified: Mon, 17 Mar 2025 23:36:44 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e39a689a8577e1219b47d3ff0ece0df386a35652e01091134a442514661dd0f`  
		Last Modified: Mon, 17 Mar 2025 23:36:47 GMT  
		Size: 101.5 MB (101512505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef416291c48600932917a03cea92fa9f2e652a7c84be7264cabbd2e16d7c8774`  
		Last Modified: Mon, 17 Mar 2025 23:36:34 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b116791b923029429767ef58876ce2f6b7429734cb641d995f89a6c211a79241`  
		Last Modified: Mon, 17 Mar 2025 23:36:46 GMT  
		Size: 20.6 MB (20638435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4225dbb196b5404ec1e3bbefff5f110e544bf77c24d6453965b900a816454d30`  
		Last Modified: Mon, 17 Mar 2025 23:36:44 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:486f85f36de41d707a3b26060d20ce8b8e54d007eb7283398a56563e79792a45`  
		Last Modified: Mon, 17 Mar 2025 23:36:45 GMT  
		Size: 481.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db8ff26d33ab0ffa983926d5620f3d3dd7fe5fc69a9591d69c1da719681bde27`  
		Last Modified: Mon, 17 Mar 2025 23:36:46 GMT  
		Size: 12.0 MB (12021284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:920effe82b94f4d4d9e752271ecb523e2b8cfc5f00e83cc98b6b244b3a4999d9`  
		Last Modified: Mon, 17 Mar 2025 23:36:46 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4786b5f16133167a6107d8600def3a5ad61c18a2250cd335994db6a7422d59a7`  
		Last Modified: Mon, 17 Mar 2025 23:36:48 GMT  
		Size: 11.4 MB (11383932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7f5514cda83ad98c5b5d48760fb63ed6a645625981a7a087cb44040a304c3d0`  
		Last Modified: Mon, 17 Mar 2025 23:36:47 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa9c14902ce77f7d7fd5bdfdc24193fb49193994025960debf295ad901e1684`  
		Last Modified: Mon, 17 Mar 2025 23:36:48 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0e6e45ee5427ae00a9ca1520f36452f14a771442bdd400ffd81b5d21941580a`  
		Last Modified: Mon, 17 Mar 2025 23:36:48 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e86c2fdf9e5ec26f1e7eaab5b279b41a2624e2bdf097628b7345b30d3f0ab12`  
		Last Modified: Tue, 18 Mar 2025 00:30:13 GMT  
		Size: 55.4 MB (55431965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d55ef3d090116cc296723b4c3588ca26fad37242f0296d5816f55572d88b137e`  
		Last Modified: Tue, 18 Mar 2025 00:30:11 GMT  
		Size: 2.1 MB (2079991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dcd6fc109cf7bf3ffaf47bc7812dd6384ef766e40a912b1af74c23dbfbf784c`  
		Last Modified: Tue, 18 Mar 2025 00:30:10 GMT  
		Size: 577.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:963bbcf747c8137e9c7898ce685e6c4812c7eec1a075f019c6842c5faf0db2de`  
		Last Modified: Tue, 18 Mar 2025 00:30:10 GMT  
		Size: 903.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f26ff9197b44d2a8dbb6dc5358afca6fa4fbe90a4bbfe8bcd1b57e2b49df42c`  
		Last Modified: Tue, 18 Mar 2025 00:30:11 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff630ff3c4e09b0314d38141a956327d3eaf1d6a325f23fc11f8736f2a08bc96`  
		Last Modified: Tue, 18 Mar 2025 00:30:11 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faa3f67c7576d59103f68083c6ab16d87e5629cc999d6f0b35941792fa75b557`  
		Last Modified: Tue, 18 Mar 2025 00:30:15 GMT  
		Size: 90.6 MB (90609282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mediawiki:legacy` - unknown; unknown

```console
$ docker pull mediawiki@sha256:b28db2a5344185123e8ce3f520ab6c548209acba7181a274255be2b1ec5a1fb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.5 KB (47525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a80431948d119037710a5d9f7248b54866383533285a59a46a80d49c40e6958`

```dockerfile
```

-	Layers:
	-	`sha256:3092be2f5ff1f2b033bf15d35194bd10ec3aefb5ae7bf8e561f36ae3e2e444cd`  
		Last Modified: Tue, 18 Mar 2025 00:30:10 GMT  
		Size: 47.5 KB (47525 bytes)  
		MIME: application/vnd.in-toto+json

### `mediawiki:legacy` - linux; ppc64le

```console
$ docker pull mediawiki@sha256:51414ffb436998127ced8c210572c1c92c40410ab2e010ee3e10612dd305813a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.8 MB (330766824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fda679e9ad95a4b086659420ede244e9d33df8c43e05c3db42add366f6e234c7`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 04 Feb 2025 10:42:04 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1740355200'
# Tue, 04 Feb 2025 10:42:04 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 04 Feb 2025 10:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 04 Feb 2025 10:42:04 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 04 Feb 2025 10:42:04 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 04 Feb 2025 10:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 04 Feb 2025 10:42:04 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 04 Feb 2025 10:42:04 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 04 Feb 2025 10:42:04 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Tue, 04 Feb 2025 10:42:04 GMT
ENV PHP_VERSION=8.1.32
# Tue, 04 Feb 2025 10:42:04 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.32.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.32.tar.xz.asc
# Tue, 04 Feb 2025 10:42:04 GMT
ENV PHP_SHA256=c582ac682a280bbc69bc2186c21eb7e3313cc73099be61a6bc1d2cd337cbf383
# Tue, 04 Feb 2025 10:42:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 04 Feb 2025 10:42:04 GMT
STOPSIGNAL SIGWINCH
# Tue, 04 Feb 2025 10:42:04 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
WORKDIR /var/www/html
# Tue, 04 Feb 2025 10:42:04 GMT
EXPOSE map[80/tcp:{}]
# Tue, 04 Feb 2025 10:42:04 GMT
CMD ["apache2-foreground"]
# Tue, 04 Feb 2025 10:42:04 GMT
RUN set -eux; 		apt-get update; 	apt-get install -y --no-install-recommends 		git 		librsvg2-bin 		imagemagick 		python3 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libicu-dev 		libonig-dev 		liblua5.1-0-dev 	; 		docker-php-ext-install -j "$(nproc)" 		calendar 		intl 		mbstring 		mysqli 		opcache 	; 		pecl install APCu-5.1.24; 	pecl install LuaSandbox-4.1.2; 	docker-php-ext-enable 		apcu 		luasandbox 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
RUN set -eux; 	a2enmod rewrite; 	{ 		echo "<Directory /var/www/html>"; 		echo "  RewriteEngine On"; 		echo "  RewriteCond %{REQUEST_FILENAME} !-f"; 		echo "  RewriteCond %{REQUEST_FILENAME} !-d"; 		echo "  RewriteRule ^ %{DOCUMENT_ROOT}/index.php [L]"; 		echo "</Directory>"; 	} > "$APACHE_CONFDIR/conf-available/short-url.conf"; 	a2enconf short-url # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
RUN sed -i "s/<\/VirtualHost>/\tAllowEncodedSlashes NoDecode\n<\/VirtualHost>/" "$APACHE_CONFDIR/sites-available/000-default.conf" # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
RUN set -eux; 	mkdir -p /var/www/data; 	chown -R www-data:www-data /var/www/data # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
ENV MEDIAWIKI_MAJOR_VERSION=1.42
# Tue, 04 Feb 2025 10:42:04 GMT
ENV MEDIAWIKI_VERSION=1.42.5
# Tue, 04 Feb 2025 10:42:04 GMT
RUN set -eux; 	fetchDeps=" 		gnupg 		dirmngr 	"; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 		curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz" -o mediawiki.tar.gz; 	curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz.sig" -o mediawiki.tar.gz.sig; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 		D7D6767D135A514BEB86E9BA75682B08E8A3FEC4 		441276E9CCD15F44F6D97D18C119E1A64D70938E 		F7F780D82EBFB8A56556E7EE82403E59F9F8CD79 		1D98867E82982C8FE0ABC25F9B69B3109D3BB7B0 		E059C034E7A430583C252F4AA8F734246D73B586 	; 	gpg --batch --verify mediawiki.tar.gz.sig mediawiki.tar.gz; 	tar -x --strip-components=1 -f mediawiki.tar.gz; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" mediawiki.tar.gz.sig mediawiki.tar.gz; 	chown -R www-data:www-data extensions skins cache images; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Feb 2025 10:42:04 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:4713de4e13d024eec0b1cb2d083909104c2a36ed3ffba92c5cf710577a33ad45`  
		Last Modified: Tue, 25 Feb 2025 01:30:47 GMT  
		Size: 32.1 MB (32052314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35bbbae4d2dc0350f7df1634e33daf64fe78cb672182650c700a26750b33b64c`  
		Last Modified: Tue, 25 Feb 2025 02:59:24 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e7f7bed916e76b3a3b176b4e6a5bcfe6e10e39a6c423be8fc3575115d7b1e06`  
		Last Modified: Tue, 25 Feb 2025 02:59:28 GMT  
		Size: 103.3 MB (103323545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21d9943a0d5cef1bf22e1a6d5df4b38af8052474c28fe7d9188d33c9e0190742`  
		Last Modified: Tue, 25 Feb 2025 02:59:24 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f5eba5668f315d2ef7f70338fc89daecbca191bf9b5b6622280439ff5ceb4a7`  
		Last Modified: Tue, 25 Feb 2025 03:04:11 GMT  
		Size: 21.3 MB (21308442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8bec4fde36a5fc026717bc0e1c4a8f85c6397c11d730b4d345fdb0b5014cc45`  
		Last Modified: Tue, 25 Feb 2025 03:04:06 GMT  
		Size: 435.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca66cb544073b521bd3bcd518135c4cf977a5939323c5191473a1b8a2a09cd05`  
		Last Modified: Tue, 25 Feb 2025 03:04:06 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5964aba6a8633f2015317711fc170714ddb1c2dcbcbd8b3f26ec3b8e99d6338f`  
		Last Modified: Fri, 14 Mar 2025 00:59:52 GMT  
		Size: 12.0 MB (12021771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b9360fd653afe015875ebbfe7e45561120334ff7f3b2620381653c76490d8aa`  
		Last Modified: Fri, 14 Mar 2025 00:59:51 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e7aea4e6cf22b3a949635191c49ad8781e648181878be1408de485f3ff706c6`  
		Last Modified: Fri, 14 Mar 2025 00:59:52 GMT  
		Size: 11.5 MB (11529569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc9b17ecad0c8de27e37bac58c19066cedc101fb7171758630bea900b538364`  
		Last Modified: Fri, 14 Mar 2025 00:59:51 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:638f40c7e8ad76e9f4889b9ce961b2e74ec42467472117ffbb5b5f27e61ad1df`  
		Last Modified: Fri, 14 Mar 2025 00:59:52 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51b13bc4112d70010cb759c70dad2ec045966532f9b8448e188d9715c8631e09`  
		Last Modified: Fri, 14 Mar 2025 00:59:52 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0a7a5a779716302ec64d2af7ec8fdae1782fff52e8662ef6b2028d181da0b6c`  
		Last Modified: Fri, 14 Mar 2025 04:48:08 GMT  
		Size: 58.1 MB (58103807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5d0fdf66153953a4c5ccb303e74ec4bd1f43695bcc644f94e7b5c374ae4c2a0`  
		Last Modified: Fri, 14 Mar 2025 04:48:06 GMT  
		Size: 1.8 MB (1809696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79e881da87cb44af067739730b68e86b5e346b8d85fc6255fd56f5c3c9ad41bd`  
		Last Modified: Fri, 14 Mar 2025 04:48:06 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4529e0ab0db7e78bb420fe7bb80bf2a25ea0a5d362bb1d5f94a3bbf8cccae93f`  
		Last Modified: Fri, 14 Mar 2025 04:48:06 GMT  
		Size: 905.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b22c5c503774e7108dc55b0cdb877c24d81357eff1453a1c246a2e909a3ea0d6`  
		Last Modified: Fri, 14 Mar 2025 04:48:07 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce78a0247493c10fbed15bde8031d9148c0ed70ff25e2bde25ae2bc5cc2ca9ee`  
		Last Modified: Fri, 14 Mar 2025 04:48:07 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3d6b3f1fcc781f64254e8a33fd78127afcdb5895eef982f1b81a54db9c00d7c`  
		Last Modified: Fri, 14 Mar 2025 04:48:10 GMT  
		Size: 90.6 MB (90610248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mediawiki:legacy` - unknown; unknown

```console
$ docker pull mediawiki@sha256:2775aca3d316921b0cae58d5d5120593117c1a77ebc09d6f8be9ebcde6b941ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.6 KB (47615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87c01cc0cecba0827bc8ddd539dabcb37e917a4b7a0f6bfa654db7d3970f66e1`

```dockerfile
```

-	Layers:
	-	`sha256:1363d549c7c6fb84c023f2514e59d48f78b25efbabe47f06316fa6914f5d98fa`  
		Last Modified: Fri, 14 Mar 2025 04:48:05 GMT  
		Size: 47.6 KB (47615 bytes)  
		MIME: application/vnd.in-toto+json
