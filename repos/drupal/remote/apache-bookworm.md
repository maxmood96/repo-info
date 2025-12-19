## `drupal:apache-bookworm`

```console
$ docker pull drupal@sha256:0344f2c7de62c850d0c304152b6a558a9a6797e3a3a2b755a1e4be5b80db289c
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

### `drupal:apache-bookworm` - linux; amd64

```console
$ docker pull drupal@sha256:918d621e173de5d09f000042a339bc1f5b1e9aba138e7efde40fa0df2cca0c73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.6 MB (203648526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c73376e7f04c4946fd78bcfe1edfe3111ce839c719f33972108c9b07a01dfd8`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Fri, 19 Dec 2025 01:26:46 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 19 Dec 2025 01:27:00 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 19 Dec 2025 01:27:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Dec 2025 01:27:00 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 19 Dec 2025 01:27:00 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 19 Dec 2025 01:27:00 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 19 Dec 2025 01:27:00 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 19 Dec 2025 01:27:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 19 Dec 2025 01:27:06 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 19 Dec 2025 01:27:06 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 19 Dec 2025 01:27:06 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Dec 2025 01:27:06 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Dec 2025 01:27:06 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 19 Dec 2025 01:27:06 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 19 Dec 2025 01:27:06 GMT
ENV PHP_VERSION=8.4.16
# Fri, 19 Dec 2025 01:27:06 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.16.tar.xz.asc
# Fri, 19 Dec 2025 01:27:06 GMT
ENV PHP_SHA256=f66f8f48db34e9e29f7bfd6901178e9cf4a1b163e6e497716dfcb8f88bcfae30
# Fri, 19 Dec 2025 01:27:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 19 Dec 2025 01:27:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 01:29:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 19 Dec 2025 01:29:45 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 01:29:45 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 19 Dec 2025 01:29:45 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 19 Dec 2025 01:29:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 19 Dec 2025 01:29:45 GMT
STOPSIGNAL SIGWINCH
# Fri, 19 Dec 2025 01:29:45 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 01:29:45 GMT
WORKDIR /var/www/html
# Fri, 19 Dec 2025 01:29:45 GMT
EXPOSE map[80/tcp:{}]
# Fri, 19 Dec 2025 01:29:45 GMT
CMD ["apache2-foreground"]
# Fri, 19 Dec 2025 02:12:08 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Dec 2025 02:12:08 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 19 Dec 2025 02:12:08 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Fri, 19 Dec 2025 02:12:08 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 02:12:08 GMT
ENV DRUPAL_VERSION=11.3.1
# Fri, 19 Dec 2025 02:12:08 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 19 Dec 2025 02:12:08 GMT
WORKDIR /opt/drupal
# Fri, 19 Dec 2025 02:12:20 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 19 Dec 2025 02:12:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:ae4ce04d0e1ccb5db08fa441b79635de5590399fae652d10bd3379b231be0ead`  
		Last Modified: Mon, 08 Dec 2025 22:17:22 GMT  
		Size: 28.2 MB (28228418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd70d728d494fc9b2f967806cc45ca01bbc525af8d4f04980bf260eedd0d51a0`  
		Last Modified: Fri, 19 Dec 2025 01:30:16 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec53cfae976038905038a3f036a1cf3359aaacd4bf9ab15263c7242322e5ed8`  
		Last Modified: Fri, 19 Dec 2025 01:30:23 GMT  
		Size: 104.3 MB (104330542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:265ae04266e25774287cec56645f845a960f671977f6af1175dcf55fba7a134a`  
		Last Modified: Fri, 19 Dec 2025 01:30:17 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5468d936ef707055197f12fa44bd106e887151f17681f0cb86674a8064f496e7`  
		Last Modified: Fri, 19 Dec 2025 01:30:18 GMT  
		Size: 20.1 MB (20131821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e959b0398bce483417ee13cdee6ae6fb1d5a4c93310881dc3fdf8fc5d51efe`  
		Last Modified: Fri, 19 Dec 2025 01:30:16 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc1a95757f9aea3828cf4cf26c69bd66b9ba861444904243f33e36349f337143`  
		Last Modified: Fri, 19 Dec 2025 01:30:21 GMT  
		Size: 481.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15251c2b0702233f193689d1eb90cad305f74fcc8b551ae3d848c45ae69bbdd3`  
		Last Modified: Fri, 19 Dec 2025 01:30:17 GMT  
		Size: 13.8 MB (13790236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ed4a2d7a8896a033207e5bb3c8d3861cbe6d9969e78639c820ce6f271f5a7cc`  
		Last Modified: Fri, 19 Dec 2025 01:30:17 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64da8d08dcdf2327f3d9b08bdbd891915cae74be9f313e9bada92ecd0589655b`  
		Last Modified: Fri, 19 Dec 2025 01:30:20 GMT  
		Size: 13.5 MB (13506543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45f3c68ea55aeab4027ef8bd3e7a8e35ba0b6cbd13737d0624ee29bb179870f3`  
		Last Modified: Fri, 19 Dec 2025 01:30:17 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f50e32688c548775e13f0ad6279c847f8afe070965e21d4b708109328eb53fd8`  
		Last Modified: Fri, 19 Dec 2025 01:30:17 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5845f25a0473972f838ad50243ef1bf4a3c3f3685072a270180eac9396fe5ed`  
		Last Modified: Fri, 19 Dec 2025 01:30:17 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:517ade244d921ff9ecebb0dba785fc2e228b10ffb80befc73ee4ade6d7063aab`  
		Last Modified: Fri, 19 Dec 2025 01:30:17 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:464484387391d2401563aa427e993433920e8d64bc3536340f8cdfaa4badb0a6`  
		Last Modified: Fri, 19 Dec 2025 02:12:45 GMT  
		Size: 1.6 MB (1574858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3698e2373f805a682ebbf99ea1ce93d7225e213f2c386af07de471d81344c40d`  
		Last Modified: Fri, 19 Dec 2025 02:12:45 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0eb1710c3f277f4bcc8d533e22b7069a0c28c5bb3f089b31386b89872e3b6e0`  
		Last Modified: Fri, 19 Dec 2025 02:12:45 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47572d3954def39ee9f19d3a25273e2cc7c892b9f5a8e1c8cfa47a27efb09e4a`  
		Last Modified: Fri, 19 Dec 2025 02:12:45 GMT  
		Size: 778.0 KB (777990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62a2a02ba3278dee6e01bb1827248ea0a99aad936b638b5f3fcc971a375ab31c`  
		Last Modified: Fri, 19 Dec 2025 02:12:45 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b2ad0a10287b16455eed23e426732df467f57d6758232a6c0fc7f5d94116eac`  
		Last Modified: Fri, 19 Dec 2025 02:12:46 GMT  
		Size: 21.3 MB (21301713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:apache-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:2ad6981429655dfa2f2fe5715da9d36f6c9f03cd2ebeaea139762d646fd616b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7096086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7ecc44bb797b94cef89cf5084609bde0129b4385a0ad6ab83e148bdea2d4dab`

```dockerfile
```

-	Layers:
	-	`sha256:1c2b6ba256c65ae5e3b2b8abf9937a3cfb03bdf40d9e1a3defbc8aae56ea9b8a`  
		Last Modified: Fri, 19 Dec 2025 06:06:16 GMT  
		Size: 7.1 MB (7052156 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77c52c1ba967ca2b25e5c9f8dd2125b686d60697c06397120f9f921e053a09f0`  
		Last Modified: Fri, 19 Dec 2025 06:06:17 GMT  
		Size: 43.9 KB (43930 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:apache-bookworm` - linux; arm variant v7

```console
$ docker pull drupal@sha256:b5a99e6105f05f2e197d4b4ea711da061ec434f92dde703e0a9246524e94b076
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.7 MB (167716212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:632bb68bbce2e86084226992ae67267fc1b6a234b47000a4b6c0f2824b57a54e`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1765152000'
# Fri, 19 Dec 2025 01:29:41 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 19 Dec 2025 01:29:56 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 19 Dec 2025 01:29:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Dec 2025 01:29:56 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 19 Dec 2025 01:29:56 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 19 Dec 2025 01:29:56 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 19 Dec 2025 01:29:56 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 19 Dec 2025 01:30:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 19 Dec 2025 01:30:03 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 19 Dec 2025 01:30:04 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 19 Dec 2025 01:30:04 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Dec 2025 01:30:04 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Dec 2025 01:30:04 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 19 Dec 2025 01:30:04 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 19 Dec 2025 01:30:04 GMT
ENV PHP_VERSION=8.4.16
# Fri, 19 Dec 2025 01:30:04 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.16.tar.xz.asc
# Fri, 19 Dec 2025 01:30:04 GMT
ENV PHP_SHA256=f66f8f48db34e9e29f7bfd6901178e9cf4a1b163e6e497716dfcb8f88bcfae30
# Fri, 19 Dec 2025 01:30:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 19 Dec 2025 01:30:12 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 01:32:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 19 Dec 2025 01:32:52 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 01:32:53 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 19 Dec 2025 01:32:53 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 19 Dec 2025 01:32:53 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 19 Dec 2025 01:32:53 GMT
STOPSIGNAL SIGWINCH
# Fri, 19 Dec 2025 01:32:53 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 01:32:53 GMT
WORKDIR /var/www/html
# Fri, 19 Dec 2025 01:32:53 GMT
EXPOSE map[80/tcp:{}]
# Fri, 19 Dec 2025 01:32:53 GMT
CMD ["apache2-foreground"]
# Fri, 19 Dec 2025 02:19:09 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Dec 2025 02:19:09 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 19 Dec 2025 02:19:09 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Fri, 19 Dec 2025 02:19:09 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 02:19:09 GMT
ENV DRUPAL_VERSION=11.3.1
# Fri, 19 Dec 2025 02:19:09 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 19 Dec 2025 02:19:09 GMT
WORKDIR /opt/drupal
# Fri, 19 Dec 2025 02:19:18 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 19 Dec 2025 02:19:18 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:e12d446114182318769a6ca4adfc14d21fbb73f898de1d765662812d9f21c3a6`  
		Last Modified: Mon, 08 Dec 2025 22:16:03 GMT  
		Size: 23.9 MB (23934020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a05a50db64ecd34dce11bdece4252d1e0c8103e7b2155217e824d6feec4cf23`  
		Last Modified: Fri, 19 Dec 2025 01:33:20 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f154192c1cc942e0803855d275b531f8b34c3574daae2238184414e0bd7757`  
		Last Modified: Fri, 19 Dec 2025 01:33:28 GMT  
		Size: 76.1 MB (76148739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3590080795b33381dd511e952c053ad4cb489e7824a64eb711ab7e138596b9e1`  
		Last Modified: Fri, 19 Dec 2025 01:33:20 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dec96f9f55b5a3143125ea1d7a361cb5b38f8a8c7da0e3996dea340b75977a8f`  
		Last Modified: Fri, 19 Dec 2025 01:33:22 GMT  
		Size: 18.9 MB (18859996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:474421206440f57c61fe210d69ab171928cadb3e159d6b898813b657ff55dfe3`  
		Last Modified: Fri, 19 Dec 2025 01:33:20 GMT  
		Size: 426.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c846fa8f99ce7d97c9136286619e2a7d8551c69d7369217f64fd6eeb3752b54c`  
		Last Modified: Fri, 19 Dec 2025 01:33:20 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:791c69de73bd40ceaa47f2fac7e1623440ea602f07633dd21240d4e64b11697b`  
		Last Modified: Fri, 19 Dec 2025 01:33:23 GMT  
		Size: 13.8 MB (13788033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2749c14cee443011a3a8747aa032a6192c6986fa95a309ec80463a6992899f90`  
		Last Modified: Fri, 19 Dec 2025 01:33:21 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b59cfd43f1fddcb24503af0a9a9942b72855c443d3703d4eb96b687b389399e`  
		Last Modified: Fri, 19 Dec 2025 01:33:22 GMT  
		Size: 11.6 MB (11605068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07f495b92b59faf5f33b71b0952bd6a656d1136249865aac5669d7c2bf29e647`  
		Last Modified: Fri, 19 Dec 2025 01:33:21 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e97edefe64351bf6157c5f3df0846ee9980e8be6d56f1857d1b63803680494b3`  
		Last Modified: Fri, 19 Dec 2025 01:33:19 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cad63433841184fbce8e19a8d833317c1642e764f234a29d41807adb41c8a088`  
		Last Modified: Fri, 19 Dec 2025 01:33:19 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ac204f3a18bcda1812c049230053f1569b3c97f4e07287ad857296753a55f00`  
		Last Modified: Fri, 19 Dec 2025 01:33:19 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8bce46d13e4fef5ab4ec73fcae4a36aad354aa2958342033f331a7d777e277e`  
		Last Modified: Fri, 19 Dec 2025 02:19:43 GMT  
		Size: 1.3 MB (1294965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04917e45e2f6c5d82985c2ef0f8e4f4740408967031239957ba07d3af47624e8`  
		Last Modified: Fri, 19 Dec 2025 02:19:43 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b25aed28fad336f9e245e9dcca321733c2846a7ef4d3e488b1db0508eed10648`  
		Last Modified: Fri, 19 Dec 2025 02:19:43 GMT  
		Size: 254.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:643a70a0dd2aef5fbd1d1aee61e4d5af91e79ed4b80234a9a9a8ff109a106319`  
		Last Modified: Fri, 19 Dec 2025 02:19:43 GMT  
		Size: 778.0 KB (778000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2646e735e4fd7fb73a88f4818a7cc43724531cf83626910009923c2d6776dcfc`  
		Last Modified: Fri, 19 Dec 2025 02:19:43 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f38cab99eb2cee9144e9bc0d0cbb531a2cda15c021b1c660f7e9bf98b4072bb`  
		Last Modified: Fri, 19 Dec 2025 02:19:46 GMT  
		Size: 21.3 MB (21300988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:apache-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:78ff0417494b829e9264e7a381fa4d758b0b7a3cb091aab8372c0da59492de81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6909619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a259ac6e0f3007dfc7bc30db8bba79eec97169fe3bbd75864fdf76311d53923`

```dockerfile
```

-	Layers:
	-	`sha256:a81055aee720ccb25936e43b7ff652b0efa8c4fb22633b90d898c2aa450e03de`  
		Last Modified: Fri, 19 Dec 2025 06:06:23 GMT  
		Size: 6.9 MB (6865524 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:512544a55b067ead16c0d22473d9568ec5a5786f977ca7a5e1f6a200d306f0bc`  
		Last Modified: Fri, 19 Dec 2025 06:06:24 GMT  
		Size: 44.1 KB (44095 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:apache-bookworm` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:84633bd32f98b32fd36acda3c939895d7418b52881235adea53ff5d090c86897
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.0 MB (197017124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63478510795f0e4a9fec820bfebca1a50f59003906ac6ca2c1b7861c1f39d10b`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1765152000'
# Fri, 19 Dec 2025 01:26:27 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 19 Dec 2025 01:26:42 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 19 Dec 2025 01:26:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Dec 2025 01:26:42 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 19 Dec 2025 01:26:42 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 19 Dec 2025 01:26:42 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 19 Dec 2025 01:26:42 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 19 Dec 2025 01:26:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 19 Dec 2025 01:26:48 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 19 Dec 2025 01:26:48 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 19 Dec 2025 01:26:48 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Dec 2025 01:26:48 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Dec 2025 01:26:48 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 19 Dec 2025 01:26:48 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 19 Dec 2025 01:26:48 GMT
ENV PHP_VERSION=8.4.16
# Fri, 19 Dec 2025 01:26:48 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.16.tar.xz.asc
# Fri, 19 Dec 2025 01:26:48 GMT
ENV PHP_SHA256=f66f8f48db34e9e29f7bfd6901178e9cf4a1b163e6e497716dfcb8f88bcfae30
# Fri, 19 Dec 2025 01:26:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 19 Dec 2025 01:26:57 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 01:29:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 19 Dec 2025 01:29:51 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 01:29:51 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 19 Dec 2025 01:29:51 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 19 Dec 2025 01:29:51 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 19 Dec 2025 01:29:51 GMT
STOPSIGNAL SIGWINCH
# Fri, 19 Dec 2025 01:29:51 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 01:29:51 GMT
WORKDIR /var/www/html
# Fri, 19 Dec 2025 01:29:51 GMT
EXPOSE map[80/tcp:{}]
# Fri, 19 Dec 2025 01:29:51 GMT
CMD ["apache2-foreground"]
# Fri, 19 Dec 2025 02:14:01 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Dec 2025 02:14:01 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 19 Dec 2025 02:14:01 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Fri, 19 Dec 2025 02:14:01 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 02:14:01 GMT
ENV DRUPAL_VERSION=11.3.1
# Fri, 19 Dec 2025 02:14:01 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 19 Dec 2025 02:14:01 GMT
WORKDIR /opt/drupal
# Fri, 19 Dec 2025 02:14:11 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 19 Dec 2025 02:14:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:8a4a7306158c2bef7a131de3110e384f4822829cbcce20bc6b4ba32dd82a1d87`  
		Last Modified: Mon, 08 Dec 2025 22:16:51 GMT  
		Size: 28.1 MB (28102229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b8e2ee7061f141b60493bf31e1ab043580119b2d0adab8eb6d903c5f7e95f3`  
		Last Modified: Fri, 19 Dec 2025 01:30:20 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:364ed7025d4c12ab897e3ca30171c9bff5db99dc8ba39104832d2fff59d603eb`  
		Last Modified: Fri, 19 Dec 2025 01:30:32 GMT  
		Size: 98.2 MB (98165984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:819df2327876f1a378faa15cc07365501af270764aba170706bd752aa6d3841f`  
		Last Modified: Fri, 19 Dec 2025 01:30:20 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d3026504eefe6b2088c148233f73867b5ef5dec59a04c7fa64cf8053dfba807`  
		Last Modified: Fri, 19 Dec 2025 01:30:25 GMT  
		Size: 20.2 MB (20158999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b5d855b1b21003d3df972ad589586a1d1e7009492fcae4f225aebf44ee2022f`  
		Last Modified: Fri, 19 Dec 2025 01:30:20 GMT  
		Size: 433.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9250f1c664215e51939cc13303d68839a196051921e8acd58c7f299413a1d6e`  
		Last Modified: Fri, 19 Dec 2025 01:30:20 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d57333f776aae21a57c252a29983d56087786337985489735cbdb0bb93bcb81c`  
		Last Modified: Fri, 19 Dec 2025 01:30:22 GMT  
		Size: 13.8 MB (13789882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ec7854bd156fd14f266d4cf4cd2992aa5a55da9f3a741069a65964ec090011a`  
		Last Modified: Fri, 19 Dec 2025 01:30:20 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec430ed45f758c00aa8f4d03a3d99f1a6851078480f7643a87a75cdf83831311`  
		Last Modified: Fri, 19 Dec 2025 01:30:23 GMT  
		Size: 13.2 MB (13151852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb0a3c01d1d6e0924fb53476f725b1951f9306376cbe7fa16ccac82ea052f52b`  
		Last Modified: Fri, 19 Dec 2025 01:30:20 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5437aff76e897f94456b30187bdbade91a42fc70825d71e99aa3e3f5ade5b901`  
		Last Modified: Fri, 19 Dec 2025 01:30:21 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e934d4bc50133356334d57d3527f158a87777e0060990492549d8579f88321b7`  
		Last Modified: Fri, 19 Dec 2025 01:30:21 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4b9e38723bfe532c7877a142786626d78bf582d8a754ea4235edaa7ea718f26`  
		Last Modified: Fri, 19 Dec 2025 01:30:21 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64a8bf96b565150e6ba4925f86416f2e224bacc621b8cbd023ecffcd57ddc82a`  
		Last Modified: Fri, 19 Dec 2025 02:14:38 GMT  
		Size: 1.6 MB (1562905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:893fb6a9b0f709697dff0100a4c00c7a7590da5851678ec1dc00c5a9ce8a56ef`  
		Last Modified: Fri, 19 Dec 2025 02:14:38 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04b62f2b25044b7228e91eae1fb09b1c543bc7a500bfc05f940cd5f851e88f9c`  
		Last Modified: Fri, 19 Dec 2025 02:14:38 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aacd92913235d36a8e4b22ca24e3311680e77caae9797c8295ed8b763a33ad38`  
		Last Modified: Fri, 19 Dec 2025 02:14:38 GMT  
		Size: 778.0 KB (778004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bea7918db91b597421b9d1696097b6931bfa22c544ff8b2d66ded4962461024`  
		Last Modified: Fri, 19 Dec 2025 02:14:38 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd179d42273551b36cf9378b1fff49ddebfb7819510d122b6383cd2a7b78cbb6`  
		Last Modified: Fri, 19 Dec 2025 02:14:42 GMT  
		Size: 21.3 MB (21300844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:apache-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:9d16f97f3cfa04c393043336b9c532f1c97868f44af44fe770ccec2a467ba06f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7124763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ded682264642e981424f1d3684229c97e966fc6ec123450e3209b00614d1b1ea`

```dockerfile
```

-	Layers:
	-	`sha256:738c3c22d5ba7dcbf12724721eaf4b612a0fa698004c0d14f611ed99a8f90e8f`  
		Last Modified: Fri, 19 Dec 2025 06:06:45 GMT  
		Size: 7.1 MB (7080617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99b011e619723ae87958c37c14067c7633b1de0ad53e8033c908c1e1a7fcec3d`  
		Last Modified: Fri, 19 Dec 2025 06:06:46 GMT  
		Size: 44.1 KB (44146 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:apache-bookworm` - linux; 386

```console
$ docker pull drupal@sha256:04291b58fa8b4cf41213921eeda09bcd2944d6033939b7338be5affc763f79e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.7 MB (202709101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69f41bc18345c90bee786ae08f8f2dbb8359ad2d7f6948d44d64da5657e4723e`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1765152000'
# Fri, 19 Dec 2025 01:27:06 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 19 Dec 2025 01:27:20 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 19 Dec 2025 01:27:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Dec 2025 01:27:20 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 19 Dec 2025 01:27:20 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 19 Dec 2025 01:27:20 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 19 Dec 2025 01:27:20 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 19 Dec 2025 01:27:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 19 Dec 2025 01:27:27 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 19 Dec 2025 01:27:27 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 19 Dec 2025 01:27:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Dec 2025 01:27:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Dec 2025 01:27:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 19 Dec 2025 01:27:27 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 19 Dec 2025 01:27:27 GMT
ENV PHP_VERSION=8.4.16
# Fri, 19 Dec 2025 01:27:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.16.tar.xz.asc
# Fri, 19 Dec 2025 01:27:27 GMT
ENV PHP_SHA256=f66f8f48db34e9e29f7bfd6901178e9cf4a1b163e6e497716dfcb8f88bcfae30
# Fri, 19 Dec 2025 01:27:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 19 Dec 2025 01:27:35 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 01:30:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 19 Dec 2025 01:30:08 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 01:30:08 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 19 Dec 2025 01:30:08 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 19 Dec 2025 01:30:08 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 19 Dec 2025 01:30:08 GMT
STOPSIGNAL SIGWINCH
# Fri, 19 Dec 2025 01:30:08 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 01:30:08 GMT
WORKDIR /var/www/html
# Fri, 19 Dec 2025 01:30:08 GMT
EXPOSE map[80/tcp:{}]
# Fri, 19 Dec 2025 01:30:08 GMT
CMD ["apache2-foreground"]
# Fri, 19 Dec 2025 02:14:25 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Dec 2025 02:14:25 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 19 Dec 2025 02:14:25 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Fri, 19 Dec 2025 02:14:26 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 02:14:26 GMT
ENV DRUPAL_VERSION=11.3.1
# Fri, 19 Dec 2025 02:14:26 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 19 Dec 2025 02:14:26 GMT
WORKDIR /opt/drupal
# Fri, 19 Dec 2025 02:14:33 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 19 Dec 2025 02:14:33 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:e28a7f622a043206041afc8ed0d2b3d1b9bbffe3b724b994051e9d6dbc2f8a1e`  
		Last Modified: Mon, 08 Dec 2025 22:16:30 GMT  
		Size: 29.2 MB (29209729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:887f7141f266d6589868e38d376b96bc9dfb5204c7c672c2ae63438526c7d1c0`  
		Last Modified: Fri, 19 Dec 2025 01:30:39 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:008bf7bf55ac046e7d386cf0de42f71089599f2879813b750162b294138cb82a`  
		Last Modified: Fri, 19 Dec 2025 01:30:47 GMT  
		Size: 101.5 MB (101518100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70a5cee9d62aacea65315aac528907ae386f1c5b379dbbfed4bd0e48a61a5f4b`  
		Last Modified: Fri, 19 Dec 2025 01:30:39 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d881e71062293897f1d7cf01aa79bf86a70f08d76de5a1cf1011bced9bee881`  
		Last Modified: Fri, 19 Dec 2025 01:30:41 GMT  
		Size: 20.7 MB (20658357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029be5b92112a9657719f24f4846656fe039f94ad713f58383b6bf4f80a82ec2`  
		Last Modified: Fri, 19 Dec 2025 01:30:39 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2aa90202ef95110a2020a2f9a80bc2e87cbee68139a85912687acd60b831361`  
		Last Modified: Fri, 19 Dec 2025 01:30:39 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7805d5450a45a5055047978320285a705d93b3698e01f4a2dc041c2f4564ae0`  
		Last Modified: Fri, 19 Dec 2025 01:30:40 GMT  
		Size: 13.8 MB (13789024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:458c1b5b3dca79823e8783c326a527b80996ff91a86c32007e436cf0f55f8558`  
		Last Modified: Fri, 19 Dec 2025 01:30:39 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:514b6c1f3d2742dc17bed69c9f3cfe8a4ccb13edc5bdd337a75205880a983485`  
		Last Modified: Fri, 19 Dec 2025 01:30:40 GMT  
		Size: 13.8 MB (13801784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:892ca7b927fe86e251a683618982bb1a0aa3d762c7f7a78632fe844c6e389155`  
		Last Modified: Fri, 19 Dec 2025 01:30:39 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6692433bdb0d59b10998852a359897228268dba763386c10d5c65973d188b664`  
		Last Modified: Fri, 19 Dec 2025 01:30:38 GMT  
		Size: 253.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c54a2e63fc6338ee9f1e0cdb47de186ea2ae7a18c7cf42eb35d71c914b5db20`  
		Last Modified: Fri, 19 Dec 2025 01:30:38 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5702c57c8ecf15e878b0e8ba55dc7c7f1cc7859f710ebc346c659c9b8243b077`  
		Last Modified: Fri, 19 Dec 2025 01:30:38 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c0a39ebad364f67b68f9a6e5a72d89f61c6e36139267b2fc1532476d6ded2b4`  
		Last Modified: Fri, 19 Dec 2025 02:14:56 GMT  
		Size: 1.6 MB (1646741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f7ab1d1a74e0d77db641ec3b72e474f54555e69973d5097078659f7a4b2748b`  
		Last Modified: Fri, 19 Dec 2025 02:14:56 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d5450057a277dfb3dc1a80bd2639814429827536f2f3ae0f1257bb4a6a9675c`  
		Last Modified: Fri, 19 Dec 2025 02:14:56 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b08cade45021c044c28708ec9733eeb695573616ef3e1557cd458fd2a882e107`  
		Last Modified: Fri, 19 Dec 2025 02:14:56 GMT  
		Size: 778.0 KB (778003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04645bb3cbb578019ad66102e5b79ba178c8cdafd02f04445fe71f82f00128e4`  
		Last Modified: Fri, 19 Dec 2025 02:14:56 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d19417eeb59090e467655e80564ee639e2102ae37b235bf69c4a7ecf38ab6dfd`  
		Last Modified: Fri, 19 Dec 2025 02:14:58 GMT  
		Size: 21.3 MB (21300939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:apache-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:824d1f81eff7c0d29dad83eca3d8cd1de6dc34ac9be4a21a58e6e294b0f75dae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7075748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56d75004d61c77e5d991c2883b03ec0aedb06248795150f19e55f1e4ecabc52d`

```dockerfile
```

-	Layers:
	-	`sha256:baa7651b9d242b2656bc853040fea948e657406b2e26886b75fda5005b5dee13`  
		Last Modified: Fri, 19 Dec 2025 06:06:52 GMT  
		Size: 7.0 MB (7031884 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d5a64e30695df56b84c131aeeb25f3d6543a2ec60129ae441bd98ac95b98600`  
		Last Modified: Fri, 19 Dec 2025 06:06:53 GMT  
		Size: 43.9 KB (43864 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:apache-bookworm` - linux; ppc64le

```console
$ docker pull drupal@sha256:0a734c405dc4332a5fc2889c39097834c2f0cc95e312d9900b00023c5d1aadc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.3 MB (208286014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b521153c1591c45f9e55913028c47e1fbdc1f3f16a613e63df9248e3c4c6e65a`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 12:44:37 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 09 Dec 2025 12:45:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 09 Dec 2025 12:45:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 12:45:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 09 Dec 2025 12:45:25 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 09 Dec 2025 12:45:25 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 09 Dec 2025 12:45:25 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 09 Dec 2025 12:51:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 09 Dec 2025 12:51:12 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 09 Dec 2025 12:51:13 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 09 Dec 2025 12:51:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 09 Dec 2025 12:51:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 09 Dec 2025 12:51:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 09 Dec 2025 12:51:13 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 09 Dec 2025 12:51:13 GMT
ENV PHP_VERSION=8.4.16
# Tue, 09 Dec 2025 12:51:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.16.tar.xz.asc
# Tue, 09 Dec 2025 12:51:13 GMT
ENV PHP_SHA256=f66f8f48db34e9e29f7bfd6901178e9cf4a1b163e6e497716dfcb8f88bcfae30
# Fri, 19 Dec 2025 02:00:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 19 Dec 2025 02:00:23 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 02:04:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 19 Dec 2025 02:04:18 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 02:04:20 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 19 Dec 2025 02:04:21 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 19 Dec 2025 02:04:21 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 19 Dec 2025 02:04:21 GMT
STOPSIGNAL SIGWINCH
# Fri, 19 Dec 2025 02:04:22 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 02:04:23 GMT
WORKDIR /var/www/html
# Fri, 19 Dec 2025 02:04:23 GMT
EXPOSE map[80/tcp:{}]
# Fri, 19 Dec 2025 02:04:23 GMT
CMD ["apache2-foreground"]
# Fri, 19 Dec 2025 02:34:59 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Dec 2025 02:34:59 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 19 Dec 2025 02:35:00 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Fri, 19 Dec 2025 02:35:00 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 02:35:00 GMT
ENV DRUPAL_VERSION=11.3.1
# Fri, 19 Dec 2025 02:35:00 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 19 Dec 2025 02:35:00 GMT
WORKDIR /opt/drupal
# Fri, 19 Dec 2025 02:35:20 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 19 Dec 2025 02:35:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:85c696326521b18996e4f030a7e27e2c57ad4956710f12ec3011da2c017e09ad`  
		Last Modified: Tue, 09 Dec 2025 09:15:52 GMT  
		Size: 32.1 MB (32068845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db7fbfa9a935f96015448b226c612416546538a1dcc52e55d20077b60dc138df`  
		Last Modified: Tue, 09 Dec 2025 12:51:07 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb33d06e000eb34d612247e4138286d5e898db5da65f963214e6d898b0fcd65`  
		Last Modified: Tue, 09 Dec 2025 12:51:17 GMT  
		Size: 103.3 MB (103329018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e40fa0c3ff80077d169fd45b8fbcf082c8de27581241e80d2c54a3edd2591a4`  
		Last Modified: Tue, 09 Dec 2025 12:51:07 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:231e39ac6179aacbf25d364d78fd814c69de366cbb654ba168ce29a3f513972f`  
		Last Modified: Tue, 09 Dec 2025 12:56:55 GMT  
		Size: 21.3 MB (21318007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0dee34846779660512ad78cede3a13043397aeb2b2107d9017b6078a6d00b3a`  
		Last Modified: Tue, 09 Dec 2025 12:56:54 GMT  
		Size: 439.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4798c347c2e1d6893d691bab3a8901ee08329f6292693da798fcac91fb1cd45e`  
		Last Modified: Tue, 09 Dec 2025 12:56:54 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b242cb949c1ad3ee053870fc611423c18958aaa8cad25cc04385116c29c4d07`  
		Last Modified: Fri, 19 Dec 2025 02:05:00 GMT  
		Size: 13.8 MB (13789799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d38c8ea8b9e52c91795b70ef43a2bf082005ad8b50ca9ad783f96c3950045173`  
		Last Modified: Fri, 19 Dec 2025 02:04:57 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:428d434b37a91b8cad111c1c4c6170ddc0b20c28e4ecad55e4349861af87ecd9`  
		Last Modified: Fri, 19 Dec 2025 02:04:59 GMT  
		Size: 13.9 MB (13918368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80e3b8b7a24e99d69c9bd15d7deab95b5606c91fec99932013d9362f1aedc27e`  
		Last Modified: Fri, 19 Dec 2025 02:05:00 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9b9d19d57506465ae511c68bbd70966274f07dba13143d7c827657fb5ef15e6`  
		Last Modified: Fri, 19 Dec 2025 02:05:03 GMT  
		Size: 253.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbbab6f7188b5422909dda5dc68f015c0770b915a0e9ea5b1f54f70d68df1b05`  
		Last Modified: Fri, 19 Dec 2025 02:04:57 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31ea1344f12fe2978f088f64ac0007234b3a2f1b16be17b38aec721ac5f07de9`  
		Last Modified: Fri, 19 Dec 2025 02:04:57 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b430499a973a1009c2843cb439fd05df868af1129845cc421a7dc768ffd5d5c1`  
		Last Modified: Fri, 19 Dec 2025 02:36:17 GMT  
		Size: 1.8 MB (1776664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77054043cfc16d68683a3bffb6009be09ee5dba237c0f152a589d012fad8b83d`  
		Last Modified: Fri, 19 Dec 2025 02:36:17 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2ed8f1f8f1924c09175cd35dc1e0adadd1d63b770131c61c173b26b31972434`  
		Last Modified: Fri, 19 Dec 2025 02:36:17 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe916b21636ec5a67ec0f8d2a0af91411a7a8320de18e03e5e222855f0051bba`  
		Last Modified: Fri, 19 Dec 2025 02:36:19 GMT  
		Size: 778.0 KB (777997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a589365c33bfcafba91623d3dc9c74f205dbc3d658298b25e90865842860ba7`  
		Last Modified: Fri, 19 Dec 2025 02:36:14 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf53e32f17d7827c1dfa24945f36d9bcbf7d65e5505893ef28779b40e27be2d`  
		Last Modified: Fri, 19 Dec 2025 02:36:19 GMT  
		Size: 21.3 MB (21300877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:apache-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:b1e8c4fbfadbb080d850a65480ae96773af80c27608e8fe4e2f6b536b107979d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7073030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:086ba0936ad0186537c3fac68cc44651251667f834955b1381ce138a401f6896`

```dockerfile
```

-	Layers:
	-	`sha256:aece74939159d7bca16980d361597e329947091737f1400a3157883e05f9781a`  
		Last Modified: Fri, 19 Dec 2025 06:06:59 GMT  
		Size: 7.0 MB (7029016 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:070d31efc3b31f21866d75ead33e3b071f4b103fd981211076b6ebb5bb62e54d`  
		Last Modified: Fri, 19 Dec 2025 06:06:59 GMT  
		Size: 44.0 KB (44014 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:apache-bookworm` - linux; s390x

```console
$ docker pull drupal@sha256:a26d68b1cb16fbf4a144c232d0e2b24be6925d1442aeebd7fe381dff6648c9c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.5 MB (177548367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fe74117beb549dc8838bd006ba50ef2c771a891c86e9537e529e58119c61196`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 22:39:37 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Mon, 08 Dec 2025 22:39:50 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Mon, 08 Dec 2025 22:39:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:39:50 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 08 Dec 2025 22:39:50 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 08 Dec 2025 22:39:50 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Mon, 08 Dec 2025 22:39:50 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Mon, 08 Dec 2025 22:41:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Mon, 08 Dec 2025 22:41:37 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Mon, 08 Dec 2025 22:41:37 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Mon, 08 Dec 2025 22:41:37 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 08 Dec 2025 22:41:37 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 08 Dec 2025 22:41:37 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 08 Dec 2025 22:41:37 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 08 Dec 2025 22:41:37 GMT
ENV PHP_VERSION=8.4.16
# Mon, 08 Dec 2025 22:41:37 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.16.tar.xz.asc
# Mon, 08 Dec 2025 22:41:37 GMT
ENV PHP_SHA256=f66f8f48db34e9e29f7bfd6901178e9cf4a1b163e6e497716dfcb8f88bcfae30
# Fri, 19 Dec 2025 01:29:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 19 Dec 2025 01:29:39 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 01:33:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 19 Dec 2025 01:33:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 01:33:32 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 19 Dec 2025 01:33:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 19 Dec 2025 01:33:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 19 Dec 2025 01:33:32 GMT
STOPSIGNAL SIGWINCH
# Fri, 19 Dec 2025 01:33:32 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 01:33:32 GMT
WORKDIR /var/www/html
# Fri, 19 Dec 2025 01:33:32 GMT
EXPOSE map[80/tcp:{}]
# Fri, 19 Dec 2025 01:33:32 GMT
CMD ["apache2-foreground"]
# Fri, 19 Dec 2025 02:14:35 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Dec 2025 02:14:35 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 19 Dec 2025 02:14:35 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Fri, 19 Dec 2025 02:14:35 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 02:14:35 GMT
ENV DRUPAL_VERSION=11.3.1
# Fri, 19 Dec 2025 02:14:35 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 19 Dec 2025 02:14:35 GMT
WORKDIR /opt/drupal
# Fri, 19 Dec 2025 02:14:41 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 19 Dec 2025 02:14:41 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:00a29f44cb5b31bbcf043ec5426ee1c018bb26435350712cb5e48d56c6d95792`  
		Last Modified: Mon, 08 Dec 2025 22:15:04 GMT  
		Size: 26.9 MB (26884429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff59590fe30695d1ffd23bb7d8622df2a77cc7800e6c3aa421f22ce474987016`  
		Last Modified: Mon, 08 Dec 2025 22:43:06 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdef6ee94f92dd0fa59fbc5f6f5418bba11da257e220868dc20d549ad69f125a`  
		Last Modified: Mon, 08 Dec 2025 22:43:14 GMT  
		Size: 80.8 MB (80826131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dd54d2594315014142dee111781b094a6ff8ba13816f8fbefaa8547b4b096d3`  
		Last Modified: Mon, 08 Dec 2025 22:43:06 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d07e2a20f67f83e4b0eaa8bc30d535bd69cef07dd239cfcbddc5d560fd820179`  
		Last Modified: Mon, 08 Dec 2025 22:44:56 GMT  
		Size: 19.9 MB (19910389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be24307575a611ffc82ce46c006bd5c150e8f50be367d9f74116ad0b9e1b2f9d`  
		Last Modified: Mon, 08 Dec 2025 22:44:52 GMT  
		Size: 435.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37cb2c3f05de2ec6367a9319b094bb59c17db8cd3bdc1c405d104aeabe9983f1`  
		Last Modified: Mon, 08 Dec 2025 22:44:52 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:601feb44957292b425beeb8cc425fdec54ee8f063432a124f64b244e4bb18ac9`  
		Last Modified: Fri, 19 Dec 2025 01:33:56 GMT  
		Size: 13.8 MB (13788615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d746f1200c61c2c0e71349e9d51b8ddb686f12cdc1f0b16ca6a7245d02c4bf34`  
		Last Modified: Fri, 19 Dec 2025 01:33:55 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:958da0c1ddd49af401f3bc8a1c4bef9a39c197ee52e31d17513596376a7ea937`  
		Last Modified: Fri, 19 Dec 2025 01:33:57 GMT  
		Size: 12.6 MB (12568076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a3c324cd73a1f4b9ec001daf6e870fef89cdf3dcada52032a5b452712287b60`  
		Last Modified: Fri, 19 Dec 2025 01:33:55 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59ad2a9aa9f89d99f67eb80e1177f2c1e6e430429b79a77bc1dac75112ec7ed1`  
		Last Modified: Fri, 19 Dec 2025 01:33:55 GMT  
		Size: 254.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad0328b7dbd5f52c30da61c9f50eb38a35116556705ffd99138730691cfb5dba`  
		Last Modified: Fri, 19 Dec 2025 01:33:55 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:977c0969f4e98042b4c116e8d515fbce286ae9543e20f357c8bfb1ce7761afb9`  
		Last Modified: Fri, 19 Dec 2025 01:33:55 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c50e564e064742a2d61f688a51de65fd1201f5b2ff9dd7f3cb19919fc1bd5bc4`  
		Last Modified: Fri, 19 Dec 2025 02:15:16 GMT  
		Size: 1.5 MB (1485448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1902d50665ecc898798dec63f82253f2178a7798ace2b9769f1cd5c6a43ac636`  
		Last Modified: Fri, 19 Dec 2025 02:15:16 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d688ef68d6fc896921b5f280b3a0b81dc1f9856b6a9189e54b4f25c33cf399f`  
		Last Modified: Fri, 19 Dec 2025 02:15:16 GMT  
		Size: 260.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfd28e6768632c2aafad1644b2b5b4301b76eec50dd98c427339ac59cfd759b3`  
		Last Modified: Fri, 19 Dec 2025 02:15:16 GMT  
		Size: 778.0 KB (778004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4c1632deb4676c6a0656a0fed4d1296a40f8cf895e71d9b615ad7c1ddf71dda`  
		Last Modified: Fri, 19 Dec 2025 02:15:03 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a886eb85c1b6d69e01e57d6a82657eec22997cb464a22af389965d18aa97d93`  
		Last Modified: Fri, 19 Dec 2025 02:15:21 GMT  
		Size: 21.3 MB (21300843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:apache-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:724856de3cad84c76b439a37991c2fa99f83f9e3632ae511f2ea69f7fa5a4119
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6933281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dc749843df4b530a4544c9d5c5c6c43f94caef1d3bc96e5e3aed08eb6823782`

```dockerfile
```

-	Layers:
	-	`sha256:4167bc03fbd7d03e9f198047e12daa844bbd272dff9758fcfa3d7def8a26cd4b`  
		Last Modified: Fri, 19 Dec 2025 06:07:06 GMT  
		Size: 6.9 MB (6889358 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a4493b649f3873e5cc5e7ff086a3979c3d5288d2c6fa90bed6ea284263c0e7a`  
		Last Modified: Fri, 19 Dec 2025 06:07:07 GMT  
		Size: 43.9 KB (43923 bytes)  
		MIME: application/vnd.in-toto+json
