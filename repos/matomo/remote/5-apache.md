## `matomo:5-apache`

```console
$ docker pull matomo@sha256:d2c004617559f0c9fc1398fc2c7205f4c0194cfe59052b277b5a3c1f2c137e96
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

### `matomo:5-apache` - linux; amd64

```console
$ docker pull matomo@sha256:0444160824007c58934a9ce67432eb691ebde7c499fe55755355a0fa772800f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.9 MB (201890682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4689968fb40cef235d5371df9afc5b455c1f1df39afc964dc1420a4899b20186`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 25 Sep 2024 20:44:12 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
CMD ["bash"]
# Wed, 25 Sep 2024 20:44:12 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 25 Sep 2024 20:44:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 25 Sep 2024 20:44:12 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 25 Sep 2024 20:44:12 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 25 Sep 2024 20:44:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 25 Sep 2024 20:44:12 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 25 Sep 2024 20:44:12 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 25 Sep 2024 20:44:12 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 25 Sep 2024 20:44:12 GMT
ENV PHP_VERSION=8.2.26
# Wed, 25 Sep 2024 20:44:12 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.26.tar.xz.asc
# Wed, 25 Sep 2024 20:44:12 GMT
ENV PHP_SHA256=54747400cb4874288ad41a785e6147e2ff546cceeeb55c23c00c771ac125c6ef
# Wed, 25 Sep 2024 20:44:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 25 Sep 2024 20:44:12 GMT
STOPSIGNAL SIGWINCH
# Wed, 25 Sep 2024 20:44:12 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
WORKDIR /var/www/html
# Wed, 25 Sep 2024 20:44:12 GMT
EXPOSE map[80/tcp:{}]
# Wed, 25 Sep 2024 20:44:12 GMT
CMD ["apache2-foreground"]
# Wed, 25 Sep 2024 20:44:12 GMT
ENV PHP_MEMORY_LIMIT=256M
# Wed, 25 Sep 2024 20:44:12 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype-dev 		libjpeg-dev 		libldap2-dev 		libpng-dev 		libzip-dev 		procps 	; 		debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		opcache 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.24; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
ENV MATOMO_VERSION=5.1.2
# Wed, 25 Sep 2024 20:44:12 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends 		$fetchDeps 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
VOLUME [/var/www/html]
# Wed, 25 Sep 2024 20:44:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 25 Sep 2024 20:44:12 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e3574ead1d990893bb2459fc5a477c1ee4efdc0f6d664b3205b3a3056c90ff8`  
		Last Modified: Thu, 21 Nov 2024 18:00:46 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33ddd73cf168e90573f670de73ca0de14790a796c52a4d0f544aca1f4f83b790`  
		Last Modified: Thu, 21 Nov 2024 18:00:47 GMT  
		Size: 104.3 MB (104345688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03e622ab61136363f89bac172f18a8f82b27867bdab0b0dc4dcf8e11d9c6c60e`  
		Last Modified: Thu, 21 Nov 2024 18:00:04 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d465c9a467df5a6900300468a7a73ef63421fa438ccf79a38f0c74bd044fb6b`  
		Last Modified: Thu, 21 Nov 2024 18:00:46 GMT  
		Size: 20.1 MB (20123804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c99b33b2d2dfd18034761fc69c5b5c672435cc3b751641984adf91c2e092b24d`  
		Last Modified: Thu, 21 Nov 2024 18:00:46 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8944b2c2d493789377b35d9a87a7db5f5e776a22fba916f487a9f7fd67db844e`  
		Last Modified: Thu, 21 Nov 2024 18:00:47 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b95e19029c21bd45bd418cc03230aab00e0f46b1fdcffad73e018f609252d2d3`  
		Last Modified: Thu, 21 Nov 2024 18:00:47 GMT  
		Size: 12.3 MB (12267606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ecc49d93144af74c148d91f735dffeb16fec09d2fe5d2e9ec9b10ff1d55e607`  
		Last Modified: Thu, 21 Nov 2024 18:00:47 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:413b3a10b41e9bb1545e62ac0a1be8c525a91b20b6a2506fe1b65bb0e0e7c3dc`  
		Last Modified: Thu, 21 Nov 2024 18:00:48 GMT  
		Size: 11.4 MB (11414696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93e37cdea03daf4396d431a6649ea544c60928b3da77d7f5959795e6bf4dcf3e`  
		Last Modified: Thu, 21 Nov 2024 18:00:48 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3cdaf28ff9fa96b13d4b3ad875e9fd9a150b3c3e308db8de8cd30a6803fc82`  
		Last Modified: Thu, 21 Nov 2024 18:00:48 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bebb38845b62901e1a0063317ad2706e7c68bab2e0eb87ad4c9ac2b6c7d0a31e`  
		Last Modified: Thu, 21 Nov 2024 18:00:48 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31421b4bc6ec402fa3a006ec0c68d0e78fba0169017481fb35eed562ad4f32ce`  
		Last Modified: Thu, 21 Nov 2024 18:13:56 GMT  
		Size: 3.3 MB (3256255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3c67fc868251134e1cba7adca2bce97ed208196bd71a1006710cdf68db50903`  
		Last Modified: Thu, 21 Nov 2024 18:13:55 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef60395f10197e4e3686e8546619f3d3b00c2102a27094bcbb0bcf45f9d9abf`  
		Last Modified: Thu, 21 Nov 2024 18:13:56 GMT  
		Size: 21.3 MB (21347686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08b04f0fb6affa79ddae90cbd802d3032197ab088702d78290e1d30c232c7059`  
		Last Modified: Thu, 21 Nov 2024 18:13:55 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:146d2812821fe1489bfa3f32eca81415e2ca00730b29bf3b33ac9ecfc081f3be`  
		Last Modified: Thu, 21 Nov 2024 18:13:56 GMT  
		Size: 824.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:5-apache` - unknown; unknown

```console
$ docker pull matomo@sha256:d5371326842944029ab552e10adaed345e042214ea335d2f52cf7cf3907de973
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 KB (36373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f077e7f1984d3d81582cee7bd3245e39501d5013d923231ba5731a3c3ec25bbc`

```dockerfile
```

-	Layers:
	-	`sha256:6a4d17aaaa452271c30ee3125549acf8d34c827502fec88e8042dc99b23f10c5`  
		Last Modified: Thu, 21 Nov 2024 18:13:55 GMT  
		Size: 36.4 KB (36373 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:5-apache` - linux; arm variant v5

```console
$ docker pull matomo@sha256:96cfcb7cf17ce354819929d932405473ff82a803989c05269bd888b443bc97c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.0 MB (175024038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99d43134f7d03a00fdd4e4a8f2ba5073179e98b96591626c3fe37684f9411c42`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 25 Sep 2024 20:44:12 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
CMD ["bash"]
# Wed, 25 Sep 2024 20:44:12 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 25 Sep 2024 20:44:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 25 Sep 2024 20:44:12 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 25 Sep 2024 20:44:12 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 25 Sep 2024 20:44:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 25 Sep 2024 20:44:12 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 25 Sep 2024 20:44:12 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 25 Sep 2024 20:44:12 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 25 Sep 2024 20:44:12 GMT
ENV PHP_VERSION=8.2.25
# Wed, 25 Sep 2024 20:44:12 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.25.tar.xz.asc
# Wed, 25 Sep 2024 20:44:12 GMT
ENV PHP_SHA256=330b54876ea1d05ade12ee9726167332058bccd58dffa1d4e12117f6b4f616b9
# Wed, 25 Sep 2024 20:44:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 25 Sep 2024 20:44:12 GMT
STOPSIGNAL SIGWINCH
# Wed, 25 Sep 2024 20:44:12 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
WORKDIR /var/www/html
# Wed, 25 Sep 2024 20:44:12 GMT
EXPOSE map[80/tcp:{}]
# Wed, 25 Sep 2024 20:44:12 GMT
CMD ["apache2-foreground"]
# Wed, 25 Sep 2024 20:44:12 GMT
ENV PHP_MEMORY_LIMIT=256M
# Wed, 25 Sep 2024 20:44:12 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype-dev 		libjpeg-dev 		libldap2-dev 		libpng-dev 		libzip-dev 		procps 	; 		debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		opcache 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.24; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
ENV MATOMO_VERSION=5.1.2
# Wed, 25 Sep 2024 20:44:12 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends 		$fetchDeps 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
VOLUME [/var/www/html]
# Wed, 25 Sep 2024 20:44:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 25 Sep 2024 20:44:12 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:5ecbccf2cc6c4ffb179160d83e2f057a548b6aea719fc2b9b49c502da3d570e3`  
		Last Modified: Tue, 12 Nov 2024 00:55:10 GMT  
		Size: 26.9 MB (26890058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a0ecfad706f423d72f784713c6e330fb07894f5581828886246a6f696dc5dcd`  
		Last Modified: Tue, 12 Nov 2024 02:32:34 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bdc0003cb59a2246daf9c98d60695941f3b7fb3e946787615b6b24498c2902a`  
		Last Modified: Tue, 12 Nov 2024 02:32:37 GMT  
		Size: 82.0 MB (81992661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30d7cc6d2cd608d6e46c893c66f11311b91174768d7c19e4e8fab10922f896d1`  
		Last Modified: Tue, 12 Nov 2024 02:32:34 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dc288200a587c04c4a516848305eb50a074c72c0da800766f18c69bf488a295`  
		Last Modified: Tue, 12 Nov 2024 02:38:57 GMT  
		Size: 19.4 MB (19419230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd8e4f30b1778e27afb7a2ff3afe61620a6461135330c97674b47ec1cba026cc`  
		Last Modified: Tue, 12 Nov 2024 02:38:56 GMT  
		Size: 437.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:464be6317f9579fddccfdb0447cafdd2b1dd8b860a64422d6dc5ff442e9bb491`  
		Last Modified: Tue, 12 Nov 2024 02:38:56 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f8ebd18ae3f14556164436fa0d85ddb353f8a1128786a1fd4541f9712d07782`  
		Last Modified: Tue, 12 Nov 2024 04:02:15 GMT  
		Size: 12.3 MB (12253184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b2618ff9378d468fb1184d19c5f1da58142516f607f6cba3af68d19f6beec45`  
		Last Modified: Tue, 12 Nov 2024 04:02:14 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d1b76f1957d95f72e17268a94eee95088a2cf42cafbac4b66da6ed854eeed21`  
		Last Modified: Tue, 12 Nov 2024 04:02:15 GMT  
		Size: 10.4 MB (10392847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e449f62e8cd60216bc2f546e993bebcd4ee51b229ac224bfb0d1791552a6ce2c`  
		Last Modified: Tue, 12 Nov 2024 04:02:14 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4ac27ab7a9f78c55da42c79834a77957249e22964978a87ab4e2ac358915345`  
		Last Modified: Tue, 12 Nov 2024 04:02:15 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c3ca3f4bc777b59fa6a38c8ab3ab11f8a842a35d9f90d3b2333ca3bfcf839fe`  
		Last Modified: Tue, 12 Nov 2024 04:02:15 GMT  
		Size: 886.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90cc2a4f79fed3d140269b9f0552b1c5ffa7799877fd2d1e6126f8652ec6ffb5`  
		Last Modified: Tue, 12 Nov 2024 12:43:53 GMT  
		Size: 2.7 MB (2723368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:641e38c3962d8c5889670b9578ed27288047a4c811142bc2d7750977f5d02bfb`  
		Last Modified: Tue, 12 Nov 2024 12:43:53 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04fbca684eb7ac26be4bfe97ff9e82668a06c53c09dde336c81f9a47a301c5be`  
		Last Modified: Tue, 12 Nov 2024 12:43:54 GMT  
		Size: 21.3 MB (21345719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47af20b3f0e478b61e298ea628e94422b2c953d753b53725ac698cce5e1cbe9c`  
		Last Modified: Tue, 12 Nov 2024 12:43:53 GMT  
		Size: 343.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b11753908978d10117bfdfa6a056affb0c9dcf781ecd08e91d97aa4937e151b`  
		Last Modified: Tue, 12 Nov 2024 12:43:54 GMT  
		Size: 824.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:5-apache` - unknown; unknown

```console
$ docker pull matomo@sha256:20e61f4311d792fce98675504741b78ca4e7cb4217ca8f51ca9bae8e391e3186
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.5 KB (36501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9e713b42be66d3c38c53e40db4fb0c1a72831cf5f0fd2f32e510d4022249c14`

```dockerfile
```

-	Layers:
	-	`sha256:022e892a126882abfc4c18394c455c6aad1a860b32f1bca546ca611ba532b872`  
		Last Modified: Tue, 12 Nov 2024 12:43:52 GMT  
		Size: 36.5 KB (36501 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:5-apache` - linux; arm variant v7

```console
$ docker pull matomo@sha256:cecc08a1f7678d3a2f0bfee7475844b634eed3788998ab75523ca9664f95f0f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.8 MB (165771823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38238a699a77c21dca0c47454128f1197dfe6daf5dddc01a95c9d4403fee7439`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 25 Sep 2024 20:44:12 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
CMD ["bash"]
# Wed, 25 Sep 2024 20:44:12 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 25 Sep 2024 20:44:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 25 Sep 2024 20:44:12 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 25 Sep 2024 20:44:12 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 25 Sep 2024 20:44:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 25 Sep 2024 20:44:12 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 25 Sep 2024 20:44:12 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 25 Sep 2024 20:44:12 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 25 Sep 2024 20:44:12 GMT
ENV PHP_VERSION=8.2.25
# Wed, 25 Sep 2024 20:44:12 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.25.tar.xz.asc
# Wed, 25 Sep 2024 20:44:12 GMT
ENV PHP_SHA256=330b54876ea1d05ade12ee9726167332058bccd58dffa1d4e12117f6b4f616b9
# Wed, 25 Sep 2024 20:44:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 25 Sep 2024 20:44:12 GMT
STOPSIGNAL SIGWINCH
# Wed, 25 Sep 2024 20:44:12 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
WORKDIR /var/www/html
# Wed, 25 Sep 2024 20:44:12 GMT
EXPOSE map[80/tcp:{}]
# Wed, 25 Sep 2024 20:44:12 GMT
CMD ["apache2-foreground"]
# Wed, 25 Sep 2024 20:44:12 GMT
ENV PHP_MEMORY_LIMIT=256M
# Wed, 25 Sep 2024 20:44:12 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype-dev 		libjpeg-dev 		libldap2-dev 		libpng-dev 		libzip-dev 		procps 	; 		debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		opcache 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.24; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
ENV MATOMO_VERSION=5.1.2
# Wed, 25 Sep 2024 20:44:12 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends 		$fetchDeps 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
VOLUME [/var/www/html]
# Wed, 25 Sep 2024 20:44:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 25 Sep 2024 20:44:12 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:ddd3c6488ea8b62db6811ba136fe14cba70219532910e67a91ed3388ec9f5757`  
		Last Modified: Tue, 12 Nov 2024 00:56:42 GMT  
		Size: 24.7 MB (24718909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4297c5ae3c7e8e8915409622802213bf4512c2b4a0bf9a86ed680878ddc18a70`  
		Last Modified: Tue, 12 Nov 2024 03:10:01 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc4b50adcb7cdffa12052ba1589718b3c06d474e40507177a93fc914de46e895`  
		Last Modified: Tue, 12 Nov 2024 03:10:04 GMT  
		Size: 76.2 MB (76162385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:681174cd466f54c52977f6c159c33d12bdd6aa108d2d06470ff258ce5d3fac19`  
		Last Modified: Tue, 12 Nov 2024 03:10:01 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3956adc6ba757482684b1a409597f790541c714f71ba631eee7d291574e817e`  
		Last Modified: Tue, 12 Nov 2024 03:15:54 GMT  
		Size: 18.9 MB (18857501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1e647e764fe2dcfbd101cd5fcaaec1c944c7cd89cd40a65dcd2442b62733654`  
		Last Modified: Tue, 12 Nov 2024 03:15:53 GMT  
		Size: 433.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:429807ca1f9d7d3c489deadada060b40a6d8bd76e76a48f0a9298d511be0304c`  
		Last Modified: Tue, 12 Nov 2024 03:15:53 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d182f4c6df47bdbe3801f7d6d20ad82afa8001530cd368ebd61776e5f50fa3ad`  
		Last Modified: Tue, 12 Nov 2024 08:04:05 GMT  
		Size: 12.3 MB (12253256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70022f0643e3c81a43c68d9dcf290573d5a8b74a3056e95d556f8bd898350a24`  
		Last Modified: Tue, 12 Nov 2024 08:04:04 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85edb6998fe32e0449c2b45b63c9f40c23f96c703a8722b3cadf0dd3b571a76a`  
		Last Modified: Tue, 12 Nov 2024 08:04:05 GMT  
		Size: 9.8 MB (9824931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53fbe069c23ad21b149523d0d100a569b4c601bd3b71b58265ba8e91e3175801`  
		Last Modified: Tue, 12 Nov 2024 08:04:04 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c4049646dc9e66848219df55afd2063bf3b7bd0ca7b3ca89ebf11ddb694da9`  
		Last Modified: Tue, 12 Nov 2024 08:04:05 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd3b1967ec410bfa1f113f761eaefd23810d8f7b1f979498f2ea2917bcd170ea`  
		Last Modified: Tue, 12 Nov 2024 08:04:05 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c77b26776f56d5ba1568cd07139d5218fc288a01a6face30eae91551bc367d9`  
		Last Modified: Wed, 13 Nov 2024 09:35:37 GMT  
		Size: 2.6 MB (2602055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:440f4a7214b24fbf440465e3c09fdfec63018f4669d22525f907cb99361d5dba`  
		Last Modified: Wed, 13 Nov 2024 09:35:37 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bc1f3737798c82298de0200d0d4224e135cd57a8ad97b00c2966c3abfb9c8db`  
		Last Modified: Wed, 13 Nov 2024 09:35:38 GMT  
		Size: 21.3 MB (21345808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79025fd1c7583d4467c9cb2e5fa7e8b99f51343108c568cd53925d0090e3862f`  
		Last Modified: Wed, 13 Nov 2024 09:35:37 GMT  
		Size: 343.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f940c16712f1afa1e961248ac1779cc6c875e56afee7dc9bb51262d44f9c610`  
		Last Modified: Wed, 13 Nov 2024 09:35:37 GMT  
		Size: 824.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:5-apache` - unknown; unknown

```console
$ docker pull matomo@sha256:99f763304a4c9f2ae5f3b4805f287ff34c1d27676f3f6b43e9a7da42d5d9f52c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.5 KB (36495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5846cda824e41ff4f5a6cd8578da381d7396f7b0f0aa383897c0d2bfb54a0fae`

```dockerfile
```

-	Layers:
	-	`sha256:969319eb734dfca69f084a64acf0862429c205d1c3f1f0e580752cc6f52d8312`  
		Last Modified: Wed, 13 Nov 2024 09:35:36 GMT  
		Size: 36.5 KB (36495 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:5-apache` - linux; arm64 variant v8

```console
$ docker pull matomo@sha256:daedff3c483c2547fbfe1350bf4ac52b5a65426c09c0eea3056eebbbb3e1f3bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.9 MB (195938054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:906bbe43b84f7976e55d04ae2f877d4b2703cf34af60b0f8acd432643e10ca5e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 25 Sep 2024 20:44:12 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
CMD ["bash"]
# Wed, 25 Sep 2024 20:44:12 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 25 Sep 2024 20:44:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 25 Sep 2024 20:44:12 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 25 Sep 2024 20:44:12 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 25 Sep 2024 20:44:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 25 Sep 2024 20:44:12 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 25 Sep 2024 20:44:12 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 25 Sep 2024 20:44:12 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 25 Sep 2024 20:44:12 GMT
ENV PHP_VERSION=8.2.25
# Wed, 25 Sep 2024 20:44:12 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.25.tar.xz.asc
# Wed, 25 Sep 2024 20:44:12 GMT
ENV PHP_SHA256=330b54876ea1d05ade12ee9726167332058bccd58dffa1d4e12117f6b4f616b9
# Wed, 25 Sep 2024 20:44:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 25 Sep 2024 20:44:12 GMT
STOPSIGNAL SIGWINCH
# Wed, 25 Sep 2024 20:44:12 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
WORKDIR /var/www/html
# Wed, 25 Sep 2024 20:44:12 GMT
EXPOSE map[80/tcp:{}]
# Wed, 25 Sep 2024 20:44:12 GMT
CMD ["apache2-foreground"]
# Wed, 25 Sep 2024 20:44:12 GMT
ENV PHP_MEMORY_LIMIT=256M
# Wed, 25 Sep 2024 20:44:12 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype-dev 		libjpeg-dev 		libldap2-dev 		libpng-dev 		libzip-dev 		procps 	; 		debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		opcache 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.24; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
ENV MATOMO_VERSION=5.1.2
# Wed, 25 Sep 2024 20:44:12 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends 		$fetchDeps 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
VOLUME [/var/www/html]
# Wed, 25 Sep 2024 20:44:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 25 Sep 2024 20:44:12 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29e9756e7bfc559baf6454131f81839efb97d80f167664be5b4272ac469b5960`  
		Last Modified: Tue, 12 Nov 2024 03:32:16 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e27785ead77c6cc3a0473bbe35b537db4b7a71bc35c6289f88af2c9ee06119`  
		Last Modified: Tue, 12 Nov 2024 03:32:19 GMT  
		Size: 98.1 MB (98130714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27a00cfa6daf2de029a0f81a774bb1018582dc28b1eb0b8bb09c1d7672fb91ce`  
		Last Modified: Tue, 12 Nov 2024 03:32:16 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca35e1d28ad7ebbff66a1fdc4d24ada4c30b131fd323f6cbea4b7fb07bc8d706`  
		Last Modified: Tue, 12 Nov 2024 03:36:02 GMT  
		Size: 20.1 MB (20120907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410639cb967ec54ee760206ed58c1613b50690b91d753ac3ebf143807443f069`  
		Last Modified: Tue, 12 Nov 2024 03:36:01 GMT  
		Size: 439.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f9efafdf219d3eb366948d2078a5f7f1d4ff893121d52b94c89678ccbee36ac`  
		Last Modified: Tue, 12 Nov 2024 03:36:01 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7946ba9a569f7e501c4f65b60c14167db6ae2052d4f038db286852df797af96`  
		Last Modified: Tue, 12 Nov 2024 07:23:33 GMT  
		Size: 12.3 MB (12254617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67f1de0deede2eea05e09dfb8a4bd8e892e3d808eef90b51356361daa7908115`  
		Last Modified: Tue, 12 Nov 2024 07:23:32 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d96ecd01e3f5ffa0265fa88830a9f954864c62085c8683fd139f9274eb517e54`  
		Last Modified: Tue, 12 Nov 2024 07:23:33 GMT  
		Size: 11.4 MB (11417386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c470e029cbda8a745b58452eea84ffb1e4b18c339ef318651bb74678eebc3fc2`  
		Last Modified: Tue, 12 Nov 2024 07:23:32 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77cbd2f3c900a11e4239528e754af9ea385218d944926df0c65cf41cd3d7dbc7`  
		Last Modified: Tue, 12 Nov 2024 07:23:33 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:646aa471737e5afeb30a122b1b252d4898b4550224496770b174a2e0b34972f6`  
		Last Modified: Tue, 12 Nov 2024 07:23:33 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbe98e5a2ac3b6822774f05c239a563249569a935c172d08f0b21e68f3185396`  
		Last Modified: Wed, 13 Nov 2024 04:48:55 GMT  
		Size: 3.5 MB (3502619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:903ec8a96138d591ac71bac0da8f1c01c8d2865407de393056aafb858553eb07`  
		Last Modified: Wed, 13 Nov 2024 04:48:54 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55c13611f813f29d8a939a631734fb409511b090a97d52e92221fe0b2c9dc5ff`  
		Last Modified: Wed, 13 Nov 2024 04:48:55 GMT  
		Size: 21.3 MB (21347485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6c15f93587a69daaa620e42db7bdacf6a1884d746a061ddcfeb69921ebbb48e`  
		Last Modified: Wed, 13 Nov 2024 04:48:54 GMT  
		Size: 342.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef44c356d6849a0db7f766e2878909df04c41343b9b11de41318df631e2e4537`  
		Last Modified: Wed, 13 Nov 2024 04:48:55 GMT  
		Size: 823.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:5-apache` - unknown; unknown

```console
$ docker pull matomo@sha256:e1cce8d0f9b3b2647c812d3433d5df8dbe9112365dab3f312335d0db078d67d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.5 KB (36549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54e40beaf6c4eae58747bd1575902702903561c78831d16564b4727d0f4f99db`

```dockerfile
```

-	Layers:
	-	`sha256:d11a7a1a596c8519dd23b8daef3006728e146b8cc85bf6aeded5ff628bc6dbb2`  
		Last Modified: Wed, 13 Nov 2024 04:48:54 GMT  
		Size: 36.5 KB (36549 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:5-apache` - linux; 386

```console
$ docker pull matomo@sha256:e0be36485b1b0e5865bad2227db6024d2aa9670874572146e414b55b74bbddc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.8 MB (200768818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f645aea585fb43e2fbc6c0cf8962ef5244c8c37e79a2a70f5cdc3bd21db0bebf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 25 Sep 2024 20:44:12 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
CMD ["bash"]
# Wed, 25 Sep 2024 20:44:12 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 25 Sep 2024 20:44:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 25 Sep 2024 20:44:12 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 25 Sep 2024 20:44:12 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 25 Sep 2024 20:44:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 25 Sep 2024 20:44:12 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 25 Sep 2024 20:44:12 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 25 Sep 2024 20:44:12 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 25 Sep 2024 20:44:12 GMT
ENV PHP_VERSION=8.2.26
# Wed, 25 Sep 2024 20:44:12 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.26.tar.xz.asc
# Wed, 25 Sep 2024 20:44:12 GMT
ENV PHP_SHA256=54747400cb4874288ad41a785e6147e2ff546cceeeb55c23c00c771ac125c6ef
# Wed, 25 Sep 2024 20:44:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 25 Sep 2024 20:44:12 GMT
STOPSIGNAL SIGWINCH
# Wed, 25 Sep 2024 20:44:12 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
WORKDIR /var/www/html
# Wed, 25 Sep 2024 20:44:12 GMT
EXPOSE map[80/tcp:{}]
# Wed, 25 Sep 2024 20:44:12 GMT
CMD ["apache2-foreground"]
# Wed, 25 Sep 2024 20:44:12 GMT
ENV PHP_MEMORY_LIMIT=256M
# Wed, 25 Sep 2024 20:44:12 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype-dev 		libjpeg-dev 		libldap2-dev 		libpng-dev 		libzip-dev 		procps 	; 		debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		opcache 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.24; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
ENV MATOMO_VERSION=5.1.2
# Wed, 25 Sep 2024 20:44:12 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends 		$fetchDeps 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
VOLUME [/var/www/html]
# Wed, 25 Sep 2024 20:44:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 25 Sep 2024 20:44:12 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:7379b58056e85869f90d8f78478cafd0c7468ad3b5085482a0850cee625a847a`  
		Last Modified: Tue, 12 Nov 2024 00:54:51 GMT  
		Size: 30.1 MB (30145450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7695c3c5f3eb69897df354e34ee497e1575155490113c736890ba59a7c4e9eb`  
		Last Modified: Thu, 21 Nov 2024 18:00:43 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab9f6c34c9d20519332651965361204da09fdfa19caa30feb75a9f964359055f`  
		Last Modified: Thu, 21 Nov 2024 18:01:02 GMT  
		Size: 101.5 MB (101514287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e268ed05784661b34bd93e4e3230c07459b90ed1d05ab612b1c4fbef636c6150`  
		Last Modified: Thu, 21 Nov 2024 18:00:59 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f003944d363818d4681ef9616367aa5253d769a143acdf39e01d387518fa6151`  
		Last Modified: Thu, 21 Nov 2024 18:01:00 GMT  
		Size: 20.6 MB (20638497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6bcb0d71ea9a0d39e2904a451fd153aa209f76a40a8a117b171f7c2f38a5dd4`  
		Last Modified: Thu, 21 Nov 2024 18:01:00 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9737a99b0590607a61242476091440506cc212d5915cfb8cd5498e9e1eac459`  
		Last Modified: Thu, 21 Nov 2024 18:01:00 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fa86440c98cef64d48fed71d4c82622b799d168232202f99f7f18d992a8ecc2`  
		Last Modified: Thu, 21 Nov 2024 18:01:01 GMT  
		Size: 12.3 MB (12266631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dec720eb381967492446d7878c0cda00d3fe822d7e84a7caa4caf5d24e7ce5e3`  
		Last Modified: Thu, 21 Nov 2024 18:01:01 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f9a21503ece2bddcc514eb5c14d26d8dec2395ed85cb3ff49280df3d3d189c5`  
		Last Modified: Thu, 21 Nov 2024 18:01:01 GMT  
		Size: 11.6 MB (11643206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22e72c5b47efb77bd57297d27e4ae846e903cc2f0a362540fcbb3bc30ccabfbb`  
		Last Modified: Thu, 21 Nov 2024 18:01:01 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:774982c679f677f87f181e4cf9e1d3c5cce5967bae9994c015a1301dd6b29e8e`  
		Last Modified: Thu, 21 Nov 2024 18:01:02 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0db0337c4b1dad71d5384d860fad65ae1c697fabb24ae988ca8a63def295c82`  
		Last Modified: Thu, 21 Nov 2024 18:01:02 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38a432017c5d8d3f59a82dfe3b07d491affa31f4cb6ae638e33d9b1e4cf0a688`  
		Last Modified: Thu, 21 Nov 2024 18:13:52 GMT  
		Size: 3.2 MB (3207299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27b495e6638591df5464082aa7902c711210ca7ec717c568b7fe0c31d3486289`  
		Last Modified: Thu, 21 Nov 2024 18:13:52 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4146cdccc495662c95cce9fde2ad064cdd2606224b7a233b116ce8caa87c4bc1`  
		Last Modified: Thu, 21 Nov 2024 18:13:53 GMT  
		Size: 21.3 MB (21346488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aec04166f09210f0f847d1ff49649bc729faf2be6dd476377eff4f2f12926ac`  
		Last Modified: Thu, 21 Nov 2024 18:13:52 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad1983e7d68a2eb5115820b0f5d3852ea63488782c8435929d56dab8264995d`  
		Last Modified: Thu, 21 Nov 2024 18:13:52 GMT  
		Size: 823.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:5-apache` - unknown; unknown

```console
$ docker pull matomo@sha256:b55ea5c142af3f5ea783226944c0f3cefcf578aefab8cf9584bda7180d16bb23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.3 KB (36317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37bd4d97fb82a7be7911d69039482cae92c6879dcb6fc66bb962b6c37d0b9143`

```dockerfile
```

-	Layers:
	-	`sha256:fd46a11169934b3d107fc43246f48329ffe71fae2f5e426ce67641761bdb8c98`  
		Last Modified: Thu, 21 Nov 2024 18:13:52 GMT  
		Size: 36.3 KB (36317 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:5-apache` - linux; mips64le

```console
$ docker pull matomo@sha256:1f61524203ad8fed365af677759cde42c472d0b1705cd473a98626f2af97299e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.8 MB (176791591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd2a4fc40291bc9c835ee27e9aa25e57407e86157c0654f9979e9e4ab4c710ab`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 25 Sep 2024 20:44:12 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
CMD ["bash"]
# Wed, 25 Sep 2024 20:44:12 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 25 Sep 2024 20:44:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 25 Sep 2024 20:44:12 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 25 Sep 2024 20:44:12 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 25 Sep 2024 20:44:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 25 Sep 2024 20:44:12 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 25 Sep 2024 20:44:12 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 25 Sep 2024 20:44:12 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 25 Sep 2024 20:44:12 GMT
ENV PHP_VERSION=8.2.25
# Wed, 25 Sep 2024 20:44:12 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.25.tar.xz.asc
# Wed, 25 Sep 2024 20:44:12 GMT
ENV PHP_SHA256=330b54876ea1d05ade12ee9726167332058bccd58dffa1d4e12117f6b4f616b9
# Wed, 25 Sep 2024 20:44:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 25 Sep 2024 20:44:12 GMT
STOPSIGNAL SIGWINCH
# Wed, 25 Sep 2024 20:44:12 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
WORKDIR /var/www/html
# Wed, 25 Sep 2024 20:44:12 GMT
EXPOSE map[80/tcp:{}]
# Wed, 25 Sep 2024 20:44:12 GMT
CMD ["apache2-foreground"]
# Wed, 25 Sep 2024 20:44:12 GMT
ENV PHP_MEMORY_LIMIT=256M
# Wed, 25 Sep 2024 20:44:12 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype-dev 		libjpeg-dev 		libldap2-dev 		libpng-dev 		libzip-dev 		procps 	; 		debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		opcache 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.24; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
ENV MATOMO_VERSION=5.1.2
# Wed, 25 Sep 2024 20:44:12 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends 		$fetchDeps 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
VOLUME [/var/www/html]
# Wed, 25 Sep 2024 20:44:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 25 Sep 2024 20:44:12 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:01c6d0bf10848996e396c89b66742849d41fd852c3610146badf9f612e62945b`  
		Last Modified: Tue, 12 Nov 2024 00:58:28 GMT  
		Size: 29.1 MB (29127365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:346c2177816783e9e289cf3372b166d07be052e7cc48f98690da6b177d62573f`  
		Last Modified: Tue, 12 Nov 2024 04:08:13 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd1c3070cec45196348f83431a430d224d58f2ae29c7f77034387a1da1bba0c0`  
		Last Modified: Tue, 12 Nov 2024 04:08:21 GMT  
		Size: 80.7 MB (80668697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d844fc4b81ddb360a025208b648de202ba45cd9113ce82fcab840d714a113030`  
		Last Modified: Tue, 12 Nov 2024 04:08:13 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3e3ea12fdbbab62c1af26697aefc532fc1af6a277566ab7f8e089e95811ac94`  
		Last Modified: Tue, 12 Nov 2024 04:28:45 GMT  
		Size: 20.1 MB (20069169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0f597baf51a1158f2bd7d1e67492508879d9f10f07022905b867a74f1563dca`  
		Last Modified: Tue, 12 Nov 2024 04:28:43 GMT  
		Size: 440.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1030ffb9a16f20c3ffe986bb80424e63d46a7e47d84a304997b65fbc6efb79e0`  
		Last Modified: Tue, 12 Nov 2024 04:28:43 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28d50a338c4a4762dd9ca62e556ccac8cabb2db396cda812be1d4ac9261be970`  
		Last Modified: Tue, 12 Nov 2024 09:03:21 GMT  
		Size: 12.3 MB (12253005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb0ac8109e1d1708997c2c85ce783eab19979adafdbabf22b569c9a725612297`  
		Last Modified: Tue, 12 Nov 2024 09:03:20 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ffa08f5c60ca3a2db8f20e7bce568cebad9beffd1b15d0b786b28c970389974`  
		Last Modified: Tue, 12 Nov 2024 09:03:21 GMT  
		Size: 10.5 MB (10490904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55683f82e8fdba9821be50995d9c27333453c8cd3b1b1431799f4f30bcf3b588`  
		Last Modified: Tue, 12 Nov 2024 09:03:20 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57b5797d5324a6e9ea751144d5b4239ffdc343219bc8c5902e2f411079074e19`  
		Last Modified: Tue, 12 Nov 2024 09:03:21 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3ecec9a69e862ee3f1f216286f4fa8aadfc3d64108e23ebeadf31c9e7bce1b5`  
		Last Modified: Tue, 12 Nov 2024 09:03:21 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ee10e5140c19b51f6a2670d5caacf8e984e76c3f8bac76040343131d8372f04`  
		Last Modified: Wed, 13 Nov 2024 05:00:10 GMT  
		Size: 2.8 MB (2829867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cb697bbbaac0e8817ddafbdb1187db23a0984a1ce7e2fd3a3b7bd7e1c96bb3e`  
		Last Modified: Wed, 13 Nov 2024 05:00:09 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82885945d0ad84cca12b4834c70aface780ac3574b4334ce750f1ed7ba2eb363`  
		Last Modified: Wed, 13 Nov 2024 05:00:12 GMT  
		Size: 21.3 MB (21345594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bad6dc411851e3d71adcf17c2b4a49c0623cb44f7f60136658e8ca2b0f5d6900`  
		Last Modified: Wed, 13 Nov 2024 05:00:09 GMT  
		Size: 342.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efbee68478368a6922c265cc57bd98ddf4e754e52a27bec2f16695cbae762477`  
		Last Modified: Wed, 13 Nov 2024 05:00:10 GMT  
		Size: 823.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:5-apache` - unknown; unknown

```console
$ docker pull matomo@sha256:c74552cd7b03eb0d8eaf7afbdf87b83cd616a163e96e71337d1bdc1f5eeca7ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.5 KB (36475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a03e1e21c6578b8c66577c6e8b7b0c9e83632723f94d0a7d369aa04c9b2c0ff3`

```dockerfile
```

-	Layers:
	-	`sha256:8f37bb98406fc1101e773db219d18f390df003a26b1a019e3f2afbf5b810cd45`  
		Last Modified: Wed, 13 Nov 2024 05:00:09 GMT  
		Size: 36.5 KB (36475 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:5-apache` - linux; ppc64le

```console
$ docker pull matomo@sha256:9b57139ab1a2584cab9ea77c146ef6ea5954071c9474352637e8aa07ed8048c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.4 MB (206358829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43f01c39eee3d8fe47016374253c091a2b0b9ae18e2e835a27558b5a0b3bf00f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 25 Sep 2024 20:44:12 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
CMD ["bash"]
# Wed, 25 Sep 2024 20:44:12 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 25 Sep 2024 20:44:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 25 Sep 2024 20:44:12 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 25 Sep 2024 20:44:12 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 25 Sep 2024 20:44:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 25 Sep 2024 20:44:12 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 25 Sep 2024 20:44:12 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 25 Sep 2024 20:44:12 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 25 Sep 2024 20:44:12 GMT
ENV PHP_VERSION=8.2.25
# Wed, 25 Sep 2024 20:44:12 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.25.tar.xz.asc
# Wed, 25 Sep 2024 20:44:12 GMT
ENV PHP_SHA256=330b54876ea1d05ade12ee9726167332058bccd58dffa1d4e12117f6b4f616b9
# Wed, 25 Sep 2024 20:44:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 25 Sep 2024 20:44:12 GMT
STOPSIGNAL SIGWINCH
# Wed, 25 Sep 2024 20:44:12 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
WORKDIR /var/www/html
# Wed, 25 Sep 2024 20:44:12 GMT
EXPOSE map[80/tcp:{}]
# Wed, 25 Sep 2024 20:44:12 GMT
CMD ["apache2-foreground"]
# Wed, 25 Sep 2024 20:44:12 GMT
ENV PHP_MEMORY_LIMIT=256M
# Wed, 25 Sep 2024 20:44:12 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype-dev 		libjpeg-dev 		libldap2-dev 		libpng-dev 		libzip-dev 		procps 	; 		debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		opcache 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.24; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
ENV MATOMO_VERSION=5.1.2
# Wed, 25 Sep 2024 20:44:12 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends 		$fetchDeps 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
VOLUME [/var/www/html]
# Wed, 25 Sep 2024 20:44:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 25 Sep 2024 20:44:12 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:75e0ed8549227769329d9bb009b10ff68c47929fad577311f0d99115885347ef`  
		Last Modified: Tue, 12 Nov 2024 00:58:20 GMT  
		Size: 33.1 MB (33125353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b02cceb11c5f92ea5660ac6e0610c26c972c38dae66eeb9d41e3387390540062`  
		Last Modified: Tue, 12 Nov 2024 03:22:53 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c1d6ec9f7f7d2e7f8318e16194758fc58116d42583559cad4394fb117b2d735`  
		Last Modified: Tue, 12 Nov 2024 03:22:56 GMT  
		Size: 103.3 MB (103323960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e883340f45c1d0e36d2a728cca20410ca3254d93c803c062646dc430b8e41e7b`  
		Last Modified: Tue, 12 Nov 2024 03:22:53 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c2155f33ef158a9585945d382ada5e33cc0a6cb3faf942e6f840e0af8c0ef4e`  
		Last Modified: Tue, 12 Nov 2024 03:27:38 GMT  
		Size: 21.3 MB (21308382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69e7c3966720dc0d3b2f38f69d3927be83fe5fbd6d2d6ee5d45e6635cd22825b`  
		Last Modified: Tue, 12 Nov 2024 03:27:37 GMT  
		Size: 435.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6b76c10e03d21d789b97d145b294ce14e9afc78a7624eddb9a1e308056c07b3`  
		Last Modified: Tue, 12 Nov 2024 03:27:37 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2f3d6b5b94bf0aba00dd060df6cc08cbf6605d672478251206d151b0f039f5c`  
		Last Modified: Tue, 12 Nov 2024 05:51:50 GMT  
		Size: 12.3 MB (12254395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b953bb1f54caeeeac6b6c0b9c344c4d4ea88b7f7a2a4280761418ed46c6750`  
		Last Modified: Tue, 12 Nov 2024 05:51:49 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2370f407e506ef638034c515209285f4cf78c57a4e94c6ed3d9781251be6b513`  
		Last Modified: Tue, 12 Nov 2024 05:51:50 GMT  
		Size: 11.8 MB (11826833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db9471a72b72b9030689acfd28cb93fcb7f6f05ca40b1c193b4fff70b47f7ea9`  
		Last Modified: Tue, 12 Nov 2024 05:51:49 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25a4a6a153504d8db2f3e6384dd78cbd990c2fe97cc93e6426387ae19ad7956d`  
		Last Modified: Tue, 12 Nov 2024 05:51:50 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8533b29478ab357c0a26ae2e53e1e1ad8ff7ee87bf8176e3175a9e981f7c5364`  
		Last Modified: Tue, 12 Nov 2024 05:51:50 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6861c6e07ad35cec4dff1d677b3b3971275fdfbff5c0de911f8ba82da34a6eb`  
		Last Modified: Tue, 12 Nov 2024 20:38:26 GMT  
		Size: 3.2 MB (3165790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d30d5be46b736fb6a7a4bd8ff7cee89288ae479d7776d41f3fe67d2446dcdb13`  
		Last Modified: Tue, 12 Nov 2024 20:38:25 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18686ef31779122b7e6f8c42103b8cfa3d9989b7889e6cbe3e4432d1223f4290`  
		Last Modified: Tue, 12 Nov 2024 20:38:27 GMT  
		Size: 21.3 MB (21347146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ec35c696d21be30c1f2866154fbbf59d52cb5f393f83e47cb137ef531bceb2`  
		Last Modified: Tue, 12 Nov 2024 20:38:26 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:245ccdd31436dde2ac0da33601ab6543090f65a083a2d9a9ea3bdf4ea53520a3`  
		Last Modified: Tue, 12 Nov 2024 20:38:27 GMT  
		Size: 823.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:5-apache` - unknown; unknown

```console
$ docker pull matomo@sha256:f05f6360fa8f750f2b65342ffa5ca3ad9daeb202781dbaa7648cb9ea6da5c8a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 KB (36444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aef87b62dd886682d5342e9a4d0027fa8eb3106440cc0f80a8a464b37bba29f7`

```dockerfile
```

-	Layers:
	-	`sha256:8521bcb704c845c648141a184c53b8a7d00b24c968130793e9782e19c41ffba8`  
		Last Modified: Tue, 12 Nov 2024 20:38:25 GMT  
		Size: 36.4 KB (36444 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:5-apache` - linux; s390x

```console
$ docker pull matomo@sha256:f16520afe4817878cd746b0c968667e7c9d0119ab8996436d26bfc78bb435409
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.3 MB (175256979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:152516aca17ca083c5b929c43c0a6e8628ae1da2c7df18b625cb17bf1a5135b2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 25 Sep 2024 20:44:12 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
CMD ["bash"]
# Wed, 25 Sep 2024 20:44:12 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 25 Sep 2024 20:44:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 25 Sep 2024 20:44:12 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 25 Sep 2024 20:44:12 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 25 Sep 2024 20:44:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 25 Sep 2024 20:44:12 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 25 Sep 2024 20:44:12 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 25 Sep 2024 20:44:12 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 25 Sep 2024 20:44:12 GMT
ENV PHP_VERSION=8.2.25
# Wed, 25 Sep 2024 20:44:12 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.25.tar.xz.asc
# Wed, 25 Sep 2024 20:44:12 GMT
ENV PHP_SHA256=330b54876ea1d05ade12ee9726167332058bccd58dffa1d4e12117f6b4f616b9
# Wed, 25 Sep 2024 20:44:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 25 Sep 2024 20:44:12 GMT
STOPSIGNAL SIGWINCH
# Wed, 25 Sep 2024 20:44:12 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
WORKDIR /var/www/html
# Wed, 25 Sep 2024 20:44:12 GMT
EXPOSE map[80/tcp:{}]
# Wed, 25 Sep 2024 20:44:12 GMT
CMD ["apache2-foreground"]
# Wed, 25 Sep 2024 20:44:12 GMT
ENV PHP_MEMORY_LIMIT=256M
# Wed, 25 Sep 2024 20:44:12 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype-dev 		libjpeg-dev 		libldap2-dev 		libpng-dev 		libzip-dev 		procps 	; 		debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		opcache 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.24; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
ENV MATOMO_VERSION=5.1.2
# Wed, 25 Sep 2024 20:44:12 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends 		$fetchDeps 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 25 Sep 2024 20:44:12 GMT
VOLUME [/var/www/html]
# Wed, 25 Sep 2024 20:44:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 25 Sep 2024 20:44:12 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:fa8cb447c1a4d7decc9cbf4223b78597699fc7980d77431c085cd6cf32c5b3ed`  
		Last Modified: Tue, 12 Nov 2024 00:59:17 GMT  
		Size: 27.5 MB (27491628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:557ec8c9288f91e0e914bc88a84e7f99c5caf8f6d9840288a739773c38a7c07a`  
		Last Modified: Tue, 12 Nov 2024 03:15:05 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c26af4e0d7a3fb552ad3968a1cee38ccd36f353e2162832fca3623342e7ab8a`  
		Last Modified: Tue, 12 Nov 2024 03:15:07 GMT  
		Size: 80.8 MB (80817024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36392fa6e835e08d294727ebd2c1c3a2bb6f80d6dc6273a5056d2f6ed2c1ffed`  
		Last Modified: Tue, 12 Nov 2024 03:15:05 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e54e67acbced0cb69e2dc640f712d45dcfa623c348b09bd75ae63c1818f0129f`  
		Last Modified: Tue, 12 Nov 2024 03:20:14 GMT  
		Size: 19.9 MB (19895214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5427c8084a617f516431588d36205b585b6e003a7c6f3326454cc9e4e520946`  
		Last Modified: Tue, 12 Nov 2024 03:20:13 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abd0bc1eddda7a2174cecf32a39f30306b749d6521c2b41823a1b05b41eef6f9`  
		Last Modified: Tue, 12 Nov 2024 03:20:13 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3045792d7daeaa7d40702a0f202dd4f51e513c1910095051fa218af2b912703`  
		Last Modified: Tue, 12 Nov 2024 06:22:13 GMT  
		Size: 12.3 MB (12253536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03580c8e2e52a438759c088b169dddf5c4f5dfe03921ab767b930b5fd13527c5`  
		Last Modified: Tue, 12 Nov 2024 06:22:13 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf8a0d82e5993a8a7e949ce2fba4f13a19cb4d33696f21c8501dfc31055478bc`  
		Last Modified: Tue, 12 Nov 2024 06:22:14 GMT  
		Size: 10.6 MB (10644710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c9953170bd68c9a1d28d8cff26ed13b1e023d89398d3b23d4c34d4965bcad2`  
		Last Modified: Tue, 12 Nov 2024 06:22:13 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82b5ca5b3fb692d59f13a93a6c0f3198b164d597816fcde527bd1538ad39a9a2`  
		Last Modified: Tue, 12 Nov 2024 06:22:14 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3142c1f502be74edfb0f59194ffd1be8da1f810c954117cba27367a3cd9a5329`  
		Last Modified: Tue, 12 Nov 2024 06:22:14 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4225c92536ae2b5a32113e01b53854824047f82c5cdb65d149cb3f2384e2aa6f`  
		Last Modified: Wed, 13 Nov 2024 00:49:26 GMT  
		Size: 2.8 MB (2801770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4398394d59faf8ce40b91809a9d91d0f3a6b8ed056f880412e54ab00109c9ba7`  
		Last Modified: Wed, 13 Nov 2024 00:49:26 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54774de46346b539e22b0e4d32e99abbcf62d15b5972171a7f5e843b8daa3dee`  
		Last Modified: Wed, 13 Nov 2024 00:49:26 GMT  
		Size: 21.3 MB (21346115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c580ab0b704d618dbe0adf764deb89b31ae5afc4d4db1b08d4bd50a8fef2b1b`  
		Last Modified: Wed, 13 Nov 2024 00:49:26 GMT  
		Size: 342.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca8da5d4561e9507386a707f9fd5b28a43fcdedb2d5794f0ff2ceca6ea95870`  
		Last Modified: Wed, 13 Nov 2024 00:49:26 GMT  
		Size: 823.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:5-apache` - unknown; unknown

```console
$ docker pull matomo@sha256:a99da960ed4c9d6c19213f4bb4fe0fafe144221867c463cc7ae0a1b0cf1c2347
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 KB (36367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2587389544e7a386065f091d7154a9fb0034bfff10fdabc84d211d4a86500f0f`

```dockerfile
```

-	Layers:
	-	`sha256:50893e4386441cb73b067ccecbe9ec3e8ed8a6735146866ca719c80efd60ce13`  
		Last Modified: Wed, 13 Nov 2024 00:49:25 GMT  
		Size: 36.4 KB (36367 bytes)  
		MIME: application/vnd.in-toto+json
