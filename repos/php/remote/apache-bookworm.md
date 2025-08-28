## `php:apache-bookworm`

```console
$ docker pull php@sha256:acbf9f87512c2e033e580cf23ec11ff5967151a022eac9b8c7318b1bd0798041
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

### `php:apache-bookworm` - linux; amd64

```console
$ docker pull php@sha256:b248c41e98131542c49f2e55f0eee183a89df6de5a91cb27955227cd7d7a6e73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.6 MB (180642959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bc7fb1e8afb84bf6f7be0031fff6b0550cd816a77a6aa8debef11d621e3428f`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 28 Aug 2025 12:46:41 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 28 Aug 2025 12:46:41 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_VERSION=8.4.12
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.12.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.12.tar.xz.asc
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_SHA256=c1b7978cbb5054eed6c749bde4444afc16a3f2268101fb70a7d5d9b1083b12ad
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 28 Aug 2025 12:46:41 GMT
STOPSIGNAL SIGWINCH
# Thu, 28 Aug 2025 12:46:41 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
WORKDIR /var/www/html
# Thu, 28 Aug 2025 12:46:41 GMT
EXPOSE map[80/tcp:{}]
# Thu, 28 Aug 2025 12:46:41 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:b1badc6e50664185acfaa0ca255d8076061c2a9d881cecaaad281ae11af000ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:36 GMT  
		Size: 28.2 MB (28230255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:388e5b6f8a5795f0e4fe593b657834e0a6e1516d000a10057262df63d9047f62`  
		Last Modified: Thu, 28 Aug 2025 19:08:24 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0cb9bba9f53a82a6c8b1fd3eeeb5d51f0fb0b1ce46af5ca15243a617caa186e`  
		Last Modified: Thu, 28 Aug 2025 19:08:59 GMT  
		Size: 104.3 MB (104333552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41ac8c51227919b786d26ec323336bdb8533deb156d8200efc56e730520e97a6`  
		Last Modified: Thu, 28 Aug 2025 19:08:28 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb45a6694822acba2fcc6e0dfc42e6e9855dc2c57ecd44b1655c5c54d9fdc4ac`  
		Last Modified: Thu, 28 Aug 2025 19:08:45 GMT  
		Size: 20.1 MB (20124069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ebe5a39abc1dc5f32946e312eb7f61adedbd9f1c0f01ddf0790ed1c25682d7`  
		Last Modified: Thu, 28 Aug 2025 19:08:24 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3dda47bb85a49496627309019cd0701f74cbeadae2d4a77f1cd16f1a712f2be`  
		Last Modified: Thu, 28 Aug 2025 19:08:25 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:327ff8612aba4906a7a63c485214692391547e4be339b7c3fb8392c3fbce493b`  
		Last Modified: Thu, 28 Aug 2025 19:08:43 GMT  
		Size: 13.8 MB (13765382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56a684016732d2505f99ef2f264ef90524f2da2e08c5bb4b86e470038eee313d`  
		Last Modified: Thu, 28 Aug 2025 19:08:25 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f10f63fbdf6f6025b77ed54add207cae57e66b772c90755a1d77c56871399a1c`  
		Last Modified: Thu, 28 Aug 2025 19:08:43 GMT  
		Size: 14.2 MB (14183964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68faeaa850b06a63b929521c12ca78b38cf481c7cae1401cda8718b97aca80b2`  
		Last Modified: Thu, 28 Aug 2025 19:08:24 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdd85968e348cb051427c3f6ddbbe86fa183148e6c57c7f84cd775195739a9d9`  
		Last Modified: Thu, 28 Aug 2025 19:08:25 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad04f4fa22064cb41f3951a3333c328eb3c7322e6d38631e6f4bb57fbfe4a0f`  
		Last Modified: Thu, 28 Aug 2025 19:08:27 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f39a3a14f38a8dea5401ba432f644d45a141ee553c57d633e1e5f3aff7a91a2e`  
		Last Modified: Thu, 28 Aug 2025 19:08:24 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:apache-bookworm` - unknown; unknown

```console
$ docker pull php@sha256:480540c7e9417ecdab5f63b9b975c74e77e0803d0e5a83b2d651f80f7966073f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6992949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0037a1da04316b745fa2949b113303069c750db7850d732ee68906ab1cc21983`

```dockerfile
```

-	Layers:
	-	`sha256:f9d9c36319f142a4c96d2c94bb49715608b8de912a0a51ada44fbcc38d1b6bc9`  
		Last Modified: Thu, 28 Aug 2025 19:56:26 GMT  
		Size: 6.9 MB (6930735 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22b1d9c8bb76458af17d890e0ba28a1890ab0bcb69ab8a2d61e0775f9d9fdc10`  
		Last Modified: Thu, 28 Aug 2025 19:56:27 GMT  
		Size: 62.2 KB (62214 bytes)  
		MIME: application/vnd.in-toto+json

### `php:apache-bookworm` - linux; arm variant v5

```console
$ docker pull php@sha256:ec2b69dff27f5ba934ada7bfde38a9108a3e1b7dd5bed6f260ec00e61f181776
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.9 MB (153853703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0de70cd0a4a1ae7fdff5eb2d997672c96643c03fdc8f481748d5ff555f405c4e`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1754870400'
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 28 Aug 2025 12:46:41 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 28 Aug 2025 12:46:41 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_VERSION=8.4.12
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.12.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.12.tar.xz.asc
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_SHA256=c1b7978cbb5054eed6c749bde4444afc16a3f2268101fb70a7d5d9b1083b12ad
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 28 Aug 2025 12:46:41 GMT
STOPSIGNAL SIGWINCH
# Thu, 28 Aug 2025 12:46:41 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
WORKDIR /var/www/html
# Thu, 28 Aug 2025 12:46:41 GMT
EXPOSE map[80/tcp:{}]
# Thu, 28 Aug 2025 12:46:41 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:53f325cb4b149fb7bd7e6ed7f8dfc1c5a37b5d828d75b4e6ba65a5cfd25aec56`  
		Last Modified: Tue, 12 Aug 2025 20:45:02 GMT  
		Size: 25.8 MB (25762718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f45607c9703b1623eae4308abc7d9dfac71b6d221b1313958be26dddd31bcd63`  
		Last Modified: Tue, 12 Aug 2025 22:03:30 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f6033c41c6a5cbd10e29711e09c8a94365510a58d88626385f53831b1bd04d5`  
		Last Modified: Tue, 12 Aug 2025 22:03:37 GMT  
		Size: 82.0 MB (81978153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de9e1469fd07000afb3b39a4178a2fa8409d180132e96dee6bffda0a65279f9e`  
		Last Modified: Tue, 12 Aug 2025 22:03:32 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abaa20572a4a3785129b37e835ffaf475213f1a14d056a625ef543e9ac026960`  
		Last Modified: Wed, 13 Aug 2025 06:13:16 GMT  
		Size: 19.4 MB (19418252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c437b13f40151972e7ef755276c4d92b4986a2d5412153e5db35eabff273e0d`  
		Last Modified: Tue, 12 Aug 2025 22:42:41 GMT  
		Size: 434.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04d698f1834ea5af3d28ed5a04bf6880643854221994f6fe45b0aa34c92258e2`  
		Last Modified: Tue, 12 Aug 2025 22:42:41 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef1add1ff207d0fd0ea69560722bc09987e8d21942185d38a9552dc6b96bb8f7`  
		Last Modified: Thu, 28 Aug 2025 18:53:40 GMT  
		Size: 13.8 MB (13763633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b116d2627ea0c9f8cfbec46ce74970df8634891781dcb7a3cad2da720c99524c`  
		Last Modified: Thu, 28 Aug 2025 18:53:39 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:169232c3758cd4a9143f148ca321f05e7de257fb9caeb87dbacbae09dcfa4724`  
		Last Modified: Thu, 28 Aug 2025 18:53:48 GMT  
		Size: 12.9 MB (12925199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d0f802b7dd4188a98c352f51ff19bcdd666f6c3bb47a49aba9277851977fbd`  
		Last Modified: Thu, 28 Aug 2025 18:53:40 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbffe96de19b1f7224f144c07d8151835e1277e257e6ab63e928c1acfcf11e82`  
		Last Modified: Thu, 28 Aug 2025 18:53:40 GMT  
		Size: 254.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d5ff4ed4fdcf4e4f7ec6e267b9b97700c7a185a9f69205479db0b6e8ecc1332`  
		Last Modified: Thu, 28 Aug 2025 18:53:40 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc7f9e7c983802a88558e793af2716123f09ade1941dcadd15944bc044e88066`  
		Last Modified: Thu, 28 Aug 2025 18:53:40 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:apache-bookworm` - unknown; unknown

```console
$ docker pull php@sha256:cc0fef78709ec2081e16b73b524fdede01681eed0f48abf7b84671ffa30725b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6802469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4752cf8d5c1f99799ef2874466ea045616a276c39bc98d60502f7a50b57373d1`

```dockerfile
```

-	Layers:
	-	`sha256:8e8e62c7c56a1c4795103e4457bcbc9344542b247d6896787e74bfcc5d4cc6f6`  
		Last Modified: Thu, 28 Aug 2025 19:56:33 GMT  
		Size: 6.7 MB (6740077 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:417361a7c1381aced624a7fe164b63ef938600f28e9aaca17ce1341a9a7c8714`  
		Last Modified: Thu, 28 Aug 2025 19:56:34 GMT  
		Size: 62.4 KB (62392 bytes)  
		MIME: application/vnd.in-toto+json

### `php:apache-bookworm` - linux; arm variant v7

```console
$ docker pull php@sha256:bd733e870c3e42ca29f90fb3dbf26722b54abe59abc21c2f9c5a8f61ff20346c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.0 MB (145004489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b2363c1ff6a63500e62dcb1fe724fac417c62141b59c3775c6fb2f8a0698fda`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1754870400'
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 28 Aug 2025 12:46:41 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 28 Aug 2025 12:46:41 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_VERSION=8.4.12
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.12.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.12.tar.xz.asc
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_SHA256=c1b7978cbb5054eed6c749bde4444afc16a3f2268101fb70a7d5d9b1083b12ad
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 28 Aug 2025 12:46:41 GMT
STOPSIGNAL SIGWINCH
# Thu, 28 Aug 2025 12:46:41 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
WORKDIR /var/www/html
# Thu, 28 Aug 2025 12:46:41 GMT
EXPOSE map[80/tcp:{}]
# Thu, 28 Aug 2025 12:46:41 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:a8db185805c54c045d888f7030794ebee970355b2336287cac0a0e22638ffc98`  
		Last Modified: Tue, 12 Aug 2025 20:46:38 GMT  
		Size: 23.9 MB (23938929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e03dd152e133ed3c4f7b6111971ebb032fa5347cab0e4ed3c3923003220f8ec4`  
		Last Modified: Tue, 12 Aug 2025 22:02:44 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d48d5562d819ed1d81511a866ab9cfa69e1c7f0351806797ebf63ebbb4bacc7c`  
		Last Modified: Tue, 12 Aug 2025 22:02:48 GMT  
		Size: 76.2 MB (76153041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c4000aa6f8df46ea73922bba283db07ef24d97efded72dc7d1e798c0d32e96`  
		Last Modified: Tue, 12 Aug 2025 22:02:45 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98d5a646260be9143e0a73e8a380305b7011867058eac866e2fc96be1e40357d`  
		Last Modified: Tue, 12 Aug 2025 22:07:13 GMT  
		Size: 18.9 MB (18855896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ec17d86983395657a14311f5bf8bb526dbcb02f4115a5efc0da9ecdd785b147`  
		Last Modified: Tue, 12 Aug 2025 22:07:09 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63aecbcda44b653e76bd7ff8168d1492421826ef90d182709984b36f3b556695`  
		Last Modified: Tue, 12 Aug 2025 22:07:08 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f0f5506c371cf2cf295429b1b4a7952995ef31ee8cc65e9c4aa699422e2bab3`  
		Last Modified: Thu, 28 Aug 2025 18:47:44 GMT  
		Size: 13.8 MB (13763619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e98b56da7d9fb6f638bfac13d75e19e87988b1845c1e292509911d0dbc5f504`  
		Last Modified: Thu, 28 Aug 2025 18:47:41 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:524f84d8e94050e09bcf671df5d17bf8c86c6b9c1ea3977e39b0040599cc3f03`  
		Last Modified: Thu, 28 Aug 2025 18:47:42 GMT  
		Size: 12.3 MB (12287276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae82115bcf0292b1bfd37fd9b5c2a28fa367dd11c1b78c0c7ac57004c5f3c326`  
		Last Modified: Thu, 28 Aug 2025 18:47:41 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c39321ffc034069862747df4de406c4b48cb35b91680c806b25cb1dfbe2c3bd4`  
		Last Modified: Thu, 28 Aug 2025 18:47:41 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c114d93443cf7175fd1d3a0be1a5944f19a71656da7c66eb87faedd9f5299b8`  
		Last Modified: Thu, 28 Aug 2025 18:47:41 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5750659720b398b43c31d6cbad49bd48a1766bc7a3af0799eebd733772f5facd`  
		Last Modified: Thu, 28 Aug 2025 18:47:41 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:apache-bookworm` - unknown; unknown

```console
$ docker pull php@sha256:299f30e4ca743fe3622f8edfa0ca2313d512da405acf1e43f2e644eb42e0dd06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6806447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a7ea52b9d02e443a74086a7ef8be92c4f7773832f0b8f3f8b876fc81c2ad509`

```dockerfile
```

-	Layers:
	-	`sha256:41836b9aca0e071eef7ffbca71e05c545d9bb71db0f846af6e9e602f2370fa6d`  
		Last Modified: Thu, 28 Aug 2025 19:56:40 GMT  
		Size: 6.7 MB (6744053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a93ac40de3b5166803cb2a9b65c22fcb210b52e917e5255102ebc92605b94d32`  
		Last Modified: Thu, 28 Aug 2025 19:56:41 GMT  
		Size: 62.4 KB (62394 bytes)  
		MIME: application/vnd.in-toto+json

### `php:apache-bookworm` - linux; arm64 variant v8

```console
$ docker pull php@sha256:095b0d83413982b6d5f1731554761e52acdef8594b645453f3e5ac6370ab6468
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.0 MB (173957712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7637465e7440debd3133638b8271f248ea0a70e4eee459ad266b92441f1010a5`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 28 Aug 2025 12:46:41 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 28 Aug 2025 12:46:41 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_VERSION=8.4.12
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.12.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.12.tar.xz.asc
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_SHA256=c1b7978cbb5054eed6c749bde4444afc16a3f2268101fb70a7d5d9b1083b12ad
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 28 Aug 2025 12:46:41 GMT
STOPSIGNAL SIGWINCH
# Thu, 28 Aug 2025 12:46:41 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
WORKDIR /var/www/html
# Thu, 28 Aug 2025 12:46:41 GMT
EXPOSE map[80/tcp:{}]
# Thu, 28 Aug 2025 12:46:41 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:9a80f9a055240e1d5ffd4b99717e18b5b3e924369b9155fb0a951a7a94b2c61f`  
		Last Modified: Tue, 12 Aug 2025 22:08:02 GMT  
		Size: 28.1 MB (28082001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b96957a20ccc9937d8c2de3a0bdbfd9e266ce8be1d80d327e05508033a6e2eaa`  
		Last Modified: Thu, 14 Aug 2025 22:36:25 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ed545b0873833b283f4e2e059b58204796f019f24b80953f49534e1df7ada7f`  
		Last Modified: Thu, 14 Aug 2025 22:36:39 GMT  
		Size: 98.2 MB (98153300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5565c1b3abdfc1ec1eb4818fac70995e2fabbe18fb754d0c6c89faacc4cf863b`  
		Last Modified: Thu, 14 Aug 2025 22:36:26 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:627036792252d06368fbde62cf9faba553f560176f9e67df708c65ca5208c54a`  
		Last Modified: Thu, 14 Aug 2025 22:40:31 GMT  
		Size: 20.1 MB (20136118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2ce5503a825e29dc8693a75eaf606a04a9f32c6127fb30b3a5c538237fdd353`  
		Last Modified: Thu, 14 Aug 2025 22:40:30 GMT  
		Size: 436.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72d9ee89df80d9edc3207619f30c512deca7475ec0d8b9e7a63a9f67ce55d7b4`  
		Last Modified: Thu, 14 Aug 2025 22:40:30 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84d9fad2515a13af77ee79855d6f4cf636cad317e5f6fac138fa9b7ec5975048`  
		Last Modified: Thu, 28 Aug 2025 18:34:50 GMT  
		Size: 13.8 MB (13765265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336ed651bf9137e50c7036c6ac708952d72a4f91cd7793c19600e90668c0991b`  
		Last Modified: Thu, 28 Aug 2025 18:34:49 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8bffb4ad4d7ff2fa10dca7bc56feeaf6e35b4ea45bb4f55e9f0060f06808dd0`  
		Last Modified: Thu, 28 Aug 2025 18:34:52 GMT  
		Size: 13.8 MB (13815273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2431cdd79a14f91777d15c95bca924636fc835f7deff8c0bd9da7f1b417bb1c4`  
		Last Modified: Thu, 28 Aug 2025 18:34:49 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e42bfddabaa9fa594ead0b12d12597e157a629a003b6fa17763bce4e3bc414c`  
		Last Modified: Thu, 28 Aug 2025 18:34:49 GMT  
		Size: 254.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:739d3ed94ca4fd5675a334a7346b3719a909fcf92fa1948fc9beb2b504898a66`  
		Last Modified: Thu, 28 Aug 2025 18:34:49 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c899b979c46aa913c49fc5a539c24cc69916b2b8d8e4f45f62abb2802bcb7de`  
		Last Modified: Thu, 28 Aug 2025 18:34:49 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:apache-bookworm` - unknown; unknown

```console
$ docker pull php@sha256:76f7f3a31845729d69ea67e3e857acbdf0bda0471d53438d38b196492b05ec35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7021582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f7ad7ff1956caa7f60862496c5e742f58798a90433aaf577691adcb379bdc2d`

```dockerfile
```

-	Layers:
	-	`sha256:731849c647b243dee1caa9d08c62d7ef89e10245baa1d9d603e38c085d7c7d93`  
		Last Modified: Thu, 28 Aug 2025 19:56:47 GMT  
		Size: 7.0 MB (6959142 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29642655ecd0077f33c17f30927c1cf14fa8a5b40d6d825d4b5bd27c012226e7`  
		Last Modified: Thu, 28 Aug 2025 19:56:48 GMT  
		Size: 62.4 KB (62440 bytes)  
		MIME: application/vnd.in-toto+json

### `php:apache-bookworm` - linux; 386

```console
$ docker pull php@sha256:75e9adb2ee641d85248afc59b5a12e4e60f034cd29336c99c23dc003c17076fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.6 MB (179614120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a185dbd5162cf89d115263b489444e7fa54f14151b67ae54e941b9e2dd64a77`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1754870400'
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 28 Aug 2025 12:46:41 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 28 Aug 2025 12:46:41 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_VERSION=8.4.12
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.12.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.12.tar.xz.asc
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_SHA256=c1b7978cbb5054eed6c749bde4444afc16a3f2268101fb70a7d5d9b1083b12ad
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 28 Aug 2025 12:46:41 GMT
STOPSIGNAL SIGWINCH
# Thu, 28 Aug 2025 12:46:41 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
WORKDIR /var/www/html
# Thu, 28 Aug 2025 12:46:41 GMT
EXPOSE map[80/tcp:{}]
# Thu, 28 Aug 2025 12:46:41 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:de83e1b86bff46f07bde3b82cca8622aed0b900dbeec110f1205a282d10bae64`  
		Last Modified: Tue, 12 Aug 2025 20:46:35 GMT  
		Size: 29.2 MB (29212605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84fb431c48c8303cc27540e3d5e827a48d8a17cf2c714aa053f2e6a25f71935a`  
		Last Modified: Thu, 28 Aug 2025 19:08:59 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7313eb3c371ebff2b5a45a1d46094c70d71894035e7333a90d2ff703426316a`  
		Last Modified: Thu, 28 Aug 2025 19:09:17 GMT  
		Size: 101.5 MB (101516355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6acc5f74676d0fcc1e060b89a418065cc5377105a2969e0914c383eeba003626`  
		Last Modified: Thu, 28 Aug 2025 18:19:52 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e15355c3009823e6e682ff1ee248dd525a646928c19d201bc46dde874ec6907f`  
		Last Modified: Thu, 28 Aug 2025 19:09:00 GMT  
		Size: 20.6 MB (20638461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:132d55ac085cc9c4f26e6394808a1f566fe95c60778bbfb702db48c16d2c931d`  
		Last Modified: Thu, 28 Aug 2025 19:08:57 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aecd9be1d30ef2e31a7d7eb10dc7aa49ebc257baa76ac5ed81c6c6a584da5704`  
		Last Modified: Thu, 28 Aug 2025 19:08:56 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:003df6cdd36b0dcc50ba4680433cc39a8fb40f073be92f7d67bd569765c9be23`  
		Last Modified: Thu, 28 Aug 2025 19:08:57 GMT  
		Size: 13.8 MB (13764509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3785d6d3d3e45bac3fc56d69811605b94c9e2ec30061a718fbe487a4d705e76e`  
		Last Modified: Thu, 28 Aug 2025 19:08:55 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7bfb56f648996af9be57c73d21e329f203a72c01b43ccf002884b73125216ad`  
		Last Modified: Thu, 28 Aug 2025 19:08:57 GMT  
		Size: 14.5 MB (14476458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:089b6346f2153d050f56e8747c6104b38672eb99c7f700166fcb0962291a6e9b`  
		Last Modified: Thu, 28 Aug 2025 19:08:54 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e278ccfe2362399126a4c015e3934f962c8dd083643f94028d9fe57a7134158`  
		Last Modified: Thu, 28 Aug 2025 19:08:54 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd901b8addb397263239b9d67f37d7395db066f04ba34f3e88cfe6c0ecba1f8c`  
		Last Modified: Thu, 28 Aug 2025 19:08:54 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae0d3c63fe086a2870f319d0c1ec74816e654e6d9de85eb6dbe1728c04ebd468`  
		Last Modified: Thu, 28 Aug 2025 19:08:53 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:apache-bookworm` - unknown; unknown

```console
$ docker pull php@sha256:546cb1e4590c3d7a0d02ea21da7f04df58b03d90f7cae3e5f91b1577c6bcaa30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6972659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90033ab0fec2d394ef52a1b1e990059203962c22ad65b01c4ec69df2849ae654`

```dockerfile
```

-	Layers:
	-	`sha256:36d5cf9df738e0c9eb2e1302c6992a2f34ccb6d48a9c80746980e7c8a2185609`  
		Last Modified: Thu, 28 Aug 2025 19:56:54 GMT  
		Size: 6.9 MB (6910495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6fea41958ee513fec659714380959455110cd6a48a089ca4373e968e7237ebe`  
		Last Modified: Thu, 28 Aug 2025 19:56:55 GMT  
		Size: 62.2 KB (62164 bytes)  
		MIME: application/vnd.in-toto+json

### `php:apache-bookworm` - linux; mips64le

```console
$ docker pull php@sha256:73f07538de3e0e6a80db692f765cfd12cae172f0c8fd8b034e0d643d0975262d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.1 MB (156093838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b13bde449954b415469c50d261e34aceae3d18e41b2c828e7f526c8a3b906b2`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1754870400'
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 28 Aug 2025 12:46:41 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 28 Aug 2025 12:46:41 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_VERSION=8.4.12
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.12.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.12.tar.xz.asc
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_SHA256=c1b7978cbb5054eed6c749bde4444afc16a3f2268101fb70a7d5d9b1083b12ad
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 28 Aug 2025 12:46:41 GMT
STOPSIGNAL SIGWINCH
# Thu, 28 Aug 2025 12:46:41 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
WORKDIR /var/www/html
# Thu, 28 Aug 2025 12:46:41 GMT
EXPOSE map[80/tcp:{}]
# Thu, 28 Aug 2025 12:46:41 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:83bd2d8e15bdca1c657f4e1229c9515648aa638816bf4ae6a4be5a7afaee3a81`  
		Last Modified: Tue, 12 Aug 2025 20:45:57 GMT  
		Size: 28.5 MB (28516923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e70e961c3aa4c19afc74902cbfb581bb8d5bace18481280d66f00049ea54978`  
		Last Modified: Wed, 13 Aug 2025 11:46:51 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04b095337cdeffc333a04e84af7d6ae38af5ad6c9b5030f90d64bf50086ff48d`  
		Last Modified: Wed, 13 Aug 2025 11:47:17 GMT  
		Size: 80.7 MB (80668311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd93d7f6ebeea552a680aac5c5c635b6e8290af953530e0dfe110739383d77df`  
		Last Modified: Wed, 13 Aug 2025 11:46:52 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24ebdbff1b2ce904af0c4649e162f512d93a4067f9d67be03739be6a5b7ee9f4`  
		Last Modified: Wed, 13 Aug 2025 12:55:07 GMT  
		Size: 20.1 MB (20069259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:526e4322b09838885afb2a168c5bd2a55566fdddd24dd02e91eadfd0e4ddd3eb`  
		Last Modified: Wed, 13 Aug 2025 12:41:33 GMT  
		Size: 438.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a886583471007fa84bea3f5297e950320ad83acb787a06b459dd901075f34019`  
		Last Modified: Wed, 13 Aug 2025 12:41:34 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bb2aa29b514147da93fb790c6dcf7d38fd142ef6a7db3537454e1df2f3a194b`  
		Last Modified: Thu, 28 Aug 2025 18:51:44 GMT  
		Size: 13.8 MB (13763329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b89be42e650ff031bce5ea8b72bd7ffaea4913eccf619dffcfa343ab58424b`  
		Last Modified: Thu, 28 Aug 2025 18:51:41 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8043fd6f2a87434f1d0e513e3f3b923e7968fcc4c98c793cff34f8e2d8a1d9a`  
		Last Modified: Thu, 28 Aug 2025 18:51:43 GMT  
		Size: 13.1 MB (13070264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff4928c1a4b291a336117ae1a7010128087a257939fb6a224269c56cce4ec66d`  
		Last Modified: Thu, 28 Aug 2025 18:51:42 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eaca69a23541a492c14e0e40cd6a4d69df81700ae830cab1ef2e017ba250b6f`  
		Last Modified: Thu, 28 Aug 2025 18:51:42 GMT  
		Size: 253.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce51ff922d9d83aac4b58a08bc9caa50c6eff08d2b7ceeb62e646eae8cd22f0`  
		Last Modified: Thu, 28 Aug 2025 18:51:42 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b42303eb8756caa3a23f81db2609c1c8d318657218bca34e56f342be1f5e40f3`  
		Last Modified: Thu, 28 Aug 2025 18:51:42 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:apache-bookworm` - unknown; unknown

```console
$ docker pull php@sha256:f9f1be54d3f6e7312d03b1c02399bbc5c530f4dbe1a0a19b787b12a3e09f1fd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.1 KB (62078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eef00ff3334a44cded0a7c6b9911791b2b1459ea9b408e0e5fdaa5ff61568935`

```dockerfile
```

-	Layers:
	-	`sha256:012ce39acd9f41f541abafb4ffcf5c0b69aeb27b21e2b57079c9e9eb92a7e10f`  
		Last Modified: Thu, 28 Aug 2025 19:57:10 GMT  
		Size: 62.1 KB (62078 bytes)  
		MIME: application/vnd.in-toto+json

### `php:apache-bookworm` - linux; ppc64le

```console
$ docker pull php@sha256:c6111a8eda7f9b7d6a85182ff6c55d6954f94057f633f27cecfb8e5d75222dd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.1 MB (185074428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:750242827b1e6e8b6e3dd0aa3f0a6cebad2ca75f7b173bcee9c569b07257c60f`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1754870400'
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 28 Aug 2025 12:46:41 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 28 Aug 2025 12:46:41 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_VERSION=8.4.12
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.12.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.12.tar.xz.asc
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_SHA256=c1b7978cbb5054eed6c749bde4444afc16a3f2268101fb70a7d5d9b1083b12ad
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 28 Aug 2025 12:46:41 GMT
STOPSIGNAL SIGWINCH
# Thu, 28 Aug 2025 12:46:41 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
WORKDIR /var/www/html
# Thu, 28 Aug 2025 12:46:41 GMT
EXPOSE map[80/tcp:{}]
# Thu, 28 Aug 2025 12:46:41 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:a0acf07605078e5950db4f22a00d81ec636270d184a86cff95e60b78f012035c`  
		Last Modified: Tue, 12 Aug 2025 23:06:40 GMT  
		Size: 32.1 MB (32073420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a363500f88bae53ed85a0884af78492e18e2de8fc3862f1472e7a5a3e503dc87`  
		Last Modified: Wed, 13 Aug 2025 06:51:52 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1eb370a99493c04fbb6a54fc3c2fa12bf4afac30b54e58e473794b525eaca2d`  
		Last Modified: Wed, 13 Aug 2025 07:37:29 GMT  
		Size: 103.3 MB (103328754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcc5ef6f8d35100f42cd71cdbcef48544c8e88e6827718d834112c80e310f368`  
		Last Modified: Wed, 13 Aug 2025 07:05:57 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cab47dec8cdcec5cbb5349fb982256d14a603de3b3c8d8e7c6bd16f30d81de63`  
		Last Modified: Wed, 13 Aug 2025 08:51:58 GMT  
		Size: 21.3 MB (21308293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83c723dfb22afab56884f3f5e825b4d8cf66f158c68932630708bc1ae2fb6b7b`  
		Last Modified: Wed, 13 Aug 2025 08:51:59 GMT  
		Size: 436.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bcd34966f4a680377a52a84288adf114ebb46153e83b68cdde845b06ea68fe3`  
		Last Modified: Wed, 13 Aug 2025 08:52:00 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f97e837562ada19715ab01f7aa89e21267914f1d013ecdba36f366ec9dbc05`  
		Last Modified: Thu, 28 Aug 2025 18:42:54 GMT  
		Size: 13.8 MB (13764956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab6bf6fce72c8a0eb43d71cddaf46b68e2a53cedd2cd84a0a1b0209c1ebb4696`  
		Last Modified: Thu, 28 Aug 2025 18:42:54 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc41e86f90c76a7cfeec62ca51b37eb2399a1121b2745b5bc24cf19514362a1c`  
		Last Modified: Thu, 28 Aug 2025 18:42:54 GMT  
		Size: 14.6 MB (14593252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f8fabcb61d68e0eac73ebd02741cc2311839687a700e9a7eb2acc3519d59756`  
		Last Modified: Thu, 28 Aug 2025 18:42:52 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99ff2c6b6957279306cb6dcdaa20576650940d9aea33bc56f2048d75460ad09d`  
		Last Modified: Thu, 28 Aug 2025 18:42:52 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014bac8d965b01261ecb7ed997d88dc662c5c2c69c51deab4143fa4001f0f801`  
		Last Modified: Thu, 28 Aug 2025 18:42:53 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:238f73d0cf0b4366b237cd6ebb56c6d813c9b72b21762c0916d9f8a8082e6302`  
		Last Modified: Thu, 28 Aug 2025 18:42:53 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:apache-bookworm` - unknown; unknown

```console
$ docker pull php@sha256:87dd942b74936364bd62cb943caa604760e152f1da8cd30f6828c523ed14ab21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6969793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:233bec8c4e00413933dc793a27a59591fea785635701f043bd29e9bfa890c5bb`

```dockerfile
```

-	Layers:
	-	`sha256:7420ed5fc06b4b5ce2b9b07db3a41c97a3278fc810c6617362976b88f7a19b46`  
		Last Modified: Thu, 28 Aug 2025 19:57:20 GMT  
		Size: 6.9 MB (6907517 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31f23a5f7a0308255df3cfa53ac2a10685e32042ee15a8f56bf2c817204af089`  
		Last Modified: Thu, 28 Aug 2025 19:57:21 GMT  
		Size: 62.3 KB (62276 bytes)  
		MIME: application/vnd.in-toto+json

### `php:apache-bookworm` - linux; s390x

```console
$ docker pull php@sha256:de215ebfd0e8dffe0e453dca9986b4d059afc965990a646961314fe73daecee1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.9 MB (154925855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c55779375252e98bf50b7606f3b218ffb0d8c4a642382a589425c05282da3962`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1754870400'
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 28 Aug 2025 12:46:41 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 28 Aug 2025 12:46:41 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_VERSION=8.4.12
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.12.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.12.tar.xz.asc
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_SHA256=c1b7978cbb5054eed6c749bde4444afc16a3f2268101fb70a7d5d9b1083b12ad
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 28 Aug 2025 12:46:41 GMT
STOPSIGNAL SIGWINCH
# Thu, 28 Aug 2025 12:46:41 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
WORKDIR /var/www/html
# Thu, 28 Aug 2025 12:46:41 GMT
EXPOSE map[80/tcp:{}]
# Thu, 28 Aug 2025 12:46:41 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:1ae61276e6df96a4fa21616b89ef0ebf78ce7e8d7e42d3264ead2281b12b910a`  
		Last Modified: Wed, 13 Aug 2025 09:16:19 GMT  
		Size: 26.9 MB (26887836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:160fd1a1a421ab2a967d88788fa69f4a8c0d0124bb8618a96dadd2d0b88b93ca`  
		Last Modified: Wed, 13 Aug 2025 10:57:35 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a62186e269f8e7afe7503ad0b95ed43cf9977a95fe4bf4276d7b309de1b2630`  
		Last Modified: Wed, 13 Aug 2025 11:56:29 GMT  
		Size: 80.8 MB (80826980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:283e45bba3759ef3324f879c06fb1eebcda36d5470316f27b6e2fd8d86a8a0d2`  
		Last Modified: Wed, 13 Aug 2025 10:57:36 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a89f7c20ff77c478fb295cf8f66b8260fe7d9594c7da1d918e23894e507d5e3`  
		Last Modified: Wed, 13 Aug 2025 12:57:49 GMT  
		Size: 19.9 MB (19895051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa7f9b3cb117e520c58e1fed8ebca993aac8c5add667e0e6eba824c44117ebc6`  
		Last Modified: Wed, 13 Aug 2025 11:13:23 GMT  
		Size: 432.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e61f86598fd509db3d73f90a72a7b48d5a025fd2791a5be72d43645b236db1c`  
		Last Modified: Wed, 13 Aug 2025 11:13:25 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a89521a1f91535724c73a876a31313c12b60a20e54c030d394ceab145ba5cf97`  
		Last Modified: Thu, 28 Aug 2025 18:59:37 GMT  
		Size: 13.8 MB (13763973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74740c1d8967eb87dbc301a09f22ad9b8fec32647f84f3a9cdea5ce25c97729f`  
		Last Modified: Thu, 28 Aug 2025 18:59:35 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d40dd3ac031de2e8d58b0ad8e35acc88c68159507255a69f13f1b538bede1825`  
		Last Modified: Thu, 28 Aug 2025 18:59:36 GMT  
		Size: 13.5 MB (13546273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9170394d4373289831e57de96454535dc1c761d1b9c1f7b4277450e750279238`  
		Last Modified: Thu, 28 Aug 2025 18:59:36 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f15f831f7c5558a46367f8ce518646080bd8b08ab2f8b321c385182c75d304bd`  
		Last Modified: Thu, 28 Aug 2025 18:59:36 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a0b7216c79cb96d03458347ecc14cc3d126718420ddd634e61e88862e5f354d`  
		Last Modified: Thu, 28 Aug 2025 18:59:36 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:463f9d02bf1104c1280c359a7284a1065f9c02caa7c5415bb80e750dee349b5d`  
		Last Modified: Thu, 28 Aug 2025 18:59:36 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:apache-bookworm` - unknown; unknown

```console
$ docker pull php@sha256:b62582645e85f48e384c1b316ba45332cbe653a6a4cf6e9f33aff4b07d1be64f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6830143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90f0559711cb920078113e02387ef5e4534ff910156abca906794abeec42f954`

```dockerfile
```

-	Layers:
	-	`sha256:33bffda16637e29f1ce0b18cd9645f07765776547d3baa751ef63b477618aafd`  
		Last Modified: Thu, 28 Aug 2025 19:57:27 GMT  
		Size: 6.8 MB (6767943 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2d2022e456e746608f5f97bf962cb48468e692f94bb0e44068eaa159661f079`  
		Last Modified: Thu, 28 Aug 2025 19:57:28 GMT  
		Size: 62.2 KB (62200 bytes)  
		MIME: application/vnd.in-toto+json
