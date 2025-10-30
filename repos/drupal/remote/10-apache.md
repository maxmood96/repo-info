## `drupal:10-apache`

```console
$ docker pull drupal@sha256:cb5f705a898e6e56c919b28563f4008f9a9d3d075e87ab6f82aeed98f5e36857
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
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
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `drupal:10-apache` - linux; amd64

```console
$ docker pull drupal@sha256:1796867f5278748c23cf3f50ef8c8f02bbe95773f7c6585f84f8a57a42ad245a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.3 MB (203332515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:068b440589fac4a86bcfb73e10f66809faf39b03e31efcbf3c9f02da9d427afb`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 02 Oct 2025 09:27:16 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1760918400'
# Thu, 02 Oct 2025 09:27:16 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 02 Oct 2025 09:27:16 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 02 Oct 2025 09:27:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 02 Oct 2025 09:27:16 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 02 Oct 2025 09:27:16 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 02 Oct 2025 09:27:16 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 02 Oct 2025 09:27:16 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 02 Oct 2025 09:27:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 02 Oct 2025 09:27:16 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 02 Oct 2025 09:27:16 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 02 Oct 2025 09:27:16 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 02 Oct 2025 09:27:16 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 02 Oct 2025 09:27:16 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 02 Oct 2025 09:27:16 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 02 Oct 2025 09:27:16 GMT
ENV PHP_VERSION=8.4.14
# Thu, 02 Oct 2025 09:27:16 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.14.tar.xz.asc
# Thu, 02 Oct 2025 09:27:16 GMT
ENV PHP_SHA256=bac90ee7cf738e814c89b6b27d4d2c4b70e50942a420837e1a22f5fd5f9867a3
# Thu, 02 Oct 2025 09:27:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 02 Oct 2025 09:27:16 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 02 Oct 2025 09:27:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 02 Oct 2025 09:27:16 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 02 Oct 2025 09:27:16 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 02 Oct 2025 09:27:16 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 02 Oct 2025 09:27:16 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 02 Oct 2025 09:27:16 GMT
STOPSIGNAL SIGWINCH
# Thu, 02 Oct 2025 09:27:16 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 02 Oct 2025 09:27:16 GMT
WORKDIR /var/www/html
# Thu, 02 Oct 2025 09:27:16 GMT
EXPOSE map[80/tcp:{}]
# Thu, 02 Oct 2025 09:27:16 GMT
CMD ["apache2-foreground"]
# Thu, 02 Oct 2025 09:27:16 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Oct 2025 09:27:16 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 02 Oct 2025 09:27:16 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Thu, 02 Oct 2025 09:27:16 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 02 Oct 2025 09:27:16 GMT
ENV DRUPAL_VERSION=10.5.4
# Thu, 02 Oct 2025 09:27:16 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 02 Oct 2025 09:27:16 GMT
WORKDIR /opt/drupal
# Thu, 02 Oct 2025 09:27:16 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 02 Oct 2025 09:27:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:38513bd7256313495cdd83b3b0915a633cfa475dc2a07072ab2c8d191020ca5d`  
		Last Modified: Tue, 21 Oct 2025 00:20:31 GMT  
		Size: 29.8 MB (29777924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:537d478c98968841134f50e0dfbf60d5624d9200fe51ed6b49981e430ff49c20`  
		Last Modified: Fri, 24 Oct 2025 19:24:35 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a15a575bf80081b5a4119dca7ad7117097ddbf96ef117127a7ce7fa582cbe87a`  
		Last Modified: Fri, 24 Oct 2025 19:24:48 GMT  
		Size: 117.8 MB (117837892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b521dae649cff96f77a31f319284ba1e558705a9bfa9f4051c27009b058327f`  
		Last Modified: Fri, 24 Oct 2025 19:24:36 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8896f13e90f100dc05a31a6c198376865a16f3045f92ae2150f82c872f66885`  
		Last Modified: Fri, 24 Oct 2025 19:24:33 GMT  
		Size: 4.2 MB (4224020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7aa74542cca1be9f81c5a601de2fdf307ccaeae7b9d36efaabf83c09fc627fc`  
		Last Modified: Fri, 24 Oct 2025 19:24:32 GMT  
		Size: 426.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a78dff104ff24011b1aee6459bc6321a42a52baf9690e6db682b7c1b1abc7a0a`  
		Last Modified: Fri, 24 Oct 2025 19:24:32 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35b6949f69ebfcb03496ac25d0b905e464ca6157df7a346ef6a35e23bc666f10`  
		Last Modified: Fri, 24 Oct 2025 19:24:36 GMT  
		Size: 13.8 MB (13810288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cc1f433822137e7bd7da3e8729ab665fd2eab81ea3782fdbb53c2e816fd59fd`  
		Last Modified: Fri, 24 Oct 2025 19:24:34 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f82b10671d662dab6407ca395cb4c37e6e0f7dc1c2e0d8702bd082518df5f424`  
		Last Modified: Fri, 24 Oct 2025 19:24:33 GMT  
		Size: 13.5 MB (13529971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ab44828dc41688d4ec13d48dc39ebe724f2b603622050d291299e9b49f0938d`  
		Last Modified: Fri, 24 Oct 2025 19:24:33 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df1bcf657709bde5d60115514a6cdb3a3c8b8f82379e0ca132db3ece77b43034`  
		Last Modified: Fri, 24 Oct 2025 19:24:35 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4054bbc52c889df9f0da3e5b7864e52da590c7119f0bd52249f885e5a007840`  
		Last Modified: Fri, 24 Oct 2025 19:24:33 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9003a201e215883f5f439e755f70a1ada4c178723439310585cecc35c49d03e`  
		Last Modified: Fri, 24 Oct 2025 19:24:32 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6177ee874780cd907af0e59d3f69977ec00dac8653036a492eba0dbe882203e`  
		Last Modified: Fri, 24 Oct 2025 21:20:20 GMT  
		Size: 1.7 MB (1656260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a83f995040e2f4046fcb6dd3ca24d742ad72880e554bff1180f86d5844f72d8f`  
		Last Modified: Fri, 24 Oct 2025 21:20:20 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94bc9b138b3e2193a2dc36aeca275ef14c20ac138e064402db0658740397d9fb`  
		Last Modified: Fri, 24 Oct 2025 21:20:20 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3190251f1dab92e571ccdeae4464c23caf5c66d2fd1524dc36c3dd32451fba63`  
		Last Modified: Fri, 24 Oct 2025 21:20:20 GMT  
		Size: 751.5 KB (751478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02ab727a82811fa995298fa5695b0b89ca58a20393b900a44a824b02671dbc6c`  
		Last Modified: Fri, 24 Oct 2025 21:20:20 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbd516e9eb4b42d21f4eae39291eb33f08c2e9cdfa79de6284edf0ea12245c7f`  
		Last Modified: Fri, 24 Oct 2025 21:20:21 GMT  
		Size: 21.7 MB (21738285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-apache` - unknown; unknown

```console
$ docker pull drupal@sha256:4d8fac3cdf79954320001e0ef10681bd1c52e00416b126f6ab2e974f94f94626
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7381155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a0d031f2fea1cdb105aed2c25eaba0a506366bde2247ce9f91bead18f6f3058`

```dockerfile
```

-	Layers:
	-	`sha256:06fbc238bef7d3f7382a1100857e507b1d3f84cf52ebbef7b682de66b263258b`  
		Last Modified: Fri, 24 Oct 2025 22:53:38 GMT  
		Size: 7.3 MB (7334014 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9db2cc37a4fb8e622742161c6c609dd5d9e309a98ecbee7f23efc52f5ae07ae0`  
		Last Modified: Fri, 24 Oct 2025 22:53:39 GMT  
		Size: 47.1 KB (47141 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-apache` - linux; arm variant v7

```console
$ docker pull drupal@sha256:2ec1d2d77273a435b07993f3b6f6805445f4b00f89220ac43efdf482b5fd8183
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.5 MB (165494683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19911b1caa7d70e65ca2e263ce8d849eaee7896988aeaf6a5200135b4fbda726`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 02 Oct 2025 09:27:16 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1760918400'
# Thu, 02 Oct 2025 09:27:16 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 02 Oct 2025 09:27:16 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 02 Oct 2025 09:27:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 02 Oct 2025 09:27:16 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 02 Oct 2025 09:27:16 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 02 Oct 2025 09:27:16 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 02 Oct 2025 09:27:16 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 02 Oct 2025 09:27:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 02 Oct 2025 09:27:16 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 02 Oct 2025 09:27:16 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 02 Oct 2025 09:27:16 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 02 Oct 2025 09:27:16 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 02 Oct 2025 09:27:16 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 02 Oct 2025 09:27:16 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 02 Oct 2025 09:27:16 GMT
ENV PHP_VERSION=8.4.14
# Thu, 02 Oct 2025 09:27:16 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.14.tar.xz.asc
# Thu, 02 Oct 2025 09:27:16 GMT
ENV PHP_SHA256=bac90ee7cf738e814c89b6b27d4d2c4b70e50942a420837e1a22f5fd5f9867a3
# Thu, 02 Oct 2025 09:27:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 02 Oct 2025 09:27:16 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 02 Oct 2025 09:27:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 02 Oct 2025 09:27:16 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 02 Oct 2025 09:27:16 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 02 Oct 2025 09:27:16 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 02 Oct 2025 09:27:16 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 02 Oct 2025 09:27:16 GMT
STOPSIGNAL SIGWINCH
# Thu, 02 Oct 2025 09:27:16 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 02 Oct 2025 09:27:16 GMT
WORKDIR /var/www/html
# Thu, 02 Oct 2025 09:27:16 GMT
EXPOSE map[80/tcp:{}]
# Thu, 02 Oct 2025 09:27:16 GMT
CMD ["apache2-foreground"]
# Thu, 02 Oct 2025 09:27:16 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Oct 2025 09:27:16 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 02 Oct 2025 09:27:16 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Thu, 02 Oct 2025 09:27:16 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 02 Oct 2025 09:27:16 GMT
ENV DRUPAL_VERSION=10.5.4
# Thu, 02 Oct 2025 09:27:16 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 02 Oct 2025 09:27:16 GMT
WORKDIR /opt/drupal
# Thu, 02 Oct 2025 09:27:16 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 02 Oct 2025 09:27:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:f157a4589edc88a89367c83c97b73205a4a80cffc6af7a71b789000a1bc8763e`  
		Last Modified: Tue, 21 Oct 2025 00:20:54 GMT  
		Size: 26.2 MB (26212894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:682aa22887a27acc5b1bff7877237f2ead9d5a19224856dd2e8c71fa409e201b`  
		Last Modified: Fri, 24 Oct 2025 19:42:56 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df0e312798854fb5569f67e5439373d2302ff8d9d9dc78e9e67ce09172488933`  
		Last Modified: Fri, 24 Oct 2025 19:43:07 GMT  
		Size: 86.2 MB (86245952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ef2613e3bbfeed85768b7161fd7bc123b5b6a788a4ab2df259d398b2bb62828`  
		Last Modified: Fri, 24 Oct 2025 19:42:56 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddfa9a0edec77c33f74e66bff981cb4b8006eaae2a6c082953a4e8e674efd3d1`  
		Last Modified: Fri, 24 Oct 2025 19:42:56 GMT  
		Size: 3.8 MB (3751987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a27350ec6bca4d503655de812f9faff3e7df84a59f08d7d909e3c5375e257323`  
		Last Modified: Fri, 24 Oct 2025 19:42:56 GMT  
		Size: 427.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de91b867c55f48ba7c14099f81c6094d631b64e6025697a4e0c89825c9e44588`  
		Last Modified: Fri, 24 Oct 2025 19:42:56 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03d5e5e780cb47bd8cc7f1479f85d0c91293739231a1cc7c8a8b3b6e7c8ba16a`  
		Last Modified: Fri, 24 Oct 2025 19:54:00 GMT  
		Size: 13.8 MB (13807940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d84479c1b692ba6d39aa4bed758b81898bbb922387266c0e649a51f82563d3c`  
		Last Modified: Fri, 24 Oct 2025 19:53:57 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0eb2656e18eb399e38896196eafaf50316fd6e2636c45cc087dd3988a436f33`  
		Last Modified: Fri, 24 Oct 2025 19:53:58 GMT  
		Size: 11.6 MB (11609132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e5fc9966ca6a7de4d0b83462745caec236b02cda2190c0e534f091b2d71aff5`  
		Last Modified: Fri, 24 Oct 2025 19:53:57 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a8d00d981993367f05d035d91bba86e172484800d8dc6401c817e458a6bd41`  
		Last Modified: Fri, 24 Oct 2025 19:53:57 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:195b3144e7e256265371421a52cb083cb15b26380b1f3e08a16a7fff18756858`  
		Last Modified: Fri, 24 Oct 2025 19:53:57 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8490bc74a5f87eb0d136b8f53ea3e0071f79a879e51bb01a3876446d2120ab00`  
		Last Modified: Fri, 24 Oct 2025 19:53:57 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20932d42de1750c916e0895d104c1f8b7647e4fd18d0733f88dea5a338daad35`  
		Last Modified: Fri, 24 Oct 2025 21:59:19 GMT  
		Size: 1.4 MB (1370356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8479e06813817a255ff3318f3de5cca1051a46244846e5a43d308d2427b3ee13`  
		Last Modified: Fri, 24 Oct 2025 21:59:19 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba09bf0be65652652883d4d6fdde80dec9e83179d1600b163d9c560f2cd03110`  
		Last Modified: Fri, 24 Oct 2025 21:59:19 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5854088e10a1d95936ace5a8a0a29f2106c2add7099acd0f78b4a084882b195`  
		Last Modified: Fri, 24 Oct 2025 21:59:19 GMT  
		Size: 751.5 KB (751478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3b3b29af405bf15df0fbba9ac3632ffa2ce382e6f28ab354876d484a0724cbf`  
		Last Modified: Fri, 24 Oct 2025 21:59:19 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1908ee59400e77b8906edde25da90f9cb0a7f0185f2de4d0392cf6425a23216`  
		Last Modified: Fri, 24 Oct 2025 21:59:21 GMT  
		Size: 21.7 MB (21738527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-apache` - unknown; unknown

```console
$ docker pull drupal@sha256:3a79e92b20db04b6d8dd7abd27f45963a90e23a4e31fd387a83cc864250e46d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7185362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4225f9645e29f37a9a6847bd1a21bb6169cd327c59b926f44fd97a6e7482cfda`

```dockerfile
```

-	Layers:
	-	`sha256:42277b49bc20a34b59587ce67c0e2dbf66cafa166c027e9b10de65ff86407fb8`  
		Last Modified: Fri, 24 Oct 2025 22:53:45 GMT  
		Size: 7.1 MB (7137975 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6eed4408c627f9546e02f5df25c61a1c31ae98871ea3b079a753ceea5d3bcb0d`  
		Last Modified: Fri, 24 Oct 2025 22:53:46 GMT  
		Size: 47.4 KB (47387 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-apache` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:7681d765f8ecd577263c33b17df24047837f2d81c010c08c027c4227cf76c8f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.7 MB (195711088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d90464d6268bc631efd3044615afe52f241ac84b30f0de9fa9b2d19897734b19`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 02 Oct 2025 09:27:16 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1760918400'
# Thu, 02 Oct 2025 09:27:16 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 02 Oct 2025 09:27:16 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 02 Oct 2025 09:27:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 02 Oct 2025 09:27:16 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 02 Oct 2025 09:27:16 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 02 Oct 2025 09:27:16 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 02 Oct 2025 09:27:16 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 02 Oct 2025 09:27:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 02 Oct 2025 09:27:16 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 02 Oct 2025 09:27:16 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 02 Oct 2025 09:27:16 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 02 Oct 2025 09:27:16 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 02 Oct 2025 09:27:16 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 02 Oct 2025 09:27:16 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 02 Oct 2025 09:27:16 GMT
ENV PHP_VERSION=8.4.14
# Thu, 02 Oct 2025 09:27:16 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.14.tar.xz.asc
# Thu, 02 Oct 2025 09:27:16 GMT
ENV PHP_SHA256=bac90ee7cf738e814c89b6b27d4d2c4b70e50942a420837e1a22f5fd5f9867a3
# Thu, 02 Oct 2025 09:27:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 02 Oct 2025 09:27:16 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 02 Oct 2025 09:27:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 02 Oct 2025 09:27:16 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 02 Oct 2025 09:27:16 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 02 Oct 2025 09:27:16 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 02 Oct 2025 09:27:16 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 02 Oct 2025 09:27:16 GMT
STOPSIGNAL SIGWINCH
# Thu, 02 Oct 2025 09:27:16 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 02 Oct 2025 09:27:16 GMT
WORKDIR /var/www/html
# Thu, 02 Oct 2025 09:27:16 GMT
EXPOSE map[80/tcp:{}]
# Thu, 02 Oct 2025 09:27:16 GMT
CMD ["apache2-foreground"]
# Thu, 02 Oct 2025 09:27:16 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Oct 2025 09:27:16 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 02 Oct 2025 09:27:16 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Thu, 02 Oct 2025 09:27:16 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 02 Oct 2025 09:27:16 GMT
ENV DRUPAL_VERSION=10.5.4
# Thu, 02 Oct 2025 09:27:16 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 02 Oct 2025 09:27:16 GMT
WORKDIR /opt/drupal
# Thu, 02 Oct 2025 09:27:16 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 02 Oct 2025 09:27:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:a16e551192670581ec8359c70ab9eebf8f2af5468ffc79b3d4f9ce21b0366f47`  
		Last Modified: Tue, 21 Oct 2025 00:23:17 GMT  
		Size: 30.1 MB (30142127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9467c7c95e7020ed7be16fc2f746a5ed27814d2b147de74044e1e1bf5de1875`  
		Last Modified: Fri, 24 Oct 2025 19:09:41 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a821faee3d6093e46c0a8313e9b16602062f9dbf28e1cdb7f50d407ce604c5`  
		Last Modified: Fri, 24 Oct 2025 19:09:57 GMT  
		Size: 110.2 MB (110163560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af35348bebe3d2ff0bc38b23d3041248a6b3288f665d9930524113c7869d29fe`  
		Last Modified: Fri, 24 Oct 2025 19:09:41 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32ba68301d3616bc68ed8ac4e1d2dbce6812a8339c6857fb0bebd20cb408d9ff`  
		Last Modified: Fri, 24 Oct 2025 19:13:20 GMT  
		Size: 4.3 MB (4302127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bd67bf5e82d220c2f0e4f8a97afd09391a046c1037563b298c4c277df70f3c2`  
		Last Modified: Fri, 24 Oct 2025 19:13:20 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0c8318e72bffe68e84117fbc95eb53160b8ab1494e5cddd823ec8e9b53ef129`  
		Last Modified: Fri, 24 Oct 2025 19:13:20 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9dc4f32205568b53147c25ae44a7c74e71b193e5053c3be6ade4219d6d2a8d9`  
		Last Modified: Fri, 24 Oct 2025 19:13:21 GMT  
		Size: 13.8 MB (13809962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:811d7a479c0c156abe3c60f7315396e10ef6e5542fff8a1c8195e91fbe325f89`  
		Last Modified: Fri, 24 Oct 2025 19:13:20 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aaea12066ddb8f8623b68bc145fe57bec7d99c4a0959a4d9d441ab0f885e11b`  
		Last Modified: Fri, 24 Oct 2025 19:13:22 GMT  
		Size: 13.2 MB (13183102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:953d3dd36570d1ee32afa3e2d6e899fd99cb1493f59fab954d4c24959679b3fb`  
		Last Modified: Fri, 24 Oct 2025 19:13:20 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12590fd1e125dfd74da15bb76ffb0f0980f6da92fd881e1f20645c3849506c43`  
		Last Modified: Fri, 24 Oct 2025 19:13:20 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed81d9ada8286ffc1789e97f08e8946dca5095dc7aa73586ea7ac0cb5c6c788`  
		Last Modified: Fri, 24 Oct 2025 19:13:20 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a0c75f19385bbe30e29450bb0ff319d5f23f633683079637c017792f4c22e94`  
		Last Modified: Fri, 24 Oct 2025 19:13:21 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d8f01a1eafc59ae2cd0d784cf1713eb49f0ffaa69d6f6296a2e57f4f98f11b3`  
		Last Modified: Fri, 24 Oct 2025 21:41:15 GMT  
		Size: 1.6 MB (1613985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37b114eeeeab1dd6b2890560197eb25e272acbc5c7d03eac6badc332e6e3d223`  
		Last Modified: Fri, 24 Oct 2025 21:41:15 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7194774fa40b2e8ae3eb574fcc30d4fc603a96c34dc723512ef9fc05a6cc3c86`  
		Last Modified: Fri, 24 Oct 2025 21:41:15 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c142a01b870e8b07365f8930472c62de5e3cbe544796a32589f8f4de50424ac`  
		Last Modified: Fri, 24 Oct 2025 21:41:15 GMT  
		Size: 751.5 KB (751479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92da4cb88564479fc94e9dff72c7b5064a44847fb40c93889f57cd842831569b`  
		Last Modified: Fri, 24 Oct 2025 21:41:15 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecbedc2743312abeb5c80ccb22a3909644b40343c672067a199f8703e384b6cc`  
		Last Modified: Fri, 24 Oct 2025 21:41:18 GMT  
		Size: 21.7 MB (21738327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-apache` - unknown; unknown

```console
$ docker pull drupal@sha256:43680f4a0885c63bebb4aec17ffee59ce63e2ad5b2a480f1f4f9de4636b18113
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7478968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21567944cfc227febfe06efb7cc855433c3878791f5f6f039d38d7d2cd496df2`

```dockerfile
```

-	Layers:
	-	`sha256:24a431318de26bb023f3f0ff8be07f41fbc198c82504b4dfdf00e340d34c3359`  
		Last Modified: Fri, 24 Oct 2025 22:53:52 GMT  
		Size: 7.4 MB (7431484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d46327fc3b9ab17da720d2800055f46b49ff2c0b9cdc77c71fe83162c335f26f`  
		Last Modified: Fri, 24 Oct 2025 22:53:53 GMT  
		Size: 47.5 KB (47484 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-apache` - linux; 386

```console
$ docker pull drupal@sha256:4244e5b42b71aa5d7922bd49606660b1245d79d407526d48376ec65cdf249efb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.8 MB (203754428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c5b91448903bf78395f3f788c3281e10df024304bd244bc398e19cccf84a8db`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 02 Oct 2025 09:27:16 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1760918400'
# Thu, 02 Oct 2025 09:27:16 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 02 Oct 2025 09:27:16 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 02 Oct 2025 09:27:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 02 Oct 2025 09:27:16 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 02 Oct 2025 09:27:16 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 02 Oct 2025 09:27:16 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 02 Oct 2025 09:27:16 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 02 Oct 2025 09:27:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 02 Oct 2025 09:27:16 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 02 Oct 2025 09:27:16 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 02 Oct 2025 09:27:16 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 02 Oct 2025 09:27:16 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 02 Oct 2025 09:27:16 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 02 Oct 2025 09:27:16 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 02 Oct 2025 09:27:16 GMT
ENV PHP_VERSION=8.4.14
# Thu, 02 Oct 2025 09:27:16 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.14.tar.xz.asc
# Thu, 02 Oct 2025 09:27:16 GMT
ENV PHP_SHA256=bac90ee7cf738e814c89b6b27d4d2c4b70e50942a420837e1a22f5fd5f9867a3
# Thu, 02 Oct 2025 09:27:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 02 Oct 2025 09:27:16 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 02 Oct 2025 09:27:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 02 Oct 2025 09:27:16 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 02 Oct 2025 09:27:16 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 02 Oct 2025 09:27:16 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 02 Oct 2025 09:27:16 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 02 Oct 2025 09:27:16 GMT
STOPSIGNAL SIGWINCH
# Thu, 02 Oct 2025 09:27:16 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 02 Oct 2025 09:27:16 GMT
WORKDIR /var/www/html
# Thu, 02 Oct 2025 09:27:16 GMT
EXPOSE map[80/tcp:{}]
# Thu, 02 Oct 2025 09:27:16 GMT
CMD ["apache2-foreground"]
# Thu, 02 Oct 2025 09:27:16 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Oct 2025 09:27:16 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 02 Oct 2025 09:27:16 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Thu, 02 Oct 2025 09:27:16 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 02 Oct 2025 09:27:16 GMT
ENV DRUPAL_VERSION=10.5.4
# Thu, 02 Oct 2025 09:27:16 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 02 Oct 2025 09:27:16 GMT
WORKDIR /opt/drupal
# Thu, 02 Oct 2025 09:27:16 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 02 Oct 2025 09:27:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:c39cee8c4780ac17d9c2caff77324495220e917ba3f61826c72fe134724c1e4a`  
		Last Modified: Tue, 21 Oct 2025 00:20:54 GMT  
		Size: 31.3 MB (31294628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ffdc86f21321788352dc394fe2e54e566ec6ef8e853e954fcd078423b21d89`  
		Last Modified: Fri, 24 Oct 2025 18:35:45 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98caeff51209d6c947dd532c0b8a7f5f9778a1dfad02f9915ce4c876abfc4561`  
		Last Modified: Fri, 24 Oct 2025 18:36:03 GMT  
		Size: 116.1 MB (116138573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44d7ac7a932603770f090813bbb0e5ccb1f16bd9d122c361e4f4bedf79fa60d9`  
		Last Modified: Fri, 24 Oct 2025 18:35:45 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcb8eaa05b400e1f5e968136684c91558d9d5dc0cff8476eba96d45dfecc3f80`  
		Last Modified: Fri, 24 Oct 2025 18:39:17 GMT  
		Size: 4.5 MB (4455511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:125f491c731f75284aa09eca0e2540fd8be511771af01bcd3dd36b3f8e312643`  
		Last Modified: Fri, 24 Oct 2025 18:39:15 GMT  
		Size: 433.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0566b8fe76f76e0ad5ea657194b4d92b42ee40030ce094df05b5dc0e6e84ae45`  
		Last Modified: Fri, 24 Oct 2025 18:39:15 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf58626682170bbf3737c7d904278ec8362b010216ae8a18f86e16ca0d009b7a`  
		Last Modified: Fri, 24 Oct 2025 18:39:16 GMT  
		Size: 13.8 MB (13809061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:923066fc41269ea4091b508de441320561c943cd6e86a64f3c3e6a90784891db`  
		Last Modified: Fri, 24 Oct 2025 18:39:16 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00690a40e9564548ebb8397d4ce85fd59a4d8d6023ac6ae022d8858d4b195327`  
		Last Modified: Fri, 24 Oct 2025 18:39:17 GMT  
		Size: 13.8 MB (13825079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c78eb25cd5e9db7613ca865e4c897be03f67e239803f4a48d4e1a8de7457429a`  
		Last Modified: Fri, 24 Oct 2025 18:39:16 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:945205ba463a893886bd195e931d5d489494f7adfab2ac6a5bfa75067717dc93`  
		Last Modified: Fri, 24 Oct 2025 18:39:16 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8267abc74317460e99d6d1268a3c500c0396e57522cb4d48bbc2c6af0e49207`  
		Last Modified: Fri, 24 Oct 2025 18:39:16 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb70a918bc87745ceb8502edcede40707265faf9389b24ee78c213ca4a1b29ce`  
		Last Modified: Fri, 24 Oct 2025 18:39:15 GMT  
		Size: 888.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:867e28fd798b27d02bfd98368b4e29b4e49ed23352e823512dcffa09d17833ef`  
		Last Modified: Fri, 24 Oct 2025 21:30:28 GMT  
		Size: 1.7 MB (1736382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d98c9a44521d11531abca096d4bb9df6a15cc133384c7d3be8465be9e90838aa`  
		Last Modified: Fri, 24 Oct 2025 21:30:28 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cda2933aef9a10b7d3a9736f5b27f76383829d999ffc31d24e1ecba0ee00a946`  
		Last Modified: Fri, 24 Oct 2025 21:30:28 GMT  
		Size: 253.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e17684c9da0d367c74f2872c80041eca1d0c554a60ed9603f473aa7cc0ba413e`  
		Last Modified: Fri, 24 Oct 2025 21:30:28 GMT  
		Size: 751.5 KB (751479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2a8bc62c4ca36c53e626e179e4c37cb565f54fabaad3a1de13aca103fd10726`  
		Last Modified: Fri, 24 Oct 2025 21:30:28 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d50667c128d76fbf997677e610f4b1e56c0f21c576b1e8c103c34fd5d69f2533`  
		Last Modified: Fri, 24 Oct 2025 21:34:20 GMT  
		Size: 21.7 MB (21737313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-apache` - unknown; unknown

```console
$ docker pull drupal@sha256:8bc566d30c8f7c4c79cca14568527f2b08d952c486ebbea037d5e808370bdd95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7354822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8396deceef0d8f355c3ce28a173d3849c15ef422e2c0effd315467cef8e4f52f`

```dockerfile
```

-	Layers:
	-	`sha256:032fc27311e57b6547d34d4d9efa12c76cf9e97674c900dfb6804ef1604fc9c8`  
		Last Modified: Fri, 24 Oct 2025 22:53:59 GMT  
		Size: 7.3 MB (7307796 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbe5bcdd0e61bebf2b63d632b7817f7d09b5a61df7c916e0897525c195a9aa5c`  
		Last Modified: Fri, 24 Oct 2025 22:54:00 GMT  
		Size: 47.0 KB (47026 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-apache` - linux; ppc64le

```console
$ docker pull drupal@sha256:a3b80bd7d776ea018a3af7dca0853144c8e8ca18d9d973c4d579bc80b6ccac18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.2 MB (200170837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bfcf6661ebdb8240d45f7a0fa8da93354bfd97cd667e405a5ef6fe5f423e6e1`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 02 Oct 2025 09:27:16 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1760918400'
# Thu, 02 Oct 2025 09:27:16 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 02 Oct 2025 09:27:16 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 02 Oct 2025 09:27:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 02 Oct 2025 09:27:16 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 02 Oct 2025 09:27:16 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 02 Oct 2025 09:27:16 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 02 Oct 2025 09:27:16 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 02 Oct 2025 09:27:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 02 Oct 2025 09:27:16 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 02 Oct 2025 09:27:16 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 02 Oct 2025 09:27:16 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 02 Oct 2025 09:27:16 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 02 Oct 2025 09:27:16 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 02 Oct 2025 09:27:16 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 02 Oct 2025 09:27:16 GMT
ENV PHP_VERSION=8.4.14
# Thu, 02 Oct 2025 09:27:16 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.14.tar.xz.asc
# Thu, 02 Oct 2025 09:27:16 GMT
ENV PHP_SHA256=bac90ee7cf738e814c89b6b27d4d2c4b70e50942a420837e1a22f5fd5f9867a3
# Thu, 02 Oct 2025 09:27:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 02 Oct 2025 09:27:16 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 02 Oct 2025 09:27:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 02 Oct 2025 09:27:16 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 02 Oct 2025 09:27:16 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 02 Oct 2025 09:27:16 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 02 Oct 2025 09:27:16 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 02 Oct 2025 09:27:16 GMT
STOPSIGNAL SIGWINCH
# Thu, 02 Oct 2025 09:27:16 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 02 Oct 2025 09:27:16 GMT
WORKDIR /var/www/html
# Thu, 02 Oct 2025 09:27:16 GMT
EXPOSE map[80/tcp:{}]
# Thu, 02 Oct 2025 09:27:16 GMT
CMD ["apache2-foreground"]
# Thu, 02 Oct 2025 09:27:16 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Oct 2025 09:27:16 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 02 Oct 2025 09:27:16 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Thu, 02 Oct 2025 09:27:16 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 02 Oct 2025 09:27:16 GMT
ENV DRUPAL_VERSION=10.5.4
# Thu, 02 Oct 2025 09:27:16 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 02 Oct 2025 09:27:16 GMT
WORKDIR /opt/drupal
# Thu, 02 Oct 2025 09:27:16 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 02 Oct 2025 09:27:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:a9b4dd19a96be85b367998327f4288ed2fa8f174d1b3e8bea8ac7c2c626ec865`  
		Last Modified: Tue, 21 Oct 2025 00:26:55 GMT  
		Size: 33.6 MB (33598518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d9930d173c844c53a7c234fc6795612dd8a9cd3fa137cebec8570aa820f7779`  
		Last Modified: Tue, 21 Oct 2025 02:18:16 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf07ac4257b79ada16559cfa4a31502b1c711128c5199e235de1363c9bcbd2bf`  
		Last Modified: Tue, 21 Oct 2025 02:18:23 GMT  
		Size: 109.6 MB (109597844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87cff8614d84588c83a0d2abe18d46fc6b68b149ff9548d76e95cacef7b67548`  
		Last Modified: Tue, 21 Oct 2025 02:18:17 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e3b57091f64452a0212e5e000a540e2f99ab05044e9f77a7c1aafc3a6b50ced`  
		Last Modified: Tue, 21 Oct 2025 02:24:58 GMT  
		Size: 4.9 MB (4875614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a745ed36448e107212d5f0bd2b9d85fd1c3429bba4f2db389c88315b0a8477d`  
		Last Modified: Tue, 21 Oct 2025 02:24:57 GMT  
		Size: 432.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1961beeb598adff8031449d8db4712825f740775002d017dd0710f99317eecc3`  
		Last Modified: Tue, 21 Oct 2025 02:24:57 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28081fafaabc852070791844441e680ac581d5c3f0a52411b145977e82506215`  
		Last Modified: Fri, 24 Oct 2025 20:35:24 GMT  
		Size: 13.8 MB (13824751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4747b89a43d13b8e4dee4a763b69436df11619c71daf206f3d840bcbf332a7f`  
		Last Modified: Fri, 24 Oct 2025 20:35:22 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5499e1591ce30fc96df2772eb7d1b36117ea0c0c91567103622db0ebf4b1d3a`  
		Last Modified: Fri, 24 Oct 2025 20:35:25 GMT  
		Size: 13.9 MB (13932648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66e37aef13f1d76ed90c506f55f4c74a384113813332fee4481c4a186a5f5444`  
		Last Modified: Fri, 24 Oct 2025 20:35:22 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55c250cef41f07a8e5e894700bf1e14476201457f15d2bd841d6388ea6420a53`  
		Last Modified: Fri, 24 Oct 2025 20:35:22 GMT  
		Size: 253.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b51a9ddd654aacf5f9a6881d1e8a7ef48ade30c5687de4c900ab027b4eceb91`  
		Last Modified: Fri, 24 Oct 2025 20:35:23 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:547dcfd04bfc5b6ad00133748fb308a2e47b97642a939405c927ee37112a87e6`  
		Last Modified: Fri, 24 Oct 2025 20:35:22 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a8c2f146cf884889f157a55be885001a4d3e82a047b2b8131336a586ce34bda`  
		Last Modified: Sat, 25 Oct 2025 06:12:41 GMT  
		Size: 1.8 MB (1845759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38668d19399e7b3019bacd34269bbf84a8b808fc9466bc0d552204490727852f`  
		Last Modified: Sat, 25 Oct 2025 06:12:41 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a1c365fdedab27d4b8401f043e49cc5ffeb843a281ad786c5a6cb5cb2f27aea`  
		Last Modified: Sat, 25 Oct 2025 06:12:41 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edf715a57cad79329f6972e0a8273cb7a1f9a7d5b660531d258ca533b37bff63`  
		Last Modified: Sat, 25 Oct 2025 06:12:41 GMT  
		Size: 751.5 KB (751479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0c3be2276b509297ab4c79c282d82709d299fc01aeb155c008dbb2db937d188`  
		Last Modified: Sat, 25 Oct 2025 06:12:41 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3af0d10b22d460118109d1e708f1d03914f72e6ab4a4d97f7261437f70981bbd`  
		Last Modified: Sat, 25 Oct 2025 06:56:22 GMT  
		Size: 21.7 MB (21737787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-apache` - unknown; unknown

```console
$ docker pull drupal@sha256:6220c0877d7bc076ee2c6149201a88be06048bb2b6e81890e1bda1c561256bfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7381208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb6040322fb9bd29cafdbbf543f80271819e7935f239dd05d07fda99abf9796c`

```dockerfile
```

-	Layers:
	-	`sha256:99a3d5a774a3c4eed1e60d613e89295db9d8824b60b3f487a87e7769204eb2d9`  
		Last Modified: Sat, 25 Oct 2025 07:53:44 GMT  
		Size: 7.3 MB (7333923 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d674144385f9d066563792ef1040501b331ca62b4431e19544ab502946cbaec6`  
		Last Modified: Sat, 25 Oct 2025 07:53:45 GMT  
		Size: 47.3 KB (47285 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-apache` - linux; riscv64

```console
$ docker pull drupal@sha256:c51a99deaddc176146bec2cfa597f7d71f25ba8e76b3aa6c54f01d41f805384c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.7 MB (229740496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:005936fe96c17c56c2c65c47f7db6953f4c50486a0364a6cf3a6d11d4269d123`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1760918400'
# Thu, 23 Oct 2025 18:46:40 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 23 Oct 2025 18:46:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 23 Oct 2025 18:46:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 23 Oct 2025 18:46:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 23 Oct 2025 18:46:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 23 Oct 2025 18:46:40 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 23 Oct 2025 18:46:40 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 23 Oct 2025 18:46:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 23 Oct 2025 18:46:40 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 23 Oct 2025 18:46:40 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 23 Oct 2025 18:46:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 23 Oct 2025 18:46:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 23 Oct 2025 18:46:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 23 Oct 2025 18:46:40 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 23 Oct 2025 18:46:40 GMT
ENV PHP_VERSION=8.4.14
# Thu, 23 Oct 2025 18:46:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.14.tar.xz.asc
# Thu, 23 Oct 2025 18:46:40 GMT
ENV PHP_SHA256=bac90ee7cf738e814c89b6b27d4d2c4b70e50942a420837e1a22f5fd5f9867a3
# Thu, 23 Oct 2025 18:46:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 23 Oct 2025 18:46:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 23 Oct 2025 18:46:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 23 Oct 2025 18:46:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 23 Oct 2025 18:46:40 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 23 Oct 2025 18:46:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 23 Oct 2025 18:46:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 23 Oct 2025 18:46:40 GMT
STOPSIGNAL SIGWINCH
# Thu, 23 Oct 2025 18:46:40 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 23 Oct 2025 18:46:40 GMT
WORKDIR /var/www/html
# Thu, 23 Oct 2025 18:46:40 GMT
EXPOSE map[80/tcp:{}]
# Thu, 23 Oct 2025 18:46:40 GMT
CMD ["apache2-foreground"]
# Wed, 29 Oct 2025 16:21:23 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 29 Oct 2025 16:21:23 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 29 Oct 2025 16:21:24 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Wed, 29 Oct 2025 16:21:24 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 29 Oct 2025 16:21:24 GMT
ENV DRUPAL_VERSION=10.5.4
# Wed, 29 Oct 2025 16:21:24 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 29 Oct 2025 16:21:24 GMT
WORKDIR /opt/drupal
# Wed, 29 Oct 2025 21:10:25 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 29 Oct 2025 21:10:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:6d1567708d42906165204f9177d357cb6a2fd51f758da447f1743b00813f892f`  
		Last Modified: Tue, 21 Oct 2025 00:37:37 GMT  
		Size: 28.3 MB (28275650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a10e23c0c73cc8f0a9cca6c3668230538af936622d758ae4720124e65d1901fb`  
		Last Modified: Tue, 21 Oct 2025 07:00:41 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a425a73dbb9980b18297b2dd5ae6470d5dd6bff4029928b3c47109bbcfc0163`  
		Last Modified: Tue, 21 Oct 2025 17:30:53 GMT  
		Size: 146.6 MB (146579498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0199b9324986716555eaee60a4139b64762a2ce7dc60435723ca0d60bbdcc8e7`  
		Last Modified: Tue, 21 Oct 2025 07:00:41 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e411973bcee0512dfec874e20878187e9ca3d61e5e85f50bb8f0f0a7c12003b7`  
		Last Modified: Tue, 21 Oct 2025 07:00:42 GMT  
		Size: 4.0 MB (4026071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f0db7f60aa00b9271b9f20a450a46ec36bd24e8cb67c827c82321a67378125a`  
		Last Modified: Tue, 21 Oct 2025 07:00:41 GMT  
		Size: 442.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aa6de92184bcc00f479d98e26a3d28b90d3c4dde823cbaff7b0da1c8aaa9a4d`  
		Last Modified: Tue, 21 Oct 2025 07:00:41 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:275f9a433c43be52198e41839a3cba754c0134d95685661ea7c7f0b6407f647e`  
		Last Modified: Sat, 25 Oct 2025 17:07:01 GMT  
		Size: 13.8 MB (13824812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3596ddc9422cfc83354ed2c55a4c5297a3c31219fd97ec3d865e64bef880424e`  
		Last Modified: Sat, 25 Oct 2025 17:07:00 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:996d1a0d48e17285f34ae307aceb5e7071959eeb7a01b4712efb85e9ada91f81`  
		Last Modified: Sat, 25 Oct 2025 17:07:00 GMT  
		Size: 13.0 MB (12965669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af1cd396e7428e6b5febc446e44cc101e617e26a7e63ba1891e5a6139f993dd0`  
		Last Modified: Sat, 25 Oct 2025 17:07:00 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a0b486608418c8ddb955870f0f1ab5a38f3fb4e37d8bb0fbaea71e02703d096`  
		Last Modified: Sat, 25 Oct 2025 17:07:00 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:212465ae3864e221ad220072d44dc5fabed1a010441e01623fb310effba1d95c`  
		Last Modified: Sat, 25 Oct 2025 17:07:00 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efc64a64def28d9b139987afbe5aaf92782b75d8b07be559be9eddd0f96778dd`  
		Last Modified: Sat, 25 Oct 2025 17:07:00 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df9e9bb72a118e571908940e529b92c3b1c097e93a8d0691f47a4134cc94190d`  
		Last Modified: Wed, 29 Oct 2025 16:27:00 GMT  
		Size: 1.6 MB (1572758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b81d6a31e9fd63f83041cb601bbf04887fb8c56ce54e73a355d74ca07a9159`  
		Last Modified: Wed, 29 Oct 2025 16:26:59 GMT  
		Size: 319.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d671fe3123bdf0fa89ad9438faf764bcc9db5384642873e28ba5ba2129ea8244`  
		Last Modified: Wed, 29 Oct 2025 16:26:59 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fb40d873e147d3028147792c10e998b3e218f057c2166cda25d9eb3cc9eef13`  
		Last Modified: Wed, 29 Oct 2025 16:26:59 GMT  
		Size: 751.5 KB (751479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9918121bf0ea5ce7d8ad1d9d13641699183b7a185ba0a9559c826064735cbf86`  
		Last Modified: Wed, 29 Oct 2025 16:26:59 GMT  
		Size: 112.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0d7e5d6a92ef15b8dddf02acfb3ab4dd0b88474090252cf2ad3ea900f222b97`  
		Last Modified: Wed, 29 Oct 2025 21:15:21 GMT  
		Size: 21.7 MB (21738108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-apache` - unknown; unknown

```console
$ docker pull drupal@sha256:21407f325041c14fd31bde66984d69fe1e8c5e1178913e5d4adbd98f6889d3d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7453162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fa647cf0afef334ba7e048eb10406064fc2e6b8e40e28c0a5c577bd6bb1611e`

```dockerfile
```

-	Layers:
	-	`sha256:e6fafed83a14f7285548a93d51783da8d30d9d30d0af28346c80650fa0de2ee0`  
		Last Modified: Wed, 29 Oct 2025 22:53:42 GMT  
		Size: 7.4 MB (7405920 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7541d274841351f058c3c8d1be0ea8fc8f5d52884f8bbf8b6f43884621629808`  
		Last Modified: Wed, 29 Oct 2025 22:53:43 GMT  
		Size: 47.2 KB (47242 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-apache` - linux; s390x

```console
$ docker pull drupal@sha256:5664ceb3002ced8712670e80f08a35447bd1f5c69b304cd892f1042d1ebb2f71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.0 MB (178019951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e843d877ef99e8380aa8367d3d28783f63ad88c36e544250c3ae7be6c30fc1b`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 02 Oct 2025 09:27:16 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1760918400'
# Thu, 02 Oct 2025 09:27:16 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 02 Oct 2025 09:27:16 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 02 Oct 2025 09:27:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 02 Oct 2025 09:27:16 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 02 Oct 2025 09:27:16 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 02 Oct 2025 09:27:16 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 02 Oct 2025 09:27:16 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 02 Oct 2025 09:27:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 02 Oct 2025 09:27:16 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 02 Oct 2025 09:27:16 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 02 Oct 2025 09:27:16 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 02 Oct 2025 09:27:16 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 02 Oct 2025 09:27:16 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 02 Oct 2025 09:27:16 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 02 Oct 2025 09:27:16 GMT
ENV PHP_VERSION=8.4.14
# Thu, 02 Oct 2025 09:27:16 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.14.tar.xz.asc
# Thu, 02 Oct 2025 09:27:16 GMT
ENV PHP_SHA256=bac90ee7cf738e814c89b6b27d4d2c4b70e50942a420837e1a22f5fd5f9867a3
# Thu, 02 Oct 2025 09:27:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 02 Oct 2025 09:27:16 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 02 Oct 2025 09:27:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 02 Oct 2025 09:27:16 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 02 Oct 2025 09:27:16 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 02 Oct 2025 09:27:16 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 02 Oct 2025 09:27:16 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 02 Oct 2025 09:27:16 GMT
STOPSIGNAL SIGWINCH
# Thu, 02 Oct 2025 09:27:16 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 02 Oct 2025 09:27:16 GMT
WORKDIR /var/www/html
# Thu, 02 Oct 2025 09:27:16 GMT
EXPOSE map[80/tcp:{}]
# Thu, 02 Oct 2025 09:27:16 GMT
CMD ["apache2-foreground"]
# Thu, 02 Oct 2025 09:27:16 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Oct 2025 09:27:16 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 02 Oct 2025 09:27:16 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Thu, 02 Oct 2025 09:27:16 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 02 Oct 2025 09:27:16 GMT
ENV DRUPAL_VERSION=10.5.4
# Thu, 02 Oct 2025 09:27:16 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 02 Oct 2025 09:27:16 GMT
WORKDIR /opt/drupal
# Thu, 02 Oct 2025 09:27:16 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 02 Oct 2025 09:27:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:71dc03f1fd788f9fc2bbb931d3df17cbfaf0b486bdfb19f4e3b8792a206689a1`  
		Last Modified: Tue, 21 Oct 2025 00:28:26 GMT  
		Size: 29.8 MB (29837255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e6c3f4ad4e24c29ede95cbb6fb2aa2828df1b20348eed91dade18765579bc19`  
		Last Modified: Tue, 21 Oct 2025 02:12:15 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b339ad9eb2dd636ee49d09322a8cc6b6ddb681a1c9115d8fdbd520598d3213bc`  
		Last Modified: Tue, 21 Oct 2025 02:12:21 GMT  
		Size: 92.6 MB (92564172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40db4669097adb199a40f97fcd445c22549de3dc01b5d9f3374183cb691b12ad`  
		Last Modified: Tue, 21 Oct 2025 02:12:15 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:907f4a0500d579438accce58638a04dd4ce07e5fd76008160639e6e34df06f9d`  
		Last Modified: Tue, 21 Oct 2025 02:20:17 GMT  
		Size: 4.3 MB (4320657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf69137470e52fde51a7921b5cad39856680b25b85c2a0174a0462a47a3c5fe`  
		Last Modified: Tue, 21 Oct 2025 02:20:16 GMT  
		Size: 435.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc8e1e01f85b458d5bf985e40c30fd371f8a678ab94adb3c979e5789fac20a33`  
		Last Modified: Tue, 21 Oct 2025 02:20:17 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a2c9cc41639b9d2f6fb4f7c40602934c959f15b43592beabc2b93e5152fb735`  
		Last Modified: Fri, 24 Oct 2025 19:36:51 GMT  
		Size: 13.8 MB (13824190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef336888dc61ad6acab53f28e5bcd0f45e014a496ed637aa0fa27e516d47637`  
		Last Modified: Fri, 24 Oct 2025 19:36:49 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3936512bbc87a42b560d878b72e3968b3e576bd2b768653ea515cabfe4530e5`  
		Last Modified: Fri, 24 Oct 2025 19:36:51 GMT  
		Size: 13.3 MB (13301926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8204e8f2af2c96deca1625e0973606411e9dca49b77e42898f5813d1ef2b3264`  
		Last Modified: Fri, 24 Oct 2025 19:36:50 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54e744bc48e9e6eeb0a70ffdc224530eb34631654635c71018df2d207ef2b354`  
		Last Modified: Fri, 24 Oct 2025 19:36:50 GMT  
		Size: 253.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfeccf8b77f02b853189f3cbb143a67eb246a950b7f4047ed3667a381cab8687`  
		Last Modified: Fri, 24 Oct 2025 19:36:50 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e654fc5cf9fdf2ec03361d5d0f43fb7eb0665ff8dfc18d9d0bffacdc4fa9733`  
		Last Modified: Fri, 24 Oct 2025 19:36:50 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd49cd268b7e1c3fb23bc57b8004ec388b60b56d3f61286754ae5d5b9322878a`  
		Last Modified: Sat, 25 Oct 2025 04:22:17 GMT  
		Size: 1.7 MB (1675293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b6029a1f44c68d9582454730860ff5c885dbdd177bc84cc6fe549857d80e5dc`  
		Last Modified: Sat, 25 Oct 2025 04:22:17 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89e87b96274ed6536cf3e4c49d0084a11a1e532bc42775246e11dfea199ad071`  
		Last Modified: Sat, 25 Oct 2025 04:22:17 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:498b581627e8569983ceef48f860125291606d6071fdb7b4021f354461e55b40`  
		Last Modified: Sat, 25 Oct 2025 04:22:17 GMT  
		Size: 751.5 KB (751479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:180a550cfedda3b8103aa18c95591f766169346ffedb9243ec20fb93d4dad67e`  
		Last Modified: Sat, 25 Oct 2025 04:22:17 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:123b0e0c5470ab9008389b70aab1d985d6c8fa670ec4221d446c9f86010749f3`  
		Last Modified: Sat, 25 Oct 2025 04:52:25 GMT  
		Size: 21.7 MB (21738553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-apache` - unknown; unknown

```console
$ docker pull drupal@sha256:a142e8fedc1773ef3cf9fcff89f92aa56dbf5c5bdfd767b2672d0bd17be04101
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7198398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52da5fe082681003683389514950b827e22a5d0319d0f8a0a6d2bd3a780c759b`

```dockerfile
```

-	Layers:
	-	`sha256:f5f52bdbd1846e4b7c92d7b8df097515f626ac47e213706f96415d40dcedba4e`  
		Last Modified: Sat, 25 Oct 2025 07:53:55 GMT  
		Size: 7.2 MB (7151264 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5722aed2a7b6112dd1ce5e7a7fac27ca09c7defcf6a556fcdad9e61f22b1122b`  
		Last Modified: Sat, 25 Oct 2025 07:53:56 GMT  
		Size: 47.1 KB (47134 bytes)  
		MIME: application/vnd.in-toto+json
