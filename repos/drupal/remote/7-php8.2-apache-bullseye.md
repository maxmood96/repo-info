## `drupal:7-php8.2-apache-bullseye`

```console
$ docker pull drupal@sha256:ffbdc87f309b9847aea9af10c8c9f062e70b70d520de25408a7bb150281ef2d5
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

### `drupal:7-php8.2-apache-bullseye` - linux; amd64

```console
$ docker pull drupal@sha256:bb69f0e9a35a7268cb920f2803c1dabd33e573f55aadbd05d1a7ad70b9d361bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.5 MB (171462821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:745df5b899c3f2bc171802ea77ec8e7d9589f04bf1120100354b4164cd856b27`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 03 Jan 2024 18:58:56 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Wed, 03 Jan 2024 18:58:56 GMT
CMD ["bash"]
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 03 Jan 2024 18:58:56 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 03 Jan 2024 18:58:56 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 03 Jan 2024 18:58:56 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 03 Jan 2024 18:58:56 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 03 Jan 2024 18:58:56 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_VERSION=8.2.14
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.14.tar.xz.asc
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_SHA256=763ecd39fcf51c3815af6ef6e43fa9aa0d0bd8e5a615009e5f4780c92705f583
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 03 Jan 2024 18:58:56 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 03 Jan 2024 18:58:56 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 03 Jan 2024 18:58:56 GMT
RUN docker-php-ext-enable sodium
# Wed, 03 Jan 2024 18:58:56 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 03 Jan 2024 18:58:56 GMT
STOPSIGNAL SIGWINCH
# Wed, 03 Jan 2024 18:58:56 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 03 Jan 2024 18:58:56 GMT
WORKDIR /var/www/html
# Wed, 03 Jan 2024 18:58:56 GMT
EXPOSE 80
# Wed, 03 Jan 2024 18:58:56 GMT
CMD ["apache2-foreground"]
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Jan 2024 18:58:56 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 03 Jan 2024 18:58:56 GMT
ENV DRUPAL_VERSION=7.99
# Wed, 03 Jan 2024 18:58:56 GMT
ENV DRUPAL_URL=https://ftp.drupal.org/files/projects/drupal-7.99.tar.gz
# Wed, 03 Jan 2024 18:58:56 GMT
ENV DRUPAL_MD5=0fbcb06e354309356e6b4e33d2cd242d
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	curl -fSL "$DRUPAL_URL" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff5e264c0172e546465321c8e7e18d28917d577b9ba9e6683a5ffe99b6aa9b5`  
		Last Modified: Thu, 11 Jan 2024 08:46:24 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30198f3cbc20934e9ef32fdefef02e3f1003c53e190223e260e5e595a3776298`  
		Last Modified: Thu, 11 Jan 2024 08:46:37 GMT  
		Size: 91.6 MB (91635933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:028e119b7673aba33f88294bb94929751a3b1e8a7ab4b84dad067d4358a4b7db`  
		Last Modified: Thu, 11 Jan 2024 08:46:24 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61eaf98ab48938fe76599776001808aeab007ee05867ae3c9c0ec61fc9a9fa51`  
		Last Modified: Thu, 11 Jan 2024 08:46:55 GMT  
		Size: 19.3 MB (19259231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f012fec9a3400565cd26117aba1583f3fef4201593561f44761cebabbebe0d`  
		Last Modified: Thu, 11 Jan 2024 08:46:52 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4671d4cdd77de421d143743f5140fa3702c1941a83c9829e0851a56f9ba65a9`  
		Last Modified: Thu, 11 Jan 2024 08:46:52 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aaf0a2fad101965631d3503c7ae7d9779ccc8a990fa740ee97542db3607e470`  
		Last Modified: Thu, 11 Jan 2024 08:55:28 GMT  
		Size: 12.4 MB (12423101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcca3808b500b990c5e1bd9390bf8b263ba3e57286ae1195fb5a68ba118db858`  
		Last Modified: Thu, 11 Jan 2024 08:55:21 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8edd6e2940853f0752f61b566d49acf772d1f2b6e4b192dd5715e43bd0f7b2d6`  
		Last Modified: Thu, 11 Jan 2024 08:55:23 GMT  
		Size: 11.4 MB (11373841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:755d03b897512138d7a4691f55236bab3a3caeb5c176700c1a90d78ce0a4e5ca`  
		Last Modified: Thu, 11 Jan 2024 08:55:21 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f720d39b513bbb504d4065cf0d4089c4a9eb146caa7f191b54695a4ad3965bce`  
		Last Modified: Thu, 11 Jan 2024 08:55:20 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb2d646d6bec3576915f47a76b67ddbba645d262054e4a396a8e71db7dd224ef`  
		Last Modified: Thu, 11 Jan 2024 08:55:20 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c79745aa15894a71c5722cdc6ff85ab9971955a94fb72faf3666bd2f021d79b`  
		Last Modified: Fri, 12 Jan 2024 00:21:20 GMT  
		Size: 1.9 MB (1928006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:081251a9cc920e72ab10955acb2984b3f4ff36b63ef59571ed0dd91f88ad2361`  
		Last Modified: Fri, 12 Jan 2024 00:21:20 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2603fdfa37b07e5282199202b3404903b4a7ce3ed94836d314ca452aded0482a`  
		Last Modified: Fri, 12 Jan 2024 00:21:20 GMT  
		Size: 3.4 MB (3418879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.2-apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:e75b44d940578bddbf531d44f56e1caaf204ff8c26ec3e2901e8807e15cbf0cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5945338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d350650c56e1c834d4cf7bf3429c99fa09765dbfabb2299d44ace0510f2f311`

```dockerfile
```

-	Layers:
	-	`sha256:f0d5af711301be9df58ebe78267143842f4f465df272f3e3a7db4a13ff2a09a9`  
		Last Modified: Fri, 12 Jan 2024 00:21:20 GMT  
		Size: 5.9 MB (5918537 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8c60055ad91d007a6fce6e2c856be6aefa7ecdb2bf29e62870f37138ccf16aa`  
		Last Modified: Fri, 12 Jan 2024 00:21:20 GMT  
		Size: 26.8 KB (26801 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-php8.2-apache-bullseye` - linux; arm variant v5

```console
$ docker pull drupal@sha256:c65cebe89b78e003dcf23cea68dfb48d3991f6defa6ea03a9497411a577e8b34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.8 MB (148794190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1aec6e775733fc0d5cf1e2f9e2dbfccc6d85b8f7ed65194bc8fe645a0e03ad55`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 03 Jan 2024 18:58:56 GMT
ADD file:771e145a148ba6b03341b2263d20ecc38b89c367acc660ed985638987faa0ae5 in / 
# Wed, 03 Jan 2024 18:58:56 GMT
CMD ["bash"]
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 03 Jan 2024 18:58:56 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 03 Jan 2024 18:58:56 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 03 Jan 2024 18:58:56 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 03 Jan 2024 18:58:56 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 03 Jan 2024 18:58:56 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_VERSION=8.2.15
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.15.tar.xz.asc
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_SHA256=eca5deac02d77d806838275f8a3024b38b35ac0a5d9853dcc71c6cbe3f1f8765
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 03 Jan 2024 18:58:56 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 03 Jan 2024 18:58:56 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 03 Jan 2024 18:58:56 GMT
RUN docker-php-ext-enable sodium
# Wed, 03 Jan 2024 18:58:56 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 03 Jan 2024 18:58:56 GMT
STOPSIGNAL SIGWINCH
# Wed, 03 Jan 2024 18:58:56 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 03 Jan 2024 18:58:56 GMT
WORKDIR /var/www/html
# Wed, 03 Jan 2024 18:58:56 GMT
EXPOSE 80
# Wed, 03 Jan 2024 18:58:56 GMT
CMD ["apache2-foreground"]
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Jan 2024 18:58:56 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 03 Jan 2024 18:58:56 GMT
ENV DRUPAL_VERSION=7.99
# Wed, 03 Jan 2024 18:58:56 GMT
ENV DRUPAL_URL=https://ftp.drupal.org/files/projects/drupal-7.99.tar.gz
# Wed, 03 Jan 2024 18:58:56 GMT
ENV DRUPAL_MD5=0fbcb06e354309356e6b4e33d2cd242d
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	curl -fSL "$DRUPAL_URL" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:05919bd913f54ba9a5204c51fd89eb54126c4f3f9bf6f1f53f67bd19652a4d14`  
		Last Modified: Thu, 11 Jan 2024 01:54:52 GMT  
		Size: 28.9 MB (28921224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70cdaa16889fb116b489c106bef6ab54a0c5cd8610d158f868d0a402490a8f15`  
		Last Modified: Thu, 11 Jan 2024 06:33:13 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14ef0bf378129c59f6e7cd5a5fee5abf53e89d9c40c60294151e105efcdd677a`  
		Last Modified: Thu, 11 Jan 2024 06:33:33 GMT  
		Size: 73.7 MB (73690275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:288221f74789a7fbe6f8d464aab644d9946f97fd2d2adb69bfaba78be7fc3dd7`  
		Last Modified: Thu, 11 Jan 2024 06:33:13 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63a0ffe128d6b1f379bd0b3a8b29252e77df1aff289613a7f7ab70e6b03f8cd0`  
		Last Modified: Thu, 11 Jan 2024 06:33:55 GMT  
		Size: 18.6 MB (18559001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f855800e41388a7120357e3f392008d78a7bd95e7cd6a8727262a2bc1b044981`  
		Last Modified: Thu, 11 Jan 2024 06:33:49 GMT  
		Size: 476.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e9b687f3eff21f4bdb840ab1a6aa77ac16774d68b8c112a163445dc8e4de4b5`  
		Last Modified: Thu, 11 Jan 2024 06:33:49 GMT  
		Size: 516.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de6b1c994fbe01e6f5a90af24ec3fccd93b058d5ad4d4b1feaffa2a250ed496e`  
		Last Modified: Fri, 19 Jan 2024 23:55:55 GMT  
		Size: 12.4 MB (12415046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c3eec954088c35828e2d73e1d09466a1c024e35f765672661856533f426c85`  
		Last Modified: Fri, 19 Jan 2024 23:55:51 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7758652d775ea68a5b59754af103cbb7a19596aa337a6b27d6931e0591a5e6e7`  
		Last Modified: Fri, 19 Jan 2024 23:55:56 GMT  
		Size: 10.4 MB (10364673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7818b7df0e939d24998488dbd37b07343a5e5aaf736f0f78b4f9ff2692fd4584`  
		Last Modified: Fri, 19 Jan 2024 23:55:52 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bba9e7b63839e03dc1e42d7e1f6ec6900e06e9178372b57699c156bd3a234ac3`  
		Last Modified: Fri, 19 Jan 2024 23:55:51 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2b901a67c041db4a01dae72ce8fdefc5ad886767dd4296180c589cdcbc957b0`  
		Last Modified: Fri, 19 Jan 2024 23:55:51 GMT  
		Size: 897.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0aae5363a0000f28e4df2a6425d538466efaa446fe0e1dc38742265bac59768`  
		Last Modified: Sat, 20 Jan 2024 01:41:28 GMT  
		Size: 1.4 MB (1419192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cb27086af4f501ca3d71d55ce66b45d6f1faae899ee74f2f721d8e32224a079`  
		Last Modified: Sat, 20 Jan 2024 01:41:28 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1f39493503f83f62b9f7b341e61b1cc278d0a69c9873b14fd11a54326bc1d32`  
		Last Modified: Sat, 20 Jan 2024 01:41:28 GMT  
		Size: 3.4 MB (3418881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.2-apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:ee05fa47412af341b6220d6208de6c2daf87746c5db521587c8a03ced82f2af1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5775951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e756f8f74592a18634ed96c2f6205882464846e203f5fc179123bf789da9528`

```dockerfile
```

-	Layers:
	-	`sha256:eccc5e451c310af47452aeb98329c56e4cadfa0f5162e5a462151eedc3438967`  
		Last Modified: Sat, 20 Jan 2024 01:41:26 GMT  
		Size: 5.7 MB (5749071 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:527334bc995c60baf14bd22edad8f6f219b235b554a4faa123c1810f056757d0`  
		Last Modified: Sat, 20 Jan 2024 01:41:26 GMT  
		Size: 26.9 KB (26880 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-php8.2-apache-bullseye` - linux; arm variant v7

```console
$ docker pull drupal@sha256:ba4cd00ac170f8582355eec0a4235fcc158d7e60ee9f90353859ab383e9a91a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.9 MB (140906834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b7952be4c5832b58f69a9b0636ee1d7584bc831dceb2b255192f8c153c91836`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 03 Jan 2024 18:58:56 GMT
ADD file:1a36d919bfcbaa6b981b71ce99d777d303e69c2d6cb1924992e5a9cd811c11c5 in / 
# Wed, 03 Jan 2024 18:58:56 GMT
CMD ["bash"]
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 03 Jan 2024 18:58:56 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 03 Jan 2024 18:58:56 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 03 Jan 2024 18:58:56 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 03 Jan 2024 18:58:56 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 03 Jan 2024 18:58:56 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_VERSION=8.2.14
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.14.tar.xz.asc
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_SHA256=763ecd39fcf51c3815af6ef6e43fa9aa0d0bd8e5a615009e5f4780c92705f583
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 03 Jan 2024 18:58:56 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 03 Jan 2024 18:58:56 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 03 Jan 2024 18:58:56 GMT
RUN docker-php-ext-enable sodium
# Wed, 03 Jan 2024 18:58:56 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 03 Jan 2024 18:58:56 GMT
STOPSIGNAL SIGWINCH
# Wed, 03 Jan 2024 18:58:56 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 03 Jan 2024 18:58:56 GMT
WORKDIR /var/www/html
# Wed, 03 Jan 2024 18:58:56 GMT
EXPOSE 80
# Wed, 03 Jan 2024 18:58:56 GMT
CMD ["apache2-foreground"]
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Jan 2024 18:58:56 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 03 Jan 2024 18:58:56 GMT
ENV DRUPAL_VERSION=7.99
# Wed, 03 Jan 2024 18:58:56 GMT
ENV DRUPAL_URL=https://ftp.drupal.org/files/projects/drupal-7.99.tar.gz
# Wed, 03 Jan 2024 18:58:56 GMT
ENV DRUPAL_MD5=0fbcb06e354309356e6b4e33d2cd242d
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	curl -fSL "$DRUPAL_URL" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:d976170654fe1bc717306b8bf14dc57d20e331b13e4797bc137e6911aa745a8a`  
		Last Modified: Thu, 11 Jan 2024 02:49:26 GMT  
		Size: 26.6 MB (26578974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4701722b879f62d8acba3f8f3e1112876a738a749abfbde91ff32668b97cf48`  
		Last Modified: Thu, 11 Jan 2024 11:13:35 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e27838f64e10b5768426c27a39253117c59cb617ecc2fc587aa0bece98752be1`  
		Last Modified: Thu, 11 Jan 2024 11:13:53 GMT  
		Size: 69.3 MB (69323950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b810c0b57076bb8a1f72f3f179e7a2e4f0279044a8c0a4db6cef528ffa6f409b`  
		Last Modified: Thu, 11 Jan 2024 11:13:35 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ecc7baa51643afebc5e0413f8d05d0acbf14de84e8c9803df60cd1d9c933b16`  
		Last Modified: Thu, 11 Jan 2024 11:14:14 GMT  
		Size: 18.0 MB (18017964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:374cc8ec493398d012ceb45f0bde0f1cefd2293900779585b332fdc7b7e31cc9`  
		Last Modified: Thu, 11 Jan 2024 11:14:09 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13b22b3e63f59f773e3514cf66caf552a14afac7d05be7aae1a18debdc685226`  
		Last Modified: Thu, 11 Jan 2024 11:14:09 GMT  
		Size: 514.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a1e57808bb5a5194d17d1041c7f02b90764a12669976e4f0ae308550e90e23`  
		Last Modified: Thu, 11 Jan 2024 11:23:40 GMT  
		Size: 12.4 MB (12421614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8622c0a7f11be90eee1399f4bdce82de79f59be0ee4eaf2ea9a78c47d6a325f`  
		Last Modified: Thu, 11 Jan 2024 11:23:37 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff70fb1b09b3f6762898dba9246c77b8827c07ae743e986032607bb68078d472`  
		Last Modified: Thu, 11 Jan 2024 11:23:40 GMT  
		Size: 9.8 MB (9830155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a6e846989d393d20d20c93c687b7d34415690abc42a91bc265fab21a06db11`  
		Last Modified: Thu, 11 Jan 2024 11:23:37 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf14bb302e34e00ad773f554e083b35b914c52f98a6b76d775d3e9be4d0d4212`  
		Last Modified: Thu, 11 Jan 2024 11:23:37 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9509aa59cdcd9d41e189263a1556e0406bf108df2ff1659751c6b488010a7bc5`  
		Last Modified: Thu, 11 Jan 2024 11:23:37 GMT  
		Size: 895.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83c46c65780888f1168a24069cc760d7557700bdb7661eb7d6e7bab1e7429f2b`  
		Last Modified: Fri, 12 Jan 2024 03:34:58 GMT  
		Size: 1.3 MB (1309410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c39240dba05e243fdb6bdac1de1415bad9dc359ee8eaea541a8a5d5455d86bba`  
		Last Modified: Fri, 12 Jan 2024 03:34:57 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c1913b254a195b032b56099aebf1b1a45bcb403b3c8e76ac7f8785c0a294bb1`  
		Last Modified: Fri, 12 Jan 2024 04:18:19 GMT  
		Size: 3.4 MB (3418877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.2-apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:597811cbfd41ce45f5650c3afb7130d5f6103d89e50b0b11bab5bab73b639e29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5777756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bf7f1aa56c1f55de37940565acd1ef258788f5d266c674b26d200678c42f491`

```dockerfile
```

-	Layers:
	-	`sha256:d4b419aa9f85e65b1906b983b206cdf701aa686a1a9296928cfae4d81461c682`  
		Last Modified: Fri, 12 Jan 2024 04:18:19 GMT  
		Size: 5.8 MB (5752989 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dec7b64fe9459ff606136d0b912e250ac30fa5d79d2d180fd6fe81aab04ee74`  
		Last Modified: Fri, 12 Jan 2024 04:18:18 GMT  
		Size: 24.8 KB (24767 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-php8.2-apache-bullseye` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:84e5fa125d61698ba88ad7394d07d87cbb9ff0a81432a306f6181492fb5f04f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.7 MB (165676210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a20791a00e4d8510ba0010ae9ff18b806bbcebd74dbff33b63b657d6a7d65be`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 03 Jan 2024 18:58:56 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Wed, 03 Jan 2024 18:58:56 GMT
CMD ["bash"]
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 03 Jan 2024 18:58:56 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 03 Jan 2024 18:58:56 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 03 Jan 2024 18:58:56 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 03 Jan 2024 18:58:56 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 03 Jan 2024 18:58:56 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_VERSION=8.2.14
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.14.tar.xz.asc
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_SHA256=763ecd39fcf51c3815af6ef6e43fa9aa0d0bd8e5a615009e5f4780c92705f583
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 03 Jan 2024 18:58:56 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 03 Jan 2024 18:58:56 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 03 Jan 2024 18:58:56 GMT
RUN docker-php-ext-enable sodium
# Wed, 03 Jan 2024 18:58:56 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 03 Jan 2024 18:58:56 GMT
STOPSIGNAL SIGWINCH
# Wed, 03 Jan 2024 18:58:56 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 03 Jan 2024 18:58:56 GMT
WORKDIR /var/www/html
# Wed, 03 Jan 2024 18:58:56 GMT
EXPOSE 80
# Wed, 03 Jan 2024 18:58:56 GMT
CMD ["apache2-foreground"]
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Jan 2024 18:58:56 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 03 Jan 2024 18:58:56 GMT
ENV DRUPAL_VERSION=7.99
# Wed, 03 Jan 2024 18:58:56 GMT
ENV DRUPAL_URL=https://ftp.drupal.org/files/projects/drupal-7.99.tar.gz
# Wed, 03 Jan 2024 18:58:56 GMT
ENV DRUPAL_MD5=0fbcb06e354309356e6b4e33d2cd242d
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	curl -fSL "$DRUPAL_URL" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84b5325d41b2385184a6306452d88092af1b9bbfba4f3b0eee422401e32a046f`  
		Last Modified: Thu, 11 Jan 2024 05:47:39 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bb4a656112423f6afce0d53ff1563ed8e9094e719e9590770f0eab9c6a89695`  
		Last Modified: Thu, 11 Jan 2024 05:47:48 GMT  
		Size: 86.9 MB (86934767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ace44d987c8de3ac442ad478520d128bad0094fa80c8ac8d7dc5e10d3239209`  
		Last Modified: Thu, 11 Jan 2024 05:47:39 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5963881fd5d9f54e5ca1b0d73c4c96df373b8b4c68a1cdd61d3af11ab9792ef6`  
		Last Modified: Thu, 11 Jan 2024 05:48:05 GMT  
		Size: 19.2 MB (19177584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91087cec2aa1b213cd5a3068f27281814a5b3e676eb2f6bbfec477b4fa373e1d`  
		Last Modified: Thu, 11 Jan 2024 05:48:03 GMT  
		Size: 472.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e83e4e1be1e626e407783ca667d5cb594fdeee2ae6018ccb2754dc1aaf8cc8a`  
		Last Modified: Thu, 11 Jan 2024 05:48:03 GMT  
		Size: 513.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22ebfaf20ce0cb372e76d3a59bff950e53491b0e437c4f86ed4e92082f8399bd`  
		Last Modified: Thu, 11 Jan 2024 05:56:01 GMT  
		Size: 12.4 MB (12422381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6720545e60b26d2c1c80c7f6026e5722c80f6a862d052bae0198087a2c595c27`  
		Last Modified: Thu, 11 Jan 2024 05:55:58 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:325aede01a984b740c6971b563e6b37ba2527bff43c3b7c5808aabe5c850c102`  
		Last Modified: Thu, 11 Jan 2024 05:56:00 GMT  
		Size: 11.5 MB (11459098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c19db3eb2da59957400a77809bc150a2f6d4fa329bed571624dac68998303618`  
		Last Modified: Thu, 11 Jan 2024 05:55:58 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4554875193d42c145f474bdb79284b3c48dd1a1c666f5a8e9b4bc76afb3edb97`  
		Last Modified: Thu, 11 Jan 2024 05:55:58 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2afeb9ab91ee345fe8a7aad686ddf23aec63abf407e144f5697da3552e326d24`  
		Last Modified: Thu, 11 Jan 2024 05:55:58 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c63d842cd296d71b1a6a4f15e4b27ae0450a5e2b7d7a903a6d729a166cc7226`  
		Last Modified: Fri, 12 Jan 2024 01:17:33 GMT  
		Size: 2.2 MB (2193627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7554931f9fa5146e30f01e87a1ff3e2ac3eb206e95f2ae0b6a8ace5728d5958`  
		Last Modified: Fri, 12 Jan 2024 01:17:33 GMT  
		Size: 309.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13011131bfd1fc14a3bf82ab202284bd3a10c556f97f176fd8fe9db37b94ad74`  
		Last Modified: Fri, 12 Jan 2024 01:30:49 GMT  
		Size: 3.4 MB (3418877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.2-apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:47c198fcbc9d9419c9b194d978e22efec88bedb9210e3bf5bf6adcd8dbb01f3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5945920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f968e7e3b36a821682d278b42069410da5e6dd43318a058565495b290c3ea892`

```dockerfile
```

-	Layers:
	-	`sha256:0535a8edd1d8958d47eb175816adb31ee32cc63d3dcee69710bece6c04cd2089`  
		Last Modified: Fri, 12 Jan 2024 01:30:49 GMT  
		Size: 5.9 MB (5921221 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44cddac76e28aa6537435a3d494110d9d6d2503747b30c7eefb309ab6a955a41`  
		Last Modified: Fri, 12 Jan 2024 01:30:49 GMT  
		Size: 24.7 KB (24699 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-php8.2-apache-bullseye` - linux; 386

```console
$ docker pull drupal@sha256:866b8b4205c8562ac8a76d78a95e8eb80137f349db99f764fd04bb83db25dd78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.3 MB (174335220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a88d2e52110c4f257b738f44d9b1633a859718829792c4006be5b7ff98a66483`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 03 Jan 2024 18:58:56 GMT
ADD file:ed1ce84cc05c621c3311366a5ef8f9ed36bdff95d75ee1564c10e7a20f993b61 in / 
# Wed, 03 Jan 2024 18:58:56 GMT
CMD ["bash"]
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 03 Jan 2024 18:58:56 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 03 Jan 2024 18:58:56 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 03 Jan 2024 18:58:56 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 03 Jan 2024 18:58:56 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 03 Jan 2024 18:58:56 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_VERSION=8.2.14
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.14.tar.xz.asc
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_SHA256=763ecd39fcf51c3815af6ef6e43fa9aa0d0bd8e5a615009e5f4780c92705f583
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 03 Jan 2024 18:58:56 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 03 Jan 2024 18:58:56 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 03 Jan 2024 18:58:56 GMT
RUN docker-php-ext-enable sodium
# Wed, 03 Jan 2024 18:58:56 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 03 Jan 2024 18:58:56 GMT
STOPSIGNAL SIGWINCH
# Wed, 03 Jan 2024 18:58:56 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 03 Jan 2024 18:58:56 GMT
WORKDIR /var/www/html
# Wed, 03 Jan 2024 18:58:56 GMT
EXPOSE 80
# Wed, 03 Jan 2024 18:58:56 GMT
CMD ["apache2-foreground"]
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Jan 2024 18:58:56 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 03 Jan 2024 18:58:56 GMT
ENV DRUPAL_VERSION=7.99
# Wed, 03 Jan 2024 18:58:56 GMT
ENV DRUPAL_URL=https://ftp.drupal.org/files/projects/drupal-7.99.tar.gz
# Wed, 03 Jan 2024 18:58:56 GMT
ENV DRUPAL_MD5=0fbcb06e354309356e6b4e33d2cd242d
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	curl -fSL "$DRUPAL_URL" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:d19cbf7b148868960150824d1e6f8ebc5f6d7542a422061491e92178f7db879b`  
		Last Modified: Thu, 11 Jan 2024 02:44:06 GMT  
		Size: 32.4 MB (32402672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:587efb275ebb74b2c5c7e4487c410281d4aeed19ced5f2582a504c4c690060bc`  
		Last Modified: Thu, 11 Jan 2024 09:13:16 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66518b377d9afc7d2be5fb2882f5697822432b0fc3141b67a6f49e93efb7801d`  
		Last Modified: Thu, 11 Jan 2024 09:13:39 GMT  
		Size: 92.7 MB (92726316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:949f2dd63a58425c29e2f92e53dca3ef43798194a0922ff21cdd4383c4ff57a7`  
		Last Modified: Thu, 11 Jan 2024 09:13:16 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f817f39508cea3046138ff5d0a4918da094553d27b0656f48184542f292d79c`  
		Last Modified: Thu, 11 Jan 2024 09:13:58 GMT  
		Size: 19.7 MB (19745310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8046853bb5590cea852148e7ab1821fb87a76a5ccd13bbeecaa41d45cdc351e`  
		Last Modified: Thu, 11 Jan 2024 09:13:54 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93bf9f1473e891db44de5b90280734858a003ef4764a59a8c500f7557e22166c`  
		Last Modified: Thu, 11 Jan 2024 09:13:54 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca2f635b7f14b94901bdf985445cc5799e3871729f0976a67f61f64468848aa6`  
		Last Modified: Thu, 11 Jan 2024 09:23:25 GMT  
		Size: 12.4 MB (12422403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c17f26c88f81330287e2bf2f449aed07e6631a1b5d2bf5f82ba10aa9e57083c`  
		Last Modified: Thu, 11 Jan 2024 09:23:22 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4736070ff7155cae565753f3ba4c787c9abeed8a0426a92dc6bc47a38f8e8f3`  
		Last Modified: Thu, 11 Jan 2024 09:23:26 GMT  
		Size: 11.6 MB (11617831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b54eb78c4e4d8b8fcea95b968ef5905ffa2907a688a8a9dd532825aa6146daa`  
		Last Modified: Thu, 11 Jan 2024 09:23:22 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:463d1358c3eabf5c6081a77e0ec961ae1facfe5e9e9d9d1fab8894f115bdc8bb`  
		Last Modified: Thu, 11 Jan 2024 09:23:22 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f090dd92b3fbc132e0478808845f9dd7dafc0a8f980ec968f8199363aa7d357e`  
		Last Modified: Thu, 11 Jan 2024 09:23:22 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c61ad7c8949be8d8555f6aebf8c29e1a37423d07b5b1a765802d086ab881a5dd`  
		Last Modified: Fri, 12 Jan 2024 00:21:21 GMT  
		Size: 2.0 MB (1995923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:169051137e7cf64b19206e555a6e2dc638d20e6613d259ee2a452741d3f15e0e`  
		Last Modified: Fri, 12 Jan 2024 00:21:21 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:457f4d35ee298d106e320e8d9a37a62611f5c52f84d1f9e84f91667608043d87`  
		Last Modified: Fri, 12 Jan 2024 00:21:22 GMT  
		Size: 3.4 MB (3418877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.2-apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:2960c2f2430e9ced70289d6902c2ee33df8b5c833cc9bfcae36ca24b456a63b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5936429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baeb0e5138557e4ab8ff87c89880450be94f1d8fc739c6e36bb194119502125c`

```dockerfile
```

-	Layers:
	-	`sha256:bbdcad2ed36691d05d1ed487d23285bbe275eefb4b0f7877dfc9bf98c4108d65`  
		Last Modified: Fri, 12 Jan 2024 00:21:21 GMT  
		Size: 5.9 MB (5909651 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:340412568fc51061eb745b9ca26241bfc6bd6c222c0d0c34a0f8cce2b8bb0ee2`  
		Last Modified: Fri, 12 Jan 2024 00:21:20 GMT  
		Size: 26.8 KB (26778 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-php8.2-apache-bullseye` - linux; mips64le

```console
$ docker pull drupal@sha256:71ca6e5efc9b44952fe0275edce0e8d699a31ae56700be7f59164a119dca2ad8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.1 MB (148054469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23eec0c7c1f997e94cbf4b4c005c11676f2d1c481d7f87e41b5088a082f08a4e`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 03 Jan 2024 18:58:56 GMT
ADD file:45b54e9ac99d4bf84139a07fe13fb123e60dcc91036e007820f717e6ef708912 in / 
# Wed, 03 Jan 2024 18:58:56 GMT
CMD ["bash"]
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 03 Jan 2024 18:58:56 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 03 Jan 2024 18:58:56 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 03 Jan 2024 18:58:56 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 03 Jan 2024 18:58:56 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 03 Jan 2024 18:58:56 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_VERSION=8.2.14
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.14.tar.xz.asc
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_SHA256=763ecd39fcf51c3815af6ef6e43fa9aa0d0bd8e5a615009e5f4780c92705f583
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 03 Jan 2024 18:58:56 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 03 Jan 2024 18:58:56 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 03 Jan 2024 18:58:56 GMT
RUN docker-php-ext-enable sodium
# Wed, 03 Jan 2024 18:58:56 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 03 Jan 2024 18:58:56 GMT
STOPSIGNAL SIGWINCH
# Wed, 03 Jan 2024 18:58:56 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 03 Jan 2024 18:58:56 GMT
WORKDIR /var/www/html
# Wed, 03 Jan 2024 18:58:56 GMT
EXPOSE 80
# Wed, 03 Jan 2024 18:58:56 GMT
CMD ["apache2-foreground"]
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Jan 2024 18:58:56 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 03 Jan 2024 18:58:56 GMT
ENV DRUPAL_VERSION=7.99
# Wed, 03 Jan 2024 18:58:56 GMT
ENV DRUPAL_URL=https://ftp.drupal.org/files/projects/drupal-7.99.tar.gz
# Wed, 03 Jan 2024 18:58:56 GMT
ENV DRUPAL_MD5=0fbcb06e354309356e6b4e33d2cd242d
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	curl -fSL "$DRUPAL_URL" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:ba6b58b3ef4d7a81d629337604645ba2efe91a5e812edd9e2fa732c0647f6f3c`  
		Last Modified: Thu, 11 Jan 2024 02:24:20 GMT  
		Size: 29.6 MB (29636033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:470c850da7112483294a47c6d6048b6a409781fbec5e501be5e81508943a0147`  
		Last Modified: Thu, 11 Jan 2024 17:19:07 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3215d2c8396cf2659def5c824c0e3eaeb1fef5d1615a7faed7724bab6b3e46f7`  
		Last Modified: Thu, 11 Jan 2024 17:19:58 GMT  
		Size: 71.8 MB (71815007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df839afcfb5ebe7f388c427e4b4625908d8cbd05ecb4edec39d71207a107e0b8`  
		Last Modified: Thu, 11 Jan 2024 17:19:07 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d71f82a89d2364794730f1ffcf1e4fdccc177f91cce9a5fa51f875c492861e81`  
		Last Modified: Thu, 11 Jan 2024 17:20:31 GMT  
		Size: 19.0 MB (18955448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da33a0534be19a1ebf2cb1311a726c624800d16c8da391d544bc00f86dbd7bb9`  
		Last Modified: Thu, 11 Jan 2024 17:20:18 GMT  
		Size: 437.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c6159708b2267e689a6aa133c3cb54ff2f4a826b4da0bc34ce9247b053b47f9`  
		Last Modified: Thu, 11 Jan 2024 17:20:18 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45080d7cc1aead04e5b594284e5e27e8d45eb4bdd8db858cba6d8e2e98d55670`  
		Last Modified: Thu, 11 Jan 2024 17:34:46 GMT  
		Size: 12.2 MB (12203931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e841dd88b0c393073546d1fdfc78eaa6cc740b478cf1fc9c8568d908c1bb5c01`  
		Last Modified: Thu, 11 Jan 2024 17:34:40 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:020088a2eb01d38ce6dc25c5255433d3a793c5a79df1c41da03303fd8e742f95`  
		Last Modified: Thu, 11 Jan 2024 17:34:49 GMT  
		Size: 10.5 MB (10501746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb0eb82773dc2e3bc1ded2b4ecb4dcf1fe26a46a5066001380197d886338ccbc`  
		Last Modified: Thu, 11 Jan 2024 17:34:40 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:919b04ee4c827e8b387ab61546087efc8cef87edcdccf1a251fa54589e50a1c0`  
		Last Modified: Thu, 11 Jan 2024 17:34:40 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e670a87b3a988850e33fc24a3e86541695643c3da413bbc4332b76a808e4c8ee`  
		Last Modified: Thu, 11 Jan 2024 17:34:40 GMT  
		Size: 895.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e83fae572e3d9439a5c7d2abe6cd72bc3f5a488679b55bb4a566fd5b19f43b6`  
		Last Modified: Fri, 12 Jan 2024 01:40:39 GMT  
		Size: 1.5 MB (1517640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dee2913d05988b962db4916f07cfc955a33cedc1fde642d3a4ecba0dee6e0da`  
		Last Modified: Fri, 12 Jan 2024 01:40:40 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f78b68d2d871d180fac3a0bc24ea05b95ffec390e5a9765f85ff97863e8ce5f`  
		Last Modified: Fri, 12 Jan 2024 01:40:40 GMT  
		Size: 3.4 MB (3418877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.2-apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:af155e84a9e99cc1f8232ee48434e758a6d91d76f2a009c8bdbc71f7ff4337f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.6 KB (26630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54cdee0f1a44da7984964fd770b667e6cc33c5817ffa4c430dbe03be2b08043d`

```dockerfile
```

-	Layers:
	-	`sha256:91f9c5577fc16539c693728ff632b59a5a0c05f9fee282747302566a5ef17f74`  
		Last Modified: Fri, 12 Jan 2024 01:40:31 GMT  
		Size: 26.6 KB (26630 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-php8.2-apache-bullseye` - linux; ppc64le

```console
$ docker pull drupal@sha256:e9e78e7b2931796f0d7a919681ebb24dd87ea334a1c8501d4604da23f423a609
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.9 MB (171894732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d1c6883f18ee6503c68fc44797352cee71fa17a9f18fa05d07d6eb53458cc3b`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 03 Jan 2024 18:58:56 GMT
ADD file:577ec786dad9a86344b678e69a7f514c3deede7cc45d9b3c9088449060272d55 in / 
# Wed, 03 Jan 2024 18:58:56 GMT
CMD ["bash"]
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 03 Jan 2024 18:58:56 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 03 Jan 2024 18:58:56 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 03 Jan 2024 18:58:56 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 03 Jan 2024 18:58:56 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 03 Jan 2024 18:58:56 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_VERSION=8.2.14
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.14.tar.xz.asc
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_SHA256=763ecd39fcf51c3815af6ef6e43fa9aa0d0bd8e5a615009e5f4780c92705f583
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 03 Jan 2024 18:58:56 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 03 Jan 2024 18:58:56 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 03 Jan 2024 18:58:56 GMT
RUN docker-php-ext-enable sodium
# Wed, 03 Jan 2024 18:58:56 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 03 Jan 2024 18:58:56 GMT
STOPSIGNAL SIGWINCH
# Wed, 03 Jan 2024 18:58:56 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 03 Jan 2024 18:58:56 GMT
WORKDIR /var/www/html
# Wed, 03 Jan 2024 18:58:56 GMT
EXPOSE 80
# Wed, 03 Jan 2024 18:58:56 GMT
CMD ["apache2-foreground"]
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Jan 2024 18:58:56 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 03 Jan 2024 18:58:56 GMT
ENV DRUPAL_VERSION=7.99
# Wed, 03 Jan 2024 18:58:56 GMT
ENV DRUPAL_URL=https://ftp.drupal.org/files/projects/drupal-7.99.tar.gz
# Wed, 03 Jan 2024 18:58:56 GMT
ENV DRUPAL_MD5=0fbcb06e354309356e6b4e33d2cd242d
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	curl -fSL "$DRUPAL_URL" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:4c9dbec0f2ecfefcce502a32967ad48a18396e58a4950f972d672b4d95c84bcc`  
		Last Modified: Thu, 11 Jan 2024 02:40:16 GMT  
		Size: 35.3 MB (35293800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c7190f696a06c78ee7b8deeea3a247e10855f7dd84a61900697e3359f2b9ae3`  
		Last Modified: Thu, 11 Jan 2024 06:48:52 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a066abb8a86243926ebf74c3212ff59c1482a22c4c7d15cd7405284de0862f8e`  
		Last Modified: Thu, 11 Jan 2024 06:49:06 GMT  
		Size: 86.6 MB (86644384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24429c3ab51c9b2d86867d99d49ce1421723a0d5b783b3a1fdc35ee37c3e1bb7`  
		Last Modified: Thu, 11 Jan 2024 06:48:51 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab235fcee54ef75691b605c36f973ae4ef670c60c51fc322797a934ed7ccf853`  
		Last Modified: Thu, 11 Jan 2024 06:49:27 GMT  
		Size: 20.5 MB (20475113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d51d2ce52ac2db42ded5f9cc92ab63f93b2ccaa74ad82fc73eec61b31d5586e`  
		Last Modified: Thu, 11 Jan 2024 06:49:23 GMT  
		Size: 475.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2486e5eebed1eee65cc5d5a20f26fd74b8bc4ba08d1903dc7d10deb2df3a5786`  
		Last Modified: Thu, 11 Jan 2024 06:49:23 GMT  
		Size: 516.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2407f6ae65c158043a235443b23dbdea1f2d241049227fe94d9dd49bd36d2fa`  
		Last Modified: Thu, 11 Jan 2024 06:58:40 GMT  
		Size: 12.4 MB (12423188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b44253f4e4da91af2255451dc7bf750e0997883ecc0fa9b2c177cd051449803b`  
		Last Modified: Thu, 11 Jan 2024 06:58:37 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef92d6a6deed0655abce57406f3d9a72c795d6eafed96c2659fe6ec9601a6501`  
		Last Modified: Thu, 11 Jan 2024 06:58:40 GMT  
		Size: 11.8 MB (11838954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff4648562aa5ce98cb88b0a0702ad5308eeaa83152b0bf49c2d3399aed686b6e`  
		Last Modified: Thu, 11 Jan 2024 06:58:37 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b208ad48fcf768cd7630ac2b8356a94d73bd8b8c2899a9271d1e61911426fe9`  
		Last Modified: Thu, 11 Jan 2024 06:58:37 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4bbfe6bfb8298c5d56991d687b5ca693262ae0ce52487faf4ef17438a279a6`  
		Last Modified: Thu, 11 Jan 2024 06:58:37 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f949a07688c06925f169039d9eef755c25547c0a9e6bc78212f3e9791f9d74b6`  
		Last Modified: Fri, 12 Jan 2024 01:09:13 GMT  
		Size: 1.8 MB (1794524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f42476d29786ad50b14ff877fbdc2d015379e59a695eccf2ce76f4557682f9d0`  
		Last Modified: Fri, 12 Jan 2024 01:09:13 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:843585a7985350c9ebfdec3586272e011545e7336d7adfc88700e04cf13adc9d`  
		Last Modified: Fri, 12 Jan 2024 01:30:51 GMT  
		Size: 3.4 MB (3418878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.2-apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:f9aa15a270464f24fb061ef61aeaa6f1dbe70d25036bb73574269a93abf54ac3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5915125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0d7a82943819e26e48ffd8a1552b9e4f575b96a3e1351c99e87d36c7cde1a31`

```dockerfile
```

-	Layers:
	-	`sha256:ad792f06bfce60f6db7ba212f7a2e7eac6b16ceedb6bcc15b0fafed9815368fa`  
		Last Modified: Fri, 12 Jan 2024 01:30:51 GMT  
		Size: 5.9 MB (5890402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79993eb00e499cab827b9a320ddcb367f9408770ccbc910265323850aa88b567`  
		Last Modified: Fri, 12 Jan 2024 01:30:50 GMT  
		Size: 24.7 KB (24723 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-php8.2-apache-bullseye` - linux; s390x

```console
$ docker pull drupal@sha256:72377a633a23d0abc43d7a17cfe091dfdca1c31a7379f49b3bb69c790c8a30a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.2 MB (148232986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cef493d1bfb2e9588fba4946412568973f43685c8b5f907cc0ce118a11ad909`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 03 Jan 2024 18:58:56 GMT
ADD file:77a92d4e9397475a6c68f4341baba607a7c875bc6e252de3e096482dd074f8ca in / 
# Wed, 03 Jan 2024 18:58:56 GMT
CMD ["bash"]
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 03 Jan 2024 18:58:56 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 03 Jan 2024 18:58:56 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 03 Jan 2024 18:58:56 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 03 Jan 2024 18:58:56 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 03 Jan 2024 18:58:56 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_VERSION=8.2.14
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.14.tar.xz.asc
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_SHA256=763ecd39fcf51c3815af6ef6e43fa9aa0d0bd8e5a615009e5f4780c92705f583
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 03 Jan 2024 18:58:56 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 03 Jan 2024 18:58:56 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 03 Jan 2024 18:58:56 GMT
RUN docker-php-ext-enable sodium
# Wed, 03 Jan 2024 18:58:56 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 03 Jan 2024 18:58:56 GMT
STOPSIGNAL SIGWINCH
# Wed, 03 Jan 2024 18:58:56 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 03 Jan 2024 18:58:56 GMT
WORKDIR /var/www/html
# Wed, 03 Jan 2024 18:58:56 GMT
EXPOSE 80
# Wed, 03 Jan 2024 18:58:56 GMT
CMD ["apache2-foreground"]
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Jan 2024 18:58:56 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 03 Jan 2024 18:58:56 GMT
ENV DRUPAL_VERSION=7.99
# Wed, 03 Jan 2024 18:58:56 GMT
ENV DRUPAL_URL=https://ftp.drupal.org/files/projects/drupal-7.99.tar.gz
# Wed, 03 Jan 2024 18:58:56 GMT
ENV DRUPAL_MD5=0fbcb06e354309356e6b4e33d2cd242d
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	curl -fSL "$DRUPAL_URL" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:a8470cec8ee9510bf45556c756635d84eb3cbc0220b52812522196008c6b0d3e`  
		Last Modified: Thu, 11 Jan 2024 01:51:19 GMT  
		Size: 29.7 MB (29656884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1f6dbf1cfe3c4cbdeae3c718a8017076eaafaeaa7f851fffee6a65e9b3a26d7`  
		Last Modified: Thu, 11 Jan 2024 08:19:13 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b3af4afd42fce7a72940da0adb8f8d962357fc71a6c302548a904593f830d59`  
		Last Modified: Thu, 11 Jan 2024 08:19:23 GMT  
		Size: 71.6 MB (71635317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9001eb8694075797a2cc406e1174b64701ccf7f9c01a8ebd52c43e3108cf9b2b`  
		Last Modified: Thu, 11 Jan 2024 08:19:13 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20074705c6c3399f6d059ea4033c3b4c509a462a323e1b81e94b72c7b241988d`  
		Last Modified: Thu, 11 Jan 2024 08:19:35 GMT  
		Size: 19.1 MB (19080566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:799aafb91517df33d3bd9f07c130983ba18da3c7fe16743aa414c6bc3548a8d7`  
		Last Modified: Thu, 11 Jan 2024 08:19:33 GMT  
		Size: 472.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619cbd41d6d814e4c7ec5edc8871e5e77fec52715281b3073d1a32ab1e4c649d`  
		Last Modified: Thu, 11 Jan 2024 08:19:33 GMT  
		Size: 514.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eb95e4d79c95498309b98c2b37a11c4f3b3aaa7feb8e4bd5df7944be5da2d18`  
		Last Modified: Thu, 11 Jan 2024 08:25:43 GMT  
		Size: 12.4 MB (12422034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0816144c4a6b13e234ed0e41d8623f8d29b1e67808f1ca7da745b32b44db8020`  
		Last Modified: Thu, 11 Jan 2024 08:25:41 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8deb68f29d6d22a03b32608871e875c9fdc9140b11359b77ce09e7c6e9e0596`  
		Last Modified: Thu, 11 Jan 2024 08:25:43 GMT  
		Size: 10.5 MB (10491200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:648d26bd337c95274dbd021049e7a5b872a7d35830a9659f1376c00272da16db`  
		Last Modified: Thu, 11 Jan 2024 08:25:41 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:128c7b4d9a61cc8fafe770aad7ac85f25454dd4106d7efa97ed4ed808a8efeb9`  
		Last Modified: Thu, 11 Jan 2024 08:25:41 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fc8fe933f0a431314a44f47a6d6394b67dd6b61ec07b5e695a5d899f485857e`  
		Last Modified: Thu, 11 Jan 2024 08:25:41 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:000ced42e80958a80d07851b933c40d024c869aa067019f5c9f713494b5a9b27`  
		Last Modified: Fri, 12 Jan 2024 00:37:37 GMT  
		Size: 1.5 MB (1522229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68f3b5d75eae708f2b2acbb9adfb1743fe906f218a2d9d5464b26ac48e13f1ed`  
		Last Modified: Fri, 12 Jan 2024 00:37:37 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:894a66192204d31aae53b03d7910c6e1c9936d5c2c5434959da52d919cd73099`  
		Last Modified: Fri, 12 Jan 2024 00:48:23 GMT  
		Size: 3.4 MB (3418877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.2-apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:536e5f46142ae670644a5e7ea357d671025db07700818fa4317552722a27ae85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5795352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7a5ba407738e30341672f2e0ce80ccb2f2a2238a573150d916a6b46ffd9adf8`

```dockerfile
```

-	Layers:
	-	`sha256:6ec6064e5d50b537f943fb973ae117faaceb8f356ca6db217f50ae0b075f29dd`  
		Last Modified: Fri, 12 Jan 2024 00:48:23 GMT  
		Size: 5.8 MB (5770660 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92051b29e53f62a7cf97550b432dc02253498fffde18258255b9d5a1b7f945de`  
		Last Modified: Fri, 12 Jan 2024 00:48:22 GMT  
		Size: 24.7 KB (24692 bytes)  
		MIME: application/vnd.in-toto+json
