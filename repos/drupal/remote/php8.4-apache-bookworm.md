## `drupal:php8.4-apache-bookworm`

```console
$ docker pull drupal@sha256:bed9cbe4793290ea766d37381c7002acdcdab277a1e749f24c0d97112cb3936f
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

### `drupal:php8.4-apache-bookworm` - linux; amd64

```console
$ docker pull drupal@sha256:e20fb13bdfd25eaec0c63659249e28a1ce7818f710b32da3b006211f3872e6ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.2 MB (212175206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:087e84fcccee6a98590e72f34d6c6635a2fa32796e106ff1ceabea920b7403ac`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 01:22:30 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 24 Jun 2026 01:22:45 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 24 Jun 2026 01:22:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:22:45 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 24 Jun 2026 01:22:46 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 24 Jun 2026 01:22:46 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 24 Jun 2026 01:22:46 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 24 Jun 2026 01:26:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 24 Jun 2026 01:26:16 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 24 Jun 2026 01:26:16 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 24 Jun 2026 01:26:16 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Jun 2026 01:26:16 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Jun 2026 01:26:16 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 24 Jun 2026 01:26:16 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 24 Jun 2026 01:26:16 GMT
ENV PHP_VERSION=8.4.22
# Wed, 24 Jun 2026 01:26:16 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.22.tar.xz.asc
# Wed, 24 Jun 2026 01:26:16 GMT
ENV PHP_SHA256=696c0f6ad92e94c59059c1eb6e300842b8d050934226efcdf00f2a413cb083cf
# Wed, 24 Jun 2026 01:26:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 24 Jun 2026 01:26:23 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:29:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 24 Jun 2026 01:29:02 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:29:02 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 24 Jun 2026 01:29:02 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 24 Jun 2026 01:29:02 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 24 Jun 2026 01:29:02 GMT
STOPSIGNAL SIGWINCH
# Wed, 24 Jun 2026 01:29:02 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:29:02 GMT
WORKDIR /var/www/html
# Wed, 24 Jun 2026 01:29:02 GMT
EXPOSE map[80/tcp:{}]
# Wed, 24 Jun 2026 01:29:02 GMT
CMD ["apache2-foreground"]
# Wed, 24 Jun 2026 02:30:32 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 02:30:33 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 24 Jun 2026 02:30:33 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Wed, 24 Jun 2026 02:30:33 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 02:30:33 GMT
ENV DRUPAL_VERSION=11.3.12
# Wed, 24 Jun 2026 02:30:33 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 24 Jun 2026 02:30:33 GMT
WORKDIR /opt/drupal
# Wed, 24 Jun 2026 02:30:39 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 24 Jun 2026 02:30:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:68629629b516c3cd6f5e71ffbe18e32afb1ae5b4926c92d058c0f11ef1fd58a3`  
		Last Modified: Wed, 24 Jun 2026 00:27:52 GMT  
		Size: 28.2 MB (28237639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e2426c0c3f033757713f62b25edf899b99d0b7935c4860bb2314fd9cb920884`  
		Last Modified: Wed, 24 Jun 2026 01:25:57 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f85c75bcc849f4189cd30b150a124164d045eb163124cbdd12a468c8ba7d2540`  
		Last Modified: Wed, 24 Jun 2026 01:26:02 GMT  
		Size: 104.3 MB (104344975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4706a37ce0736d1df3d410311def4fe803d7bab285e421639dccc735eea2d6f`  
		Last Modified: Wed, 24 Jun 2026 01:25:58 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3bc08da1c6fd9941f366f0bf9be53e7edc331e88fee95a0ecdcdb7d31cfc22c`  
		Last Modified: Wed, 24 Jun 2026 01:29:14 GMT  
		Size: 20.1 MB (20142277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4bcbb1bc2214284bd90632755aef0679451cf42d58c97ebfeb3f7f94be85132`  
		Last Modified: Wed, 24 Jun 2026 01:29:13 GMT  
		Size: 434.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90cbadecab3ed92e54461110759044830c248850ec8a00f44dafb74b6b285269`  
		Last Modified: Wed, 24 Jun 2026 01:29:13 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72e9b6d61def2e99ca62e0525a2a0b1c150809be7ba08909ccd3f2954a68470d`  
		Last Modified: Wed, 24 Jun 2026 01:29:13 GMT  
		Size: 13.9 MB (13860919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d49f3267733480f922ecefa9dbbd2d3f08afd23ad78a173be0b259738cf67481`  
		Last Modified: Wed, 24 Jun 2026 01:29:14 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56181c3774e5001e0c3dc7f60fabc3af8f998c1d8a3d239b1de560d1ba09974d`  
		Last Modified: Wed, 24 Jun 2026 01:29:14 GMT  
		Size: 13.7 MB (13660862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7428bcc7805d1bc55a6d4684ac8663ea3471b4decb3a88ae921565f444700c70`  
		Last Modified: Wed, 24 Jun 2026 01:29:15 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b4fce61eb3db78ec59a83562e4185e6359055a842f299ae79f4090061524b09`  
		Last Modified: Wed, 24 Jun 2026 01:29:15 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28c56fdc7f98a8ba36b15172bc6b181222326562c1c33c7025283373e27084c7`  
		Last Modified: Wed, 24 Jun 2026 01:29:16 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9c22b28f0406d27004aecaf602df25b757b1033ce927fb247f3c897efe4918c`  
		Last Modified: Wed, 24 Jun 2026 01:29:16 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a48e242a1dd56d86b0d718d85fbb8d35317713d7a7e966e77a021e96405110`  
		Last Modified: Wed, 24 Jun 2026 02:30:57 GMT  
		Size: 9.7 MB (9714568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dbcb39be51bbb7482a0b7ea08bc4d654499aded1b2826bffcb00c73117ffed7`  
		Last Modified: Wed, 24 Jun 2026 02:30:56 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f4590d28d439e1fd57780b1efd883d8600c822fbcb13945e15c603da4601625`  
		Last Modified: Wed, 24 Jun 2026 02:30:56 GMT  
		Size: 254.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f25b5326cfe10c532a6902ad19a958b381983b5f12b5eb32b9c2ece061dd3402`  
		Last Modified: Wed, 24 Jun 2026 02:30:56 GMT  
		Size: 823.3 KB (823340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:351ce745f8e5ac048fa5522f707285faef7cd70d690ef8cdc9ffdf97e9ab15b2`  
		Last Modified: Wed, 24 Jun 2026 02:30:58 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8927187b92df78fd69ea6308cf3a6c0b7d66d714dbcd92030c877b696d1a6531`  
		Last Modified: Wed, 24 Jun 2026 02:30:58 GMT  
		Size: 21.4 MB (21384212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.4-apache-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:f08439c2f762f6f9f539d99fb14984923766969fe9d3d7740e9c35218191612e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7196945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:450c473bd0a2411e15a93e44b4bc2d935279a74d48ad1c1600448395f5539e3e`

```dockerfile
```

-	Layers:
	-	`sha256:85fdc5f8c6783ef83c80e14d0575acac2bfcc3a98ef07ce3cf36899850893b99`  
		Last Modified: Wed, 24 Jun 2026 02:30:56 GMT  
		Size: 7.2 MB (7152850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad6ba2543ee0183de2e0f9ab0345aa8511703ce359e966096b02fc96424d6427`  
		Last Modified: Wed, 24 Jun 2026 02:30:56 GMT  
		Size: 44.1 KB (44095 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.4-apache-bookworm` - linux; arm variant v7

```console
$ docker pull drupal@sha256:2daf1292c4128d2fbc6e384a313aa2d85d4e7f5e038a0b0146cfcf81ccfce278
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.0 MB (173045847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:487542b072ba41d2630495ce7365cc7eef61864d469d6f832b697bce489149be`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:34:44 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 11 Jun 2026 00:34:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 11 Jun 2026 00:34:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:34:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 11 Jun 2026 00:34:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 11 Jun 2026 00:34:58 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 11 Jun 2026 00:34:58 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 11 Jun 2026 00:35:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 11 Jun 2026 00:35:05 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 11 Jun 2026 00:35:05 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 11 Jun 2026 00:35:05 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jun 2026 00:35:05 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jun 2026 00:35:05 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 11 Jun 2026 00:35:05 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 11 Jun 2026 00:35:05 GMT
ENV PHP_VERSION=8.4.22
# Thu, 11 Jun 2026 00:35:05 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.22.tar.xz.asc
# Thu, 11 Jun 2026 00:35:05 GMT
ENV PHP_SHA256=696c0f6ad92e94c59059c1eb6e300842b8d050934226efcdf00f2a413cb083cf
# Thu, 11 Jun 2026 00:35:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 11 Jun 2026 00:35:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:37:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 11 Jun 2026 00:37:51 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:37:51 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 11 Jun 2026 00:37:51 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 11 Jun 2026 00:37:51 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 11 Jun 2026 00:37:51 GMT
STOPSIGNAL SIGWINCH
# Thu, 11 Jun 2026 00:37:51 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:37:51 GMT
WORKDIR /var/www/html
# Thu, 11 Jun 2026 00:37:51 GMT
EXPOSE map[80/tcp:{}]
# Thu, 11 Jun 2026 00:37:51 GMT
CMD ["apache2-foreground"]
# Wed, 17 Jun 2026 22:25:48 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Jun 2026 22:25:48 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 17 Jun 2026 22:25:48 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Wed, 17 Jun 2026 22:25:48 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 17 Jun 2026 22:25:48 GMT
ENV DRUPAL_VERSION=11.3.12
# Wed, 17 Jun 2026 22:25:48 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 17 Jun 2026 22:25:48 GMT
WORKDIR /opt/drupal
# Wed, 17 Jun 2026 22:26:01 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 17 Jun 2026 22:26:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:8ae2378435d99f39097aa4fd0d6c58c08445becca3153d53205b2cc5054b09c2`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 23.9 MB (23944473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0de860c5eae593e1e109e061ccea43c5fe0205bf00f625636c8983e146703bf`  
		Last Modified: Thu, 11 Jun 2026 00:38:07 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c55da1ea0892f0639d299665ac9c49b2082ace4d26a2dac96c7066cf6f21c261`  
		Last Modified: Thu, 11 Jun 2026 00:38:10 GMT  
		Size: 76.2 MB (76154199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbb83940079fcffe001112422c13671fc7413caf2696ee603d30db9e03e8ee40`  
		Last Modified: Thu, 11 Jun 2026 00:38:07 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f7cc5cd9e9f6c08c180fcaf24329ab36645466df1114a78812d16d7b6520c6d`  
		Last Modified: Thu, 11 Jun 2026 00:38:08 GMT  
		Size: 18.9 MB (18850393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eda4e770a9d2ad1f0cc9b95dcb9e9926fa0a54307f1be9cc23c2e27c692e8f86`  
		Last Modified: Thu, 11 Jun 2026 00:38:09 GMT  
		Size: 425.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:718085c14e63f67d468ad7a2fe4f7e58065f9a981b831b09c4b59a62e90b404b`  
		Last Modified: Thu, 11 Jun 2026 00:38:09 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6af2f61dbec3189c8db97c3c2a94e3f1b43c933ed6460854d70f24d7b591126`  
		Last Modified: Thu, 11 Jun 2026 00:38:10 GMT  
		Size: 13.9 MB (13859046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6e160176b34b403efe75440ddadf258af5554f6685541dd44e66e8e8cbec1f2`  
		Last Modified: Thu, 11 Jun 2026 00:38:10 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47cab4d2c21b425c6cb556a31481e5e121b1eb73d231d926333a982b3209404d`  
		Last Modified: Thu, 11 Jun 2026 00:38:11 GMT  
		Size: 11.7 MB (11690713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c485a53d7157840f5a3b60391fc9f27ca62661a4e77df89ec6226126ea3320c5`  
		Last Modified: Thu, 11 Jun 2026 00:38:12 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b4096ff2a41f2c2aacdb8689f95156e05db03349931e83afdf98be83153358f`  
		Last Modified: Thu, 11 Jun 2026 00:38:12 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01f9808c6800cde98122c6153f5ac5d83e6c4b08ebd436a63710bcbefb344611`  
		Last Modified: Thu, 11 Jun 2026 00:38:12 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08901e1b882fe4b5258193373e826bc3610dda6404ecf5f6282d4edd5033d8fa`  
		Last Modified: Thu, 11 Jun 2026 00:38:12 GMT  
		Size: 888.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26f4d607b2a9f398b49b61548c9f7e482e22f04e4bfff516410196b83bd62842`  
		Last Modified: Wed, 17 Jun 2026 22:26:19 GMT  
		Size: 6.3 MB (6333090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c73c99c4bca38e54904f233eca0af540074e312f78f2cd6c3bbe8f795e223e8`  
		Last Modified: Wed, 17 Jun 2026 22:26:19 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bcb96408f7c83d138389f8c0df377bfbdf9562ce6951be17d60dc601240524f`  
		Last Modified: Wed, 17 Jun 2026 22:26:19 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b689f466ca927ec5cdee6e72978dddfb5bd0fef24a5f125b9dbe4266d62d0794`  
		Last Modified: Wed, 17 Jun 2026 22:26:19 GMT  
		Size: 823.3 KB (823342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f808b81b52aaf154d534c2736dc235cc5c6cdb64ebb0a53fbca79bd8d71e9bc`  
		Last Modified: Wed, 17 Jun 2026 22:26:20 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:007a37eeef99e63a7f0b6dffe55d9cb33f00ec5fa79ba1f6b80e1f4855eb5669`  
		Last Modified: Wed, 17 Jun 2026 22:26:21 GMT  
		Size: 21.4 MB (21384190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.4-apache-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:121233fd71b301cbb4d4fd73f454dbe7f39d86353e2b52583a092d004a10fc95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7010692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1acffbf4fa2da34dbc61d2f7303c7b51d47b79d1575adab4a168f550407c5a4d`

```dockerfile
```

-	Layers:
	-	`sha256:522647395e9e3b686c1a56219d1498cafa3b493551b6f23ffd9b6c79035c4edc`  
		Last Modified: Wed, 17 Jun 2026 22:26:19 GMT  
		Size: 7.0 MB (6966431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0d09c0e2e8d76b3c76fcc37055113a3afe531190b9043a9e7fafabfb2f4e1c8`  
		Last Modified: Wed, 17 Jun 2026 22:26:18 GMT  
		Size: 44.3 KB (44261 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.4-apache-bookworm` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:0f9674e1119e3c61368e02656074be51f4bfe26623cebbc2da1724a030d4d7ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.4 MB (203442152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cead7662cd6ca111e2aa1b9865b3af6f5abd9754241545fc40157423f9235238`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:24:29 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 11 Jun 2026 00:24:43 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 11 Jun 2026 00:24:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:24:43 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 11 Jun 2026 00:24:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 11 Jun 2026 00:24:43 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 11 Jun 2026 00:24:43 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 11 Jun 2026 00:28:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 11 Jun 2026 00:28:21 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 11 Jun 2026 00:28:21 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 11 Jun 2026 00:28:21 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jun 2026 00:28:21 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jun 2026 00:28:21 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 11 Jun 2026 00:28:21 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 11 Jun 2026 00:28:21 GMT
ENV PHP_VERSION=8.4.22
# Thu, 11 Jun 2026 00:28:21 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.22.tar.xz.asc
# Thu, 11 Jun 2026 00:28:21 GMT
ENV PHP_SHA256=696c0f6ad92e94c59059c1eb6e300842b8d050934226efcdf00f2a413cb083cf
# Thu, 11 Jun 2026 00:28:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 11 Jun 2026 00:28:29 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:31:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 11 Jun 2026 00:31:16 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:31:16 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 11 Jun 2026 00:31:16 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 11 Jun 2026 00:31:16 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 11 Jun 2026 00:31:16 GMT
STOPSIGNAL SIGWINCH
# Thu, 11 Jun 2026 00:31:16 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:31:16 GMT
WORKDIR /var/www/html
# Thu, 11 Jun 2026 00:31:16 GMT
EXPOSE map[80/tcp:{}]
# Thu, 11 Jun 2026 00:31:16 GMT
CMD ["apache2-foreground"]
# Wed, 17 Jun 2026 22:24:38 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Jun 2026 22:24:38 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 17 Jun 2026 22:24:39 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Wed, 17 Jun 2026 22:24:39 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 17 Jun 2026 22:24:39 GMT
ENV DRUPAL_VERSION=11.3.12
# Wed, 17 Jun 2026 22:24:39 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 17 Jun 2026 22:24:39 GMT
WORKDIR /opt/drupal
# Wed, 17 Jun 2026 22:27:04 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 17 Jun 2026 22:27:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:402614bd39aaec1e4bdcf25aa67f88588fc8d93997a2551c4e130e6ed2b06c7a`  
		Last Modified: Wed, 10 Jun 2026 23:39:57 GMT  
		Size: 28.1 MB (28122307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e88c4bbab64b5e5d8efa267def998ae7efbca8fb57a4cd1219340cc938b53ecb`  
		Last Modified: Thu, 11 Jun 2026 00:28:03 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c3a7763b623ef31669c8e57034f175fdb1ea69ff8e8f71bf9a32018054b7d8d`  
		Last Modified: Thu, 11 Jun 2026 00:28:06 GMT  
		Size: 98.2 MB (98177577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6afb996f24cc571886f56f72025ac14be52e63d04c3e2fc4bb5a40f1a688319e`  
		Last Modified: Thu, 11 Jun 2026 00:28:03 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba7871c41ce6f189f598e3f223efbc8ad7cd0e89aad68859ed39b44afd069204`  
		Last Modified: Thu, 11 Jun 2026 00:31:29 GMT  
		Size: 20.2 MB (20166628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6057f67e92a858b9c811fd56cc49077975e9057e55f9a12807c9ae7e270ed568`  
		Last Modified: Thu, 11 Jun 2026 00:31:27 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb174c5f5e545faf8c4c7c49a36c36c84981f6bcb4c3e0402b13254bf1097ea5`  
		Last Modified: Thu, 11 Jun 2026 00:31:27 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ee035f8a901d9176d2e2c7ec42bc4309e4a2661a1458880c76197a78a34dd37`  
		Last Modified: Thu, 11 Jun 2026 00:31:28 GMT  
		Size: 13.9 MB (13860679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da48ef992da59ca4b9f41f7c65f1514cb95260894f4df53f0e8b011bc96b9cb6`  
		Last Modified: Thu, 11 Jun 2026 00:31:29 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2bf176bf4c5c1f655ad8cd08ee83baefffcfc0f14de1d74a9e9ea7e2d2de03f`  
		Last Modified: Thu, 11 Jun 2026 00:31:29 GMT  
		Size: 13.3 MB (13292579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4d62ec9805ee899767d29ed1f93aa007b3d589930dc307bb2cbc215b331541`  
		Last Modified: Thu, 11 Jun 2026 00:31:30 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e98ae16a2d1d9db782b45e055d876468c6aebf534f29fdbaa7b709f937bf7e5`  
		Last Modified: Thu, 11 Jun 2026 00:31:30 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fb386d7a82c7988eedf896df241d5ae8442269847beefb171410ec0ba096b64`  
		Last Modified: Thu, 11 Jun 2026 00:31:31 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:596a8f7eb50bf73ba13eb3f43f1d12b7aa7776d8c3ceb5383ae13b3f3c74a07e`  
		Last Modified: Thu, 11 Jun 2026 00:31:31 GMT  
		Size: 888.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0d473d4ec0d4f348eeb4019d74c398b9f6e03b3a9bbbb6ac40161da07f5654f`  
		Last Modified: Wed, 17 Jun 2026 22:25:04 GMT  
		Size: 7.6 MB (7608522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:920f6507fe5d670a1629e13858e459792dd89405e7bc5bb0c985c824337ca15c`  
		Last Modified: Wed, 17 Jun 2026 22:25:04 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64a263f8dfed69f2aed679deeed3d376bfad706dbdfc4f93b80e3d2a5ccbf1d4`  
		Last Modified: Wed, 17 Jun 2026 22:25:04 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4ae45ecfb420d79d7257a91222ff0839c2b16d3b3c7646fc0dafbe8cc3a5b2a`  
		Last Modified: Wed, 17 Jun 2026 22:25:04 GMT  
		Size: 823.3 KB (823342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4eef01ff64f563f80de65992f3a1a22c3134de24e227f19ef4ca4265a9a0d25`  
		Last Modified: Wed, 17 Jun 2026 22:25:03 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54262d25667a15e0c4c97affa911077744e9c7724ef28211a3922b83cf4e0ab4`  
		Last Modified: Wed, 17 Jun 2026 22:27:21 GMT  
		Size: 21.4 MB (21384121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.4-apache-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:7dd14e9139434e5d0a71331cac3fbc26030ce8aea35d3459ab491857c6427f8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7225693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:781caf6ff3834abe476c6c132c5ec32ddb592e65aaf27f8ff636d4932f371d2a`

```dockerfile
```

-	Layers:
	-	`sha256:9d0d37951fbfc4379bc2e8afde8b5d9fcd8fb7a51895a438ae5fc2a54322bdc7`  
		Last Modified: Wed, 17 Jun 2026 22:27:20 GMT  
		Size: 7.2 MB (7181382 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43f372ffe59ceaa0200ba502f3b4f08b579be6e69ec9cf2a13f0cbd101875ff2`  
		Last Modified: Wed, 17 Jun 2026 22:27:19 GMT  
		Size: 44.3 KB (44311 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.4-apache-bookworm` - linux; 386

```console
$ docker pull drupal@sha256:e354c5e15885e7ced6c6aea99b636e9dce5b2a147683325968e92c12586892c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.0 MB (208018027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dc7d55fafce55ba5862b7e7bf69295677112f33761ebbd568bfc66490d3087d`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:19:39 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 11 Jun 2026 00:19:54 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 11 Jun 2026 00:19:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:19:54 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 11 Jun 2026 00:19:54 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 11 Jun 2026 00:19:54 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 11 Jun 2026 00:19:54 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 11 Jun 2026 00:19:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 11 Jun 2026 00:20:00 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 11 Jun 2026 00:20:00 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 11 Jun 2026 00:20:00 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jun 2026 00:20:00 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jun 2026 00:20:00 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 11 Jun 2026 00:20:00 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 11 Jun 2026 00:20:00 GMT
ENV PHP_VERSION=8.4.22
# Thu, 11 Jun 2026 00:20:00 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.22.tar.xz.asc
# Thu, 11 Jun 2026 00:20:00 GMT
ENV PHP_SHA256=696c0f6ad92e94c59059c1eb6e300842b8d050934226efcdf00f2a413cb083cf
# Thu, 11 Jun 2026 00:24:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 11 Jun 2026 00:24:08 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:26:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 11 Jun 2026 00:26:49 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:26:49 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 11 Jun 2026 00:26:49 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 11 Jun 2026 00:26:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 11 Jun 2026 00:26:49 GMT
STOPSIGNAL SIGWINCH
# Thu, 11 Jun 2026 00:26:49 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:26:49 GMT
WORKDIR /var/www/html
# Thu, 11 Jun 2026 00:26:49 GMT
EXPOSE map[80/tcp:{}]
# Thu, 11 Jun 2026 00:26:49 GMT
CMD ["apache2-foreground"]
# Wed, 17 Jun 2026 22:24:03 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Jun 2026 22:24:03 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 17 Jun 2026 22:24:03 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Wed, 17 Jun 2026 22:24:03 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 17 Jun 2026 22:24:03 GMT
ENV DRUPAL_VERSION=11.3.12
# Wed, 17 Jun 2026 22:24:03 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 17 Jun 2026 22:24:03 GMT
WORKDIR /opt/drupal
# Wed, 17 Jun 2026 22:24:09 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 17 Jun 2026 22:24:09 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:707460b758530d4476f3fefff30544db7cf8dbd98838ccc3533bc05e79016be4`  
		Last Modified: Wed, 10 Jun 2026 23:40:00 GMT  
		Size: 29.2 MB (29225762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebb0c8c72b4e1426304e46511f9acd004e3d19ac0f8e60c84d09d6c1f94be000`  
		Last Modified: Thu, 11 Jun 2026 00:23:47 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e446bb4f64170bbd544cd502a35060557e49defad8139c7fc19bde65b2ee58a`  
		Last Modified: Thu, 11 Jun 2026 00:23:51 GMT  
		Size: 101.5 MB (101536860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9616a92d330e2fddb2b865dedc8c51d0a0f82ab634cb3294622a41ac2f3361f7`  
		Last Modified: Thu, 11 Jun 2026 00:23:47 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6825dad5f4707b4da79a299fe5838aa2ea999847e70827c83b54f3ac2696b733`  
		Last Modified: Thu, 11 Jun 2026 00:23:48 GMT  
		Size: 20.7 MB (20665695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:651494a554c945d1bc8a9c38bbd9cd904cb5158003f63b212319a7a86c50fb16`  
		Last Modified: Thu, 11 Jun 2026 00:23:48 GMT  
		Size: 432.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67f8001f000d0760fa689362ecd249d1542f5332588d96c4dec49215eefaab05`  
		Last Modified: Thu, 11 Jun 2026 00:23:48 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7377fa6d7a3d4df810832df80450e3b99f9556308a8c69e8b7e0a3cf3cefbc7a`  
		Last Modified: Thu, 11 Jun 2026 00:27:00 GMT  
		Size: 13.9 MB (13860116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a8a6293d00837aecba008abdead0d574dae0b1ba3cc7ef933db81850dcc68c0`  
		Last Modified: Thu, 11 Jun 2026 00:26:59 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eded4ab4285e0825baed643713887a0d300317e91f8e23f92ead38714b8806c8`  
		Last Modified: Thu, 11 Jun 2026 00:27:00 GMT  
		Size: 14.0 MB (13956562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:209c456595c63d5e612106257dd4e4907ab0d6dd7d99f6af09b22014e1817b3f`  
		Last Modified: Thu, 11 Jun 2026 00:27:00 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5569566a50fc8607830709ad34acbbe941506357976c1229ac2de0594dac405e`  
		Last Modified: Thu, 11 Jun 2026 00:27:01 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24cadf561373a9d08ca9931b514fb6ce530ce61847971a4ef290b3ceb9d63c2c`  
		Last Modified: Thu, 11 Jun 2026 00:27:01 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c48a9082f0813c577c257e13c9dcb5552e182beaa5e0cbb06da0e210267e596e`  
		Last Modified: Thu, 11 Jun 2026 00:27:01 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea472757409371c214e227659023ec6255e50b14d7d8e62557dbe95158d9db05`  
		Last Modified: Wed, 17 Jun 2026 22:24:26 GMT  
		Size: 6.6 MB (6559110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab45330ceb5aeb105c13b0fe877c55b9361ccf85b903943432339a9f59e4c721`  
		Last Modified: Wed, 17 Jun 2026 22:24:26 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b3e063524251ff52aecfa5c9274c98289c04f2a34567a663d576e26f507c1c2`  
		Last Modified: Wed, 17 Jun 2026 22:24:26 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a241dedae3ba088ba42f182d04510b644ff43fef14711d2077820023e2557ab`  
		Last Modified: Wed, 17 Jun 2026 22:24:26 GMT  
		Size: 823.3 KB (823343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a984852fbe3c503e5c1930196c415faac5fa4ebc3572891a1ad8d29340196c1a`  
		Last Modified: Wed, 17 Jun 2026 22:24:27 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96354f8a6b148900d5bd2a2e2027d8c5c799441c960590fd15ccd82b8f7e02d9`  
		Last Modified: Wed, 17 Jun 2026 22:24:28 GMT  
		Size: 21.4 MB (21384165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.4-apache-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:87903d50f544116e0c25d3f680c2ce55113895318b501ebf5a9ee69e7c7d3af0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7169873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15db5a62b66e6065c9e12999df8e5f7b80ddf92c8241bd3f8e9562982d266d1f`

```dockerfile
```

-	Layers:
	-	`sha256:46e44d396acfb47038cbc5315a75dd26b09cbec6f43d2ff52f4a3eb50a482049`  
		Last Modified: Wed, 17 Jun 2026 22:24:26 GMT  
		Size: 7.1 MB (7125846 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:edc5227653960c7186e426cbcca37dc688e1face5deb6b79de48710b12413fc4`  
		Last Modified: Wed, 17 Jun 2026 22:24:25 GMT  
		Size: 44.0 KB (44027 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.4-apache-bookworm` - linux; ppc64le

```console
$ docker pull drupal@sha256:8704b7586ab285ab90ecfc0bbe228bdf805648d35e147b0078a34e0be39139d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.1 MB (215125256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51f0929892066f36e1a808589489091dd380f31de7b6cc9be9342d20e5f52235`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 03:11:32 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 11 Jun 2026 03:12:06 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 11 Jun 2026 03:12:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 03:12:06 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 11 Jun 2026 03:12:07 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 11 Jun 2026 03:12:07 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 11 Jun 2026 03:12:07 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 11 Jun 2026 03:14:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 11 Jun 2026 03:14:53 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 11 Jun 2026 03:14:53 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 11 Jun 2026 03:14:53 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jun 2026 03:14:53 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jun 2026 03:14:53 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 11 Jun 2026 03:14:53 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 11 Jun 2026 03:14:53 GMT
ENV PHP_VERSION=8.4.22
# Thu, 11 Jun 2026 03:14:53 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.22.tar.xz.asc
# Thu, 11 Jun 2026 03:14:53 GMT
ENV PHP_SHA256=696c0f6ad92e94c59059c1eb6e300842b8d050934226efcdf00f2a413cb083cf
# Thu, 11 Jun 2026 03:35:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 11 Jun 2026 03:35:37 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 03:40:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 11 Jun 2026 03:40:03 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 03:40:03 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 11 Jun 2026 03:40:04 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 11 Jun 2026 03:40:04 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 11 Jun 2026 03:40:04 GMT
STOPSIGNAL SIGWINCH
# Thu, 11 Jun 2026 03:40:04 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 03:40:04 GMT
WORKDIR /var/www/html
# Thu, 11 Jun 2026 03:40:04 GMT
EXPOSE map[80/tcp:{}]
# Thu, 11 Jun 2026 03:40:04 GMT
CMD ["apache2-foreground"]
# Wed, 17 Jun 2026 16:41:51 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Jun 2026 16:41:51 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 17 Jun 2026 16:41:52 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Wed, 17 Jun 2026 16:41:52 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 17 Jun 2026 16:41:52 GMT
ENV DRUPAL_VERSION=11.3.12
# Wed, 17 Jun 2026 16:41:52 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 17 Jun 2026 16:41:52 GMT
WORKDIR /opt/drupal
# Wed, 17 Jun 2026 22:32:27 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 17 Jun 2026 22:32:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:23f7cdee3ef2598b081c2b848fee95730a7ab2b1cc5b726c72dcb8c2fe3632f7`  
		Last Modified: Thu, 11 Jun 2026 00:21:33 GMT  
		Size: 32.1 MB (32081941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60f401effa3d6714ddb79ba94727795c8f0a3a88062ac122b5ee2b0e8569182b`  
		Last Modified: Thu, 11 Jun 2026 03:17:07 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:240f00b5b075e0ec40f2f3588739804d321a9e2a31a0cc00af6e3a278e020250`  
		Last Modified: Thu, 11 Jun 2026 03:17:11 GMT  
		Size: 103.3 MB (103334125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dff0f2e18a8eceb1609665b9d19e05533e28d58fec8497b4915edf3585bc68a5`  
		Last Modified: Thu, 11 Jun 2026 03:17:07 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5a05a0266369b3c5d29abc9937572a5304dba0263036108ba471fd1b198e131`  
		Last Modified: Thu, 11 Jun 2026 03:20:01 GMT  
		Size: 21.3 MB (21333938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e015947f7c149906d4247585ea0cf14955eecf5a551cbec15e0715f260ee7f0b`  
		Last Modified: Thu, 11 Jun 2026 03:20:00 GMT  
		Size: 443.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:253f39cd570c2a553c8d84e262880bf813fa0dc7c859fe1abf85b47bfbfefaa0`  
		Last Modified: Thu, 11 Jun 2026 03:20:00 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e7425de0eebecdb3adf2bf47013b18a45449ec508f4516d9b67997dbc2cd9a1`  
		Last Modified: Thu, 11 Jun 2026 03:40:28 GMT  
		Size: 13.9 MB (13860492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eb735b8e4d1d6d2c3287b74edf414d6c47bc3114c21d4dc0445c65e3b47cb29`  
		Last Modified: Thu, 11 Jun 2026 03:40:27 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66cca4f2546bd6dc2c5e212213dddaff151723d3cb3f01b0535ef43ce5e7a5af`  
		Last Modified: Thu, 11 Jun 2026 03:40:28 GMT  
		Size: 14.1 MB (14072232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:142cddde2cd3ebc74e86786d97afb6cb44a4c12e01916943134185a124d98960`  
		Last Modified: Thu, 11 Jun 2026 03:40:27 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59b86697200d8a3209042f3705e9578f9bc54fc4eccbe82d03be659426a948c1`  
		Last Modified: Thu, 11 Jun 2026 03:40:28 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15df49c7963db1267f5d3fce276124d57fefb20b1e553c027eae2a9eb1d7ac9c`  
		Last Modified: Thu, 11 Jun 2026 03:40:28 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be246b3957f84d692ad3ced117c15475122d393cd66de4f4db56dece5b1b4fa3`  
		Last Modified: Thu, 11 Jun 2026 03:40:30 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61bac881fd154074cd349806f0930d51606ae9240b42fc1d3a85ecf98923f0ff`  
		Last Modified: Wed, 17 Jun 2026 16:42:46 GMT  
		Size: 8.2 MB (8229037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b541e88838c752c460864867c5c652b6bc4e55e18c266afe433180842debc40`  
		Last Modified: Wed, 17 Jun 2026 16:42:46 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:195ed36c5e5f48175222ba88c5c11c93338559814b5fceb26859266396e926fe`  
		Last Modified: Wed, 17 Jun 2026 16:42:46 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47fca81d0235a7e080d7f133cab2eda0467eda021b8775f64ce85014094d27f4`  
		Last Modified: Wed, 17 Jun 2026 16:42:46 GMT  
		Size: 823.3 KB (823345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c2c94eb03d31db6100903bbc1afeca1f0205b85ace8346d62262275c3f3698e`  
		Last Modified: Wed, 17 Jun 2026 16:42:47 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6654d7f2170255171a34948b66f0b3b5e0bb33b2d77c6b8a9a800263b6556e1a`  
		Last Modified: Wed, 17 Jun 2026 22:33:09 GMT  
		Size: 21.4 MB (21383706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.4-apache-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:bb88efdbbf8c19497caf296644e309b13ddd500613c689110999c015d05ae34b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7174276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83b90de82cb5114db1b1b015b116c76ce1e3ff65d8bd1e477cf7df9e11ebef0a`

```dockerfile
```

-	Layers:
	-	`sha256:9ef1c66247bec54002d1b02161cd35b6fc3b2fbc20c5ff760095ed0dda34e918`  
		Last Modified: Wed, 17 Jun 2026 22:33:08 GMT  
		Size: 7.1 MB (7130097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b97bde7b3dc860be21eaed6dc2849ebbc47eddfeab9f02438b1ed262fc8b0917`  
		Last Modified: Wed, 17 Jun 2026 22:33:08 GMT  
		Size: 44.2 KB (44179 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.4-apache-bookworm` - linux; s390x

```console
$ docker pull drupal@sha256:54fef45922beb6c0bad8575626a207f0d0ad24d9003a3be8de22f4dbf90207c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.8 MB (183764739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b70877566a584207bd066b7e8a64f330c49235c39eee0bf0abff74ae9566933f`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:29:53 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 11 Jun 2026 00:30:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 11 Jun 2026 00:30:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:30:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 11 Jun 2026 00:30:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 11 Jun 2026 00:30:14 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 11 Jun 2026 00:30:14 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 11 Jun 2026 00:30:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 11 Jun 2026 00:30:49 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 11 Jun 2026 00:30:49 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 11 Jun 2026 00:30:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jun 2026 00:30:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jun 2026 00:30:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 11 Jun 2026 00:30:49 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 11 Jun 2026 00:30:49 GMT
ENV PHP_VERSION=8.4.22
# Thu, 11 Jun 2026 00:30:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.22.tar.xz.asc
# Thu, 11 Jun 2026 00:30:49 GMT
ENV PHP_SHA256=696c0f6ad92e94c59059c1eb6e300842b8d050934226efcdf00f2a413cb083cf
# Thu, 11 Jun 2026 00:40:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 11 Jun 2026 00:40:42 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:44:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 11 Jun 2026 00:44:37 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:44:38 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 11 Jun 2026 00:44:38 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 11 Jun 2026 00:44:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 11 Jun 2026 00:44:38 GMT
STOPSIGNAL SIGWINCH
# Thu, 11 Jun 2026 00:44:38 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:44:38 GMT
WORKDIR /var/www/html
# Thu, 11 Jun 2026 00:44:38 GMT
EXPOSE map[80/tcp:{}]
# Thu, 11 Jun 2026 00:44:38 GMT
CMD ["apache2-foreground"]
# Wed, 17 Jun 2026 16:55:12 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Jun 2026 16:55:18 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 17 Jun 2026 16:55:23 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Wed, 17 Jun 2026 16:55:32 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 17 Jun 2026 16:55:42 GMT
ENV DRUPAL_VERSION=11.3.12
# Wed, 17 Jun 2026 16:55:42 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 17 Jun 2026 16:55:42 GMT
WORKDIR /opt/drupal
# Wed, 17 Jun 2026 22:24:48 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 17 Jun 2026 22:24:48 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:6483bebe0f30256cfdd9c6f96373508f6b33d18b4bc61668ee641c700aa3108a`  
		Last Modified: Wed, 10 Jun 2026 23:41:10 GMT  
		Size: 26.9 MB (26893508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:760bd98ba6f0dd242612b772363db9255777926da7a6de678aecf2f09b8d5732`  
		Last Modified: Thu, 11 Jun 2026 00:35:15 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f67c915a547eb9b0822aa7ee67c5e7ecc13a91135df9ea75a1bc931a92c4d2fa`  
		Last Modified: Thu, 11 Jun 2026 00:35:17 GMT  
		Size: 80.8 MB (80829344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:624ec25b7891427e77853374900796edc8ff332bc21cb7b919324f378695e981`  
		Last Modified: Thu, 11 Jun 2026 00:35:15 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff87533fc6ce2cc27ea6fc98a8ad365f202059a976a90eb88a9e5ada587c869`  
		Last Modified: Thu, 11 Jun 2026 00:35:51 GMT  
		Size: 19.9 MB (19919167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:899d853badeade8087e2e91365ab8a8094c92ed367d01c47a0c04a34e847be56`  
		Last Modified: Thu, 11 Jun 2026 00:35:50 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:594731f96f9f714220f03b14ca6aea7d1f24f21d6d2f25ce308d3271d7852dc8`  
		Last Modified: Thu, 11 Jun 2026 00:35:50 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c36cf18c390e345d3e2594992a2460092e0ee763b91e8dc2d30b173e3c49116`  
		Last Modified: Thu, 11 Jun 2026 00:44:56 GMT  
		Size: 13.9 MB (13859503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a0e9b2c608b05059a48097ccc0e02933ede987794c392dffefd804ab54a3426`  
		Last Modified: Thu, 11 Jun 2026 00:44:56 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a99c2686ca771e9b88da3d1a9da8a9ad98ee4e535895deb06d6cec9a643c0f5`  
		Last Modified: Thu, 11 Jun 2026 00:44:57 GMT  
		Size: 12.7 MB (12710859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e38a2e70c703ebbaf79b24c886d0646b8e60b6595041e3294d669a189033448`  
		Last Modified: Thu, 11 Jun 2026 00:44:56 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85bd1b4fac25a4fa6fb48958dad1dc28bbcbb000349246dec685ec01b972bf34`  
		Last Modified: Thu, 11 Jun 2026 00:44:58 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8770b04bbe54a2cebec843d8738148455d0c0db28b568f6c1b1b86394f03472f`  
		Last Modified: Thu, 11 Jun 2026 00:44:57 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15d0e28dbb972fb22317807712a2d6dc73945746f844f009767841653b611420`  
		Last Modified: Thu, 11 Jun 2026 00:44:58 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33544fc7a3109a2f3399ddb06d792b53ecb1870be1ad6e46e9bfc004e0b1ee8d`  
		Last Modified: Wed, 17 Jun 2026 17:00:58 GMT  
		Size: 7.3 MB (7340349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a90df3078aa8cffc63ba8e0f1890efca1326aa6ccac614d18fd43d3f443c5568`  
		Last Modified: Wed, 17 Jun 2026 17:00:52 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aeedfd54ad6ffc93146dc29f27ff2a51c1d4550703788a9b906f1afa65d5bc2`  
		Last Modified: Wed, 17 Jun 2026 17:00:47 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddb935e66658d5f6157ac2075d430d54e74cb9b60b6192456af37ae3d46ec71e`  
		Last Modified: Wed, 17 Jun 2026 17:00:46 GMT  
		Size: 823.3 KB (823341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bce41e4ab482bc8548cf1fe0e685b251e2dba3318200b8a755784e744a084d9`  
		Last Modified: Wed, 17 Jun 2026 17:00:48 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72ae66219bee43387c7d90faf823bb5f6e9e27fea8b03e53e17511716e372750`  
		Last Modified: Wed, 17 Jun 2026 22:25:12 GMT  
		Size: 21.4 MB (21382260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.4-apache-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:3b925dcd7ed1ba1a161c948359b7721dca53aa393568a74a95b5015fbfed5bf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7031870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d421258b0bb224b58dffd6e39c79223ab8d95bcd312480e53f9cc56418934f88`

```dockerfile
```

-	Layers:
	-	`sha256:434e4803ecc2bde8321efe60c3a6b538ff318a2cdaa693a7eea578c634e2c3c6`  
		Last Modified: Wed, 17 Jun 2026 22:25:12 GMT  
		Size: 7.0 MB (6989981 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16ba3c4117a86b3e3d7befd8827bcd5afd55c2473533db1b4d40f22a00d6a98f`  
		Last Modified: Wed, 17 Jun 2026 22:25:11 GMT  
		Size: 41.9 KB (41889 bytes)  
		MIME: application/vnd.in-toto+json
