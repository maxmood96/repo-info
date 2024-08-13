## `backdrop:latest`

```console
$ docker pull backdrop@sha256:648655bcd223c686c0d53e4a5f61be4507c96de33996005a28a95ca087401a8c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:latest` - linux; amd64

```console
$ docker pull backdrop@sha256:65f1103d27cbfdeab122ec37ea13dd4456655c6bc2ed9fff19c4fb00556d75cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.4 MB (191432142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:844e54434e12481d630c6e587c160e8645a057af62cca30f04078a2883f5baac`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 14 Oct 2023 00:46:03 GMT
ADD file:3d9897cfe027ecc7cbdb16e74a676ed143725ea2d08dbb0dde23309e041de0f3 in / 
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["bash"]
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 14 Oct 2023 00:46:03 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Sat, 14 Oct 2023 00:46:03 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Sat, 14 Oct 2023 00:46:03 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 14 Oct 2023 00:46:03 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_VERSION=8.1.29
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.29.tar.xz.asc
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_SHA256=288884af60581d4284baba2ace9ca6d646f72facbd3e3c2dd2acc7fe6f903536
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sat, 14 Oct 2023 00:46:03 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 14 Oct 2023 00:46:03 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Sat, 14 Oct 2023 00:46:03 GMT
RUN docker-php-ext-enable sodium
# Sat, 14 Oct 2023 00:46:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 14 Oct 2023 00:46:03 GMT
STOPSIGNAL SIGWINCH
# Sat, 14 Oct 2023 00:46:03 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Sat, 14 Oct 2023 00:46:03 GMT
WORKDIR /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
EXPOSE 80
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["apache2-foreground"]
# Sat, 14 Oct 2023 00:46:03 GMT
RUN a2enmod rewrite # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
WORKDIR /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
ENV BACKDROP_VERSION=1.26.1
# Sat, 14 Oct 2023 00:46:03 GMT
ENV BACKDROP_MD5=0a6fad09190b1f8da266f586955454a2
# Sat, 14 Oct 2023 00:46:03 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:e4fff0779e6ddd22366469f08626c3ab1884b5cbe1719b26da238c95f247b305`  
		Last Modified: Tue, 13 Aug 2024 00:23:48 GMT  
		Size: 29.1 MB (29126232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebe65c9579cf319330d41574ba2da6432b17c0704a30f367e69a18f8fb521d08`  
		Last Modified: Tue, 13 Aug 2024 02:53:56 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73fb9bdf2456ca44f41273902e3ffd4c8913ba2c9e48754e4802b8646b2d6cf8`  
		Last Modified: Tue, 13 Aug 2024 02:54:11 GMT  
		Size: 104.3 MB (104349003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029db5f1c17f8a732ffd7afbeccfbaaf44323a683087527c8d2414213ab53f32`  
		Last Modified: Tue, 13 Aug 2024 02:53:56 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:364fd66af37d30f608a646fe71d0c1e709e0549a5d4d3fb008993ec89ebfe57b`  
		Last Modified: Tue, 13 Aug 2024 02:54:33 GMT  
		Size: 20.3 MB (20327979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de55dbd5d2208f77cf2fe2643914f9f219753016786a9cea73fb344ac0f892b7`  
		Last Modified: Tue, 13 Aug 2024 02:54:31 GMT  
		Size: 438.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18b6e8540b906f4440e44686742488990c25449285e6138059d60f268556b965`  
		Last Modified: Tue, 13 Aug 2024 02:54:31 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83b088dc790fe0f6c346b16b5f80d6ec93cc1e71cddbe6b51b7a5f1b7f4e67fc`  
		Last Modified: Tue, 13 Aug 2024 03:02:05 GMT  
		Size: 12.2 MB (12159416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25779f1055863b9fd30f308fd727e0c0e650c6cf713e812f1c8364fb95506bc0`  
		Last Modified: Tue, 13 Aug 2024 03:02:02 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f781cb0f10758969e239f7fdb573e608e3d85b9d3e029518d976c112e63c3840`  
		Last Modified: Tue, 13 Aug 2024 03:02:04 GMT  
		Size: 11.2 MB (11155845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e555397bcfab647ff44d94f832c3e0588943255bb25637402d04edc379f6bde0`  
		Last Modified: Tue, 13 Aug 2024 03:02:02 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b90e4ceed4d60375c67c596077465c4925f4acad6b042aaab7ba824c7d1e5989`  
		Last Modified: Tue, 13 Aug 2024 03:02:02 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bbed0b95816864f8a261190688aa2ae587c5bdbbc812f7208221707d22bc77b`  
		Last Modified: Tue, 13 Aug 2024 03:02:02 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:250e30d2c9502bd6c1fdea608710506ecaf11bb9fd295e7e06a82e622fbef12f`  
		Last Modified: Tue, 13 Aug 2024 04:01:36 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d530ec10014af85296e384eee01c10d1b6f3373917eb360e5a97548bd8812cf`  
		Last Modified: Tue, 13 Aug 2024 04:01:36 GMT  
		Size: 5.5 MB (5501759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7869fb1262a6fcaaa983d5c5101915f4d1ceb1e87d54d483c01f3e87fc380ba`  
		Last Modified: Tue, 13 Aug 2024 04:01:36 GMT  
		Size: 8.8 MB (8805154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d83d8844d5dfd735fe9c43fbe677df5464d4aaf42273c0fc5bf21bbaea4ec2d`  
		Last Modified: Tue, 13 Aug 2024 04:01:36 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:latest` - unknown; unknown

```console
$ docker pull backdrop@sha256:de600ad0ec61aae818059c024e8466872a580fe15cf298ada2f359bbea7fe046
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6955229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:213cb5289f363788224ee734a0b86bd34a20d89e6fa1369be4d87e6b23fe5368`

```dockerfile
```

-	Layers:
	-	`sha256:c333742e027300148857def78c6482151ed162c8adaf5bc5e81232b82cc10b4e`  
		Last Modified: Tue, 13 Aug 2024 04:01:36 GMT  
		Size: 6.9 MB (6926280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43c79de848488f459792550ec90afe0a303b722f83b59be80c14dc18a515c213`  
		Last Modified: Tue, 13 Aug 2024 04:01:36 GMT  
		Size: 28.9 KB (28949 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:latest` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:a03c903e82a06e83624ea263c2a2f88df64f194ed07de1ab432a7279a4b6315b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.3 MB (185259817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e34e809df7665c405ccb0c44e2d49e07b487ceb919a4eae28c663838a323daa`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 14 Oct 2023 00:46:03 GMT
ADD file:9b9556e1f3168a82eb85577dc07d85b2e7c1a72c5c35a4003f00042dd27b4fa2 in / 
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["bash"]
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 14 Oct 2023 00:46:03 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Sat, 14 Oct 2023 00:46:03 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Sat, 14 Oct 2023 00:46:03 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 14 Oct 2023 00:46:03 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_VERSION=8.1.29
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.29.tar.xz.asc
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_SHA256=288884af60581d4284baba2ace9ca6d646f72facbd3e3c2dd2acc7fe6f903536
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sat, 14 Oct 2023 00:46:03 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 14 Oct 2023 00:46:03 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Sat, 14 Oct 2023 00:46:03 GMT
RUN docker-php-ext-enable sodium
# Sat, 14 Oct 2023 00:46:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 14 Oct 2023 00:46:03 GMT
STOPSIGNAL SIGWINCH
# Sat, 14 Oct 2023 00:46:03 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Sat, 14 Oct 2023 00:46:03 GMT
WORKDIR /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
EXPOSE 80
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["apache2-foreground"]
# Sat, 14 Oct 2023 00:46:03 GMT
RUN a2enmod rewrite # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
WORKDIR /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
ENV BACKDROP_VERSION=1.26.1
# Sat, 14 Oct 2023 00:46:03 GMT
ENV BACKDROP_MD5=0a6fad09190b1f8da266f586955454a2
# Sat, 14 Oct 2023 00:46:03 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:262a5f25eec7a7daccd94a64695e41acca5262f481c3630ef31289616897aa40`  
		Last Modified: Tue, 23 Jul 2024 04:20:29 GMT  
		Size: 29.2 MB (29156571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfc24c12812b24708888b440f67cf39295111ce0406b3816522533957cfca6a5`  
		Last Modified: Tue, 23 Jul 2024 07:47:55 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c80056e3fbbff475fe84dde2da2642e8ed70b430cb97f6aa613d49ef6c635624`  
		Last Modified: Tue, 23 Jul 2024 07:48:07 GMT  
		Size: 98.1 MB (98131446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f09a265e9595e55f8a9e0c1f1e8b47c3dfa5c5ef02b83f68606ccaca026601a`  
		Last Modified: Tue, 23 Jul 2024 07:47:55 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9bee02aac93aa565658f5f0df1cfbc9d3bd396876bd1c96e47ba2aa0529bd33`  
		Last Modified: Tue, 23 Jul 2024 07:48:30 GMT  
		Size: 20.3 MB (20324783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0df0b4d6b36f10ef6560f6dec888e4c9a33aaf22dd49ab5406dc4bf2b4a41ff2`  
		Last Modified: Tue, 23 Jul 2024 07:48:28 GMT  
		Size: 434.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45ee99f2fe1d2c0500eea615b9137c7284a47b9e6bac9f34a412dab37f39b6d7`  
		Last Modified: Tue, 23 Jul 2024 07:48:28 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03aa511cf3ab2c98eab26613ed0359f79b351b7d2fb884dc1b928b2133feb403`  
		Last Modified: Tue, 23 Jul 2024 07:59:57 GMT  
		Size: 12.2 MB (12159036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:269536d152165187d565a0eadd714bce34ae92c27c1215fcb2e19c2efd21ad01`  
		Last Modified: Tue, 23 Jul 2024 07:59:55 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9729c5375183ecc71e8ba24f125937fe85f92664a52515ee535f538c03cf44f4`  
		Last Modified: Tue, 23 Jul 2024 07:59:56 GMT  
		Size: 11.2 MB (11154586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5daee4feb0a2602a28bad589927be4bfe565070df6a2281568becde4fb4bf022`  
		Last Modified: Tue, 23 Jul 2024 07:59:55 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:751bac29936487c5c4625fca68a93e4f1bd32f28395aaeb36381dbebe8eaec5f`  
		Last Modified: Tue, 23 Jul 2024 07:59:55 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77525f8b166eb792f5de4c1fe7082d10f5ea1735a93b72ead3df97d86c09125d`  
		Last Modified: Tue, 23 Jul 2024 07:59:55 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5be397d309c8a336fc937ac3301aa9f1c0eabe90ac87a2828de2ec28b8274352`  
		Last Modified: Tue, 23 Jul 2024 11:11:46 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce44306e951d8ae1af2c1a9f4c8323c25f1b233446f50f35e70c89831328a158`  
		Last Modified: Tue, 23 Jul 2024 11:11:47 GMT  
		Size: 5.5 MB (5521473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d98a42ca8fddc1f70209c809ef1e9104c758f3b1820d65e5b1aeb3409d7300d3`  
		Last Modified: Tue, 23 Jul 2024 11:11:47 GMT  
		Size: 8.8 MB (8805178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08159f37174fa841546f5948cc275530afd32adabef0258ecdf7771d9f973b66`  
		Last Modified: Tue, 23 Jul 2024 11:11:47 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:latest` - unknown; unknown

```console
$ docker pull backdrop@sha256:6d0e1799d585182361e55c8e0d0ca13b1f0efd238f85848504d1438c38ad587c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6984085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:298c3e1fbdc755f15375846b4fa3d228a706ee70aacbd0b1f52e60af82c4b534`

```dockerfile
```

-	Layers:
	-	`sha256:4f4f6a2a77aaea52694ef533aa903ed7877f0cc976e79a689f2c63eccee0595c`  
		Last Modified: Tue, 23 Jul 2024 11:11:43 GMT  
		Size: 7.0 MB (6954792 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd0fd1146ecc3b42a45d23308ee40bdfdb8b64ee8247a83c79cf5f718c584fc1`  
		Last Modified: Tue, 23 Jul 2024 11:11:42 GMT  
		Size: 29.3 KB (29293 bytes)  
		MIME: application/vnd.in-toto+json
