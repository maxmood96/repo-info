## `drupal:7-php8.2-apache-bookworm`

```console
$ docker pull drupal@sha256:aa82acd29d69232a3b61e61abaa64e9bfc93b6acb0abe7709f64e4403b7b80cf
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

### `drupal:7-php8.2-apache-bookworm` - linux; amd64

```console
$ docker pull drupal@sha256:28f5a555cc0ac0159e252c02f77336f8af56881a7210590fc06543602f256cc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.1 MB (183083596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad55c3aac347fcb69b93e5ed321bd4bda7eab4d529d0aa022c1f387b3cefc0a4`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 05 Jun 2024 22:17:43 GMT
ADD file:a9a95cfab16803be03e59ade41622ef5061cf90f2d034304fe4ac1ee9ff30389 in / 
# Wed, 05 Jun 2024 22:17:43 GMT
CMD ["bash"]
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 05 Jun 2024 22:17:43 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 05 Jun 2024 22:17:43 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 05 Jun 2024 22:17:43 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 05 Jun 2024 22:17:43 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 05 Jun 2024 22:17:43 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_VERSION=8.2.24
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.24.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.24.tar.xz.asc
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_SHA256=80a5225746a9eb484475b312d4c626c63a88a037d8e56d214f30205e1ba1411a
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 05 Jun 2024 22:17:43 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 05 Jun 2024 22:17:43 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 05 Jun 2024 22:17:43 GMT
RUN docker-php-ext-enable sodium
# Wed, 05 Jun 2024 22:17:43 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 05 Jun 2024 22:17:43 GMT
STOPSIGNAL SIGWINCH
# Wed, 05 Jun 2024 22:17:43 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 05 Jun 2024 22:17:43 GMT
WORKDIR /var/www/html
# Wed, 05 Jun 2024 22:17:43 GMT
EXPOSE 80
# Wed, 05 Jun 2024 22:17:43 GMT
CMD ["apache2-foreground"]
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Jun 2024 22:17:43 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 05 Jun 2024 22:17:43 GMT
ENV DRUPAL_VERSION=7.101
# Wed, 05 Jun 2024 22:17:43 GMT
ENV DRUPAL_URL=https://ftp.drupal.org/files/projects/drupal-7.101.tar.gz
# Wed, 05 Jun 2024 22:17:43 GMT
ENV DRUPAL_MD5=ddcd8cb4e885ae865a3d1a8b06707a67
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	curl -fSL "$DRUPAL_URL" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab`  
		Last Modified: Fri, 27 Sep 2024 04:33:11 GMT  
		Size: 29.1 MB (29126276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07fc0890b857ec241446d5da032bf36da2a006ce8868ba150a76a1ee16772b39`  
		Last Modified: Fri, 27 Sep 2024 07:40:54 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:141aa7d58c576d5efbf995cfdd139044be15add60b2f0e5f7b295fdc4cc511d3`  
		Last Modified: Fri, 27 Sep 2024 07:41:08 GMT  
		Size: 104.3 MB (104345685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2720d4bca8b3db19acbea04618296e463e4cde1df16c277954505ad4e50893eb`  
		Last Modified: Fri, 27 Sep 2024 07:40:54 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82deca51468c5fb0464e6db26d14da0d5605682524cb4acfafbbc7cc55a2b20e`  
		Last Modified: Fri, 27 Sep 2024 07:41:32 GMT  
		Size: 20.3 MB (20327579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dec741dfa52689fcf27c3934a0b87bdaefb62c643d04fe352f88589f791315e9`  
		Last Modified: Fri, 27 Sep 2024 07:41:29 GMT  
		Size: 437.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e204b0efab9499a1608734207890fb199b60d100af89f57dc74f1ca26a00f8d5`  
		Last Modified: Fri, 27 Sep 2024 07:41:29 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a9b8825ee85fc4938aaf820f3caf1223417b94afec555058896f5b22507694b`  
		Last Modified: Fri, 27 Sep 2024 07:47:14 GMT  
		Size: 12.4 MB (12443162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef45e9da2633a738d27d41da1df46c1f67f160743fab61eba2df3a7c35a22289`  
		Last Modified: Fri, 27 Sep 2024 07:47:11 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2b46378d521434bae6da351a128bfab45a8b2231106fd1bd946aa5220eea6a8`  
		Last Modified: Fri, 27 Sep 2024 07:47:13 GMT  
		Size: 11.4 MB (11410499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c104459ddadb2f472d9239c9d997b1f6163c8e5c7307aa24b0e78693c56cd9c`  
		Last Modified: Fri, 27 Sep 2024 07:47:11 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:282db878d4dda03bc59a283134735a2b602fad3e0d969b40d2159a55659cb8d8`  
		Last Modified: Fri, 27 Sep 2024 07:47:12 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a1f827cc210d8b001bc4c20ca2cb4dbc5679cff500d40ff52e89d8bc24c5b20`  
		Last Modified: Fri, 27 Sep 2024 07:47:11 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f127291f260c158dac42a7584a0d0a65b07151effc8013b9ebb75ceb73954ed`  
		Last Modified: Fri, 27 Sep 2024 08:59:14 GMT  
		Size: 2.0 MB (1996896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cef34793ddb4a39af9f8ae98bdbb34644d99314435f829ce7263ebf6bfa5fa3`  
		Last Modified: Fri, 27 Sep 2024 08:59:14 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b63ad0ca3f8bd0fb8ffcb6890d2cee4871b5cd1c2cb2a4846049cc3127b790c`  
		Last Modified: Fri, 27 Sep 2024 08:59:15 GMT  
		Size: 3.4 MB (3427732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.2-apache-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:60aea156c62a81cc29b35738b53f58fec6d309fd699d6d4d8f59cd7818253166
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6789334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68fc40221544fc71be5ac73cd7364167f37e6181f4e2abbf9d87e155e822270d`

```dockerfile
```

-	Layers:
	-	`sha256:0bdf4c79d4c1092f1c1e2544b62fdac6057c580db678acc11e407a60e1692e5b`  
		Last Modified: Fri, 27 Sep 2024 08:59:13 GMT  
		Size: 6.8 MB (6763299 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5786732e7c9713acc43ebf34728fbffbd481a124c528d4f449a3b7b9310b6ff6`  
		Last Modified: Fri, 27 Sep 2024 08:59:13 GMT  
		Size: 26.0 KB (26035 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-php8.2-apache-bookworm` - linux; arm variant v5

```console
$ docker pull drupal@sha256:c77e7591bcfd0eca0649da5ad91cf9874c39c40432e340be1a07cef56e071c46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.2 MB (156246072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bb08720b7f2bc8641770f076bead6f66ec2500ca2d8a833422fa07ec3b36be5`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 05 Jun 2024 22:17:43 GMT
ADD file:91b876c600b7d3198bc98296224f6861440f56fcbd15a2188c95a8785b94061a in / 
# Wed, 05 Jun 2024 22:17:43 GMT
CMD ["bash"]
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 05 Jun 2024 22:17:43 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 05 Jun 2024 22:17:43 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 05 Jun 2024 22:17:43 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 05 Jun 2024 22:17:43 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 05 Jun 2024 22:17:43 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_VERSION=8.2.24
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.24.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.24.tar.xz.asc
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_SHA256=80a5225746a9eb484475b312d4c626c63a88a037d8e56d214f30205e1ba1411a
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 05 Jun 2024 22:17:43 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 05 Jun 2024 22:17:43 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 05 Jun 2024 22:17:43 GMT
RUN docker-php-ext-enable sodium
# Wed, 05 Jun 2024 22:17:43 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 05 Jun 2024 22:17:43 GMT
STOPSIGNAL SIGWINCH
# Wed, 05 Jun 2024 22:17:43 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 05 Jun 2024 22:17:43 GMT
WORKDIR /var/www/html
# Wed, 05 Jun 2024 22:17:43 GMT
EXPOSE 80
# Wed, 05 Jun 2024 22:17:43 GMT
CMD ["apache2-foreground"]
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Jun 2024 22:17:43 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 05 Jun 2024 22:17:43 GMT
ENV DRUPAL_VERSION=7.101
# Wed, 05 Jun 2024 22:17:43 GMT
ENV DRUPAL_URL=https://ftp.drupal.org/files/projects/drupal-7.101.tar.gz
# Wed, 05 Jun 2024 22:17:43 GMT
ENV DRUPAL_MD5=ddcd8cb4e885ae865a3d1a8b06707a67
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	curl -fSL "$DRUPAL_URL" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:75a20c44e8becd141ba586ea413a1649251437a207502d4f8ad23d208f013e60`  
		Last Modified: Fri, 27 Sep 2024 03:21:44 GMT  
		Size: 26.9 MB (26887302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4abee9b0737593e9835dc555292a01c58c3fb19f389ffbb556e3ec83d8222c6`  
		Last Modified: Fri, 27 Sep 2024 04:57:48 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36e5de77c609405dc64f2e8c8206bbec62da53ccc60aedc603672b7a337a412b`  
		Last Modified: Fri, 27 Sep 2024 04:58:03 GMT  
		Size: 82.0 MB (81995092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ddddd6ae7c7fda37305d6bc5117d36ac423f550ff4c6ad424d1de53e6b2a1e0`  
		Last Modified: Fri, 27 Sep 2024 04:57:48 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deccef66bda4d8995be278ceb309f484f6a52595d369da981611dc922e98e887`  
		Last Modified: Fri, 27 Sep 2024 04:58:27 GMT  
		Size: 19.6 MB (19624329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20f63ad9166a15b4f481cc55af64fe92ea1c78d1a77d1d9d16f34bf495afdfae`  
		Last Modified: Fri, 27 Sep 2024 04:58:23 GMT  
		Size: 438.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5517924e644a07b5b6ba20a6189dc63a69c99f73da7e8bdb535bfaccaa37d098`  
		Last Modified: Fri, 27 Sep 2024 04:58:23 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5c677df6d5476e48e4baa887258617c6a7576a325e67648fc267a220d369f54`  
		Last Modified: Fri, 27 Sep 2024 05:01:39 GMT  
		Size: 12.4 MB (12441482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bda9f496be5aa5db0b1d6e3664dd26fe0666eb2a36923852b0868a36fb85d36`  
		Last Modified: Fri, 27 Sep 2024 05:01:36 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e0b7c20e5283235884f774e80308adf04635a2b1feca80c7ce774308998c08d`  
		Last Modified: Fri, 27 Sep 2024 05:01:38 GMT  
		Size: 10.4 MB (10393961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d8ab1b0bf6a03e6e4f110b639f8253e8ed42d8f83384886aef8b2c3c03a9bd`  
		Last Modified: Fri, 27 Sep 2024 05:01:36 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98f7c1756f2245c74a6ba06a4ea90201af8defbdacb29d54cd600763ab088cfe`  
		Last Modified: Fri, 27 Sep 2024 05:01:36 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:954b26bee1c396a1d68f9a9d15f0e1916e6614cf9a064c105c0331fd6b4f9219`  
		Last Modified: Fri, 27 Sep 2024 05:01:36 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dfa3253d9fbe046531c4c8ae42d5f9721f467cd907201f25add20c138d90690`  
		Last Modified: Fri, 27 Sep 2024 06:56:42 GMT  
		Size: 1.5 MB (1470401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4bb1736adde36bd3bb50a95bc2da9268a2ed3ce6b60aa1bc48427bf675140c0`  
		Last Modified: Fri, 27 Sep 2024 06:56:42 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e1980d3e91f2977ddf46ffb3eea63e07990961ac6734cae7c86f4523e0091c`  
		Last Modified: Fri, 27 Sep 2024 06:56:42 GMT  
		Size: 3.4 MB (3427727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.2-apache-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:9e70c0e80c5c4bfeda583e68ab5ae006aff51d1e9a0fde4dd388968c39a75d20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6600827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8635742ba78f860dfd57f4c35a7cf046173faa184748e24a5a2be30de0dbd395`

```dockerfile
```

-	Layers:
	-	`sha256:dc0600b7b457f57b17481b9ad2ad9e5ab2442b3b6b2f47e557e630cf9d42ce63`  
		Last Modified: Fri, 27 Sep 2024 06:56:39 GMT  
		Size: 6.6 MB (6574685 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26ce182e17049cbeb286be44b8e71fb42056ba0cc953c5747d30bbe7ab13d36c`  
		Last Modified: Fri, 27 Sep 2024 06:56:38 GMT  
		Size: 26.1 KB (26142 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-php8.2-apache-bookworm` - linux; arm variant v7

```console
$ docker pull drupal@sha256:ae003d24fc5b6d582425d55f4eefba9b1a968f560a833a85df5c8a7222f25fb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.0 MB (146997525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24005be387992dba413f14385683cfc4a2efac947e10dd49e43fbd5c66f24586`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 05 Jun 2024 22:17:43 GMT
ADD file:7eec8434e7851a0c9296426e66771b108dd584ea08a7e2aaec3ec3077c58bf89 in / 
# Wed, 05 Jun 2024 22:17:43 GMT
CMD ["bash"]
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 05 Jun 2024 22:17:43 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 05 Jun 2024 22:17:43 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 05 Jun 2024 22:17:43 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 05 Jun 2024 22:17:43 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 05 Jun 2024 22:17:43 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_VERSION=8.2.24
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.24.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.24.tar.xz.asc
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_SHA256=80a5225746a9eb484475b312d4c626c63a88a037d8e56d214f30205e1ba1411a
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 05 Jun 2024 22:17:43 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 05 Jun 2024 22:17:43 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 05 Jun 2024 22:17:43 GMT
RUN docker-php-ext-enable sodium
# Wed, 05 Jun 2024 22:17:43 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 05 Jun 2024 22:17:43 GMT
STOPSIGNAL SIGWINCH
# Wed, 05 Jun 2024 22:17:43 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 05 Jun 2024 22:17:43 GMT
WORKDIR /var/www/html
# Wed, 05 Jun 2024 22:17:43 GMT
EXPOSE 80
# Wed, 05 Jun 2024 22:17:43 GMT
CMD ["apache2-foreground"]
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Jun 2024 22:17:43 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 05 Jun 2024 22:17:43 GMT
ENV DRUPAL_VERSION=7.101
# Wed, 05 Jun 2024 22:17:43 GMT
ENV DRUPAL_URL=https://ftp.drupal.org/files/projects/drupal-7.101.tar.gz
# Wed, 05 Jun 2024 22:17:43 GMT
ENV DRUPAL_MD5=ddcd8cb4e885ae865a3d1a8b06707a67
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	curl -fSL "$DRUPAL_URL" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:2136499185ba9023c6db11bbc836b6c428da7969aa7db3ccaac576a10052c9ce`  
		Last Modified: Fri, 27 Sep 2024 05:17:12 GMT  
		Size: 24.7 MB (24718145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71b4b796e3156825c9c7128cd43753f55a7b4846d8bb402dd9a77a8abe211f01`  
		Last Modified: Fri, 27 Sep 2024 07:09:08 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56632fe12bcb53322059eec59ebb6d32be677cd5a7660f8c58dcbae4c842f7f4`  
		Last Modified: Fri, 27 Sep 2024 07:09:25 GMT  
		Size: 76.2 MB (76163133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb66744d163056f62ac800c7c39d0b124a45a20946685aaa7af12a7294b6dd0`  
		Last Modified: Fri, 27 Sep 2024 07:09:08 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ee92f2ee8b075bcd1aeef5d185504ff3e36174d27b571c1d00d251e4aac01f2`  
		Last Modified: Fri, 27 Sep 2024 07:09:50 GMT  
		Size: 19.1 MB (19062052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a43b487640b16be1e8dd3173f866dd400247e62d55fa7a367338223039daed09`  
		Last Modified: Fri, 27 Sep 2024 07:09:47 GMT  
		Size: 439.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63d6909db46b1f42af9fe07c4658e5b551d5f0614c90d2978ebd00ec8d848ef4`  
		Last Modified: Fri, 27 Sep 2024 07:09:47 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ac1fd045a39ba4953541f44d7851fd9b237e55adaeedea075bfe91032734c6c`  
		Last Modified: Fri, 27 Sep 2024 07:15:50 GMT  
		Size: 12.4 MB (12441480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6de6931d84a75584f61b609601c48975c336bc36f0a0521b0b418171309212e`  
		Last Modified: Fri, 27 Sep 2024 07:15:47 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48dc2fb30d7dec3cc4329141d1b25c214b16c99c1c9dbb3c6af56b780c87a77c`  
		Last Modified: Fri, 27 Sep 2024 07:15:50 GMT  
		Size: 9.8 MB (9825870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3981dd0e5135caf2c7aecbe83a4f7b9fc4186f5d9dabb45ca08a53e81bf8782`  
		Last Modified: Fri, 27 Sep 2024 07:15:47 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd176459f376d553b627b1d938e16095194a321ee199af16f8f8a43a20048084`  
		Last Modified: Fri, 27 Sep 2024 07:15:47 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d2e67247d94640f766196e0f61a630acafb24ba54ae54526a29c8d877bc248`  
		Last Modified: Fri, 27 Sep 2024 07:15:47 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa8634946ecb6bc3e841fac3647093be725ed864eefeb2b2cad30534a70f2a27`  
		Last Modified: Fri, 27 Sep 2024 19:16:47 GMT  
		Size: 1.4 MB (1353335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7add9bc79704f26b47a0920c1c4c0694ad6b6f9d6fe773fa69b09ace0e9aa692`  
		Last Modified: Fri, 27 Sep 2024 19:16:47 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7b42137c9d4d81c633699910587f8403200ee27a9af305030a7713d9f8a2b56`  
		Last Modified: Fri, 27 Sep 2024 19:33:33 GMT  
		Size: 3.4 MB (3427733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.2-apache-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:e9f3280643e26be0f20cde9c5c2f4db7ccd21e1d141f25c5754bbe32999b838c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6604810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:519b30a4057f6db2ee0d464a6c60c4747eff304a8911a9eec6508ba9c4a69bac`

```dockerfile
```

-	Layers:
	-	`sha256:4bd4f38cec396507f97c8aa10885ffb02d443be0ef7ded633b656c6cb7360833`  
		Last Modified: Fri, 27 Sep 2024 19:33:32 GMT  
		Size: 6.6 MB (6578671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50c04a18e12561379b3eda84461a7eee2c6164ef22c41c2182ff33d379e3a7d3`  
		Last Modified: Fri, 27 Sep 2024 19:33:32 GMT  
		Size: 26.1 KB (26139 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-php8.2-apache-bookworm` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:e04953ab2dbad9efaee004fd34639b7c82bec0706af3322af6d6b0f66ad5676d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.2 MB (177161288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83e9ba361d65772a2f0bf11adb396af184acbe327bf36f7d76f1a083fd4468cd`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 05 Jun 2024 22:17:43 GMT
ADD file:28df1cb6a6576d40b5226851d0a6a76ffd5d1c94644ee441490b74a90f29f425 in / 
# Wed, 05 Jun 2024 22:17:43 GMT
CMD ["bash"]
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 05 Jun 2024 22:17:43 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 05 Jun 2024 22:17:43 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 05 Jun 2024 22:17:43 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 05 Jun 2024 22:17:43 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 05 Jun 2024 22:17:43 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_VERSION=8.2.24
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.24.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.24.tar.xz.asc
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_SHA256=80a5225746a9eb484475b312d4c626c63a88a037d8e56d214f30205e1ba1411a
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 05 Jun 2024 22:17:43 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 05 Jun 2024 22:17:43 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 05 Jun 2024 22:17:43 GMT
RUN docker-php-ext-enable sodium
# Wed, 05 Jun 2024 22:17:43 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 05 Jun 2024 22:17:43 GMT
STOPSIGNAL SIGWINCH
# Wed, 05 Jun 2024 22:17:43 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 05 Jun 2024 22:17:43 GMT
WORKDIR /var/www/html
# Wed, 05 Jun 2024 22:17:43 GMT
EXPOSE 80
# Wed, 05 Jun 2024 22:17:43 GMT
CMD ["apache2-foreground"]
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Jun 2024 22:17:43 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 05 Jun 2024 22:17:43 GMT
ENV DRUPAL_VERSION=7.101
# Wed, 05 Jun 2024 22:17:43 GMT
ENV DRUPAL_URL=https://ftp.drupal.org/files/projects/drupal-7.101.tar.gz
# Wed, 05 Jun 2024 22:17:43 GMT
ENV DRUPAL_MD5=ddcd8cb4e885ae865a3d1a8b06707a67
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	curl -fSL "$DRUPAL_URL" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:14c9d9d199323cbf0a4c2347a8af85f2875c1f2c26a1558fd34dfca7a26cff22`  
		Last Modified: Fri, 27 Sep 2024 04:40:53 GMT  
		Size: 29.2 MB (29156369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4075a2a900cbcc12ab034169fddf2bcdd894e0953be6ad883c380b275350502`  
		Last Modified: Fri, 27 Sep 2024 07:16:46 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fd31999ed1795da18acdfe1dd60f9dde145223af54a887ef424786e8e885b85`  
		Last Modified: Fri, 27 Sep 2024 07:16:57 GMT  
		Size: 98.1 MB (98130981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:131265d95889b23e897a24b57123c95173e80ddd3d485f561737530371309615`  
		Last Modified: Fri, 27 Sep 2024 07:16:46 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a5d1249bb626a5f47a598928fd07fd4a19ad72531ffba7cc72915271a3ba1d8`  
		Last Modified: Fri, 27 Sep 2024 07:17:20 GMT  
		Size: 20.3 MB (20325543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a5db4ebb80f5842a34d9507b254e11285a6960058a9b8d5a6dcc4673b6167a3`  
		Last Modified: Fri, 27 Sep 2024 07:17:18 GMT  
		Size: 435.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b1b2c6cdce0afc5c6e74c307dde16e25accbd2baad830908593184e9eba9d5d`  
		Last Modified: Fri, 27 Sep 2024 07:17:18 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6809e2f715ec177dbbff79e3215a246b238b8be6fc552cd8163304052389d56d`  
		Last Modified: Fri, 27 Sep 2024 07:22:47 GMT  
		Size: 12.4 MB (12442902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e8ce1d2fb13190d056cca21991ed3b93dade5f0256c936bc73111122b2a0db5`  
		Last Modified: Fri, 27 Sep 2024 07:22:45 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f6f00aafc3aba1e10cf12c5288378abcfe9e3ab2c91afb19c4c49d04f667534`  
		Last Modified: Fri, 27 Sep 2024 07:22:47 GMT  
		Size: 11.4 MB (11417828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1c42fd6a2f0ac25ab85f0e381c2b4b3945389a72179fcba1f35a0e8f19e85e1`  
		Last Modified: Fri, 27 Sep 2024 07:22:45 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c14eb04cdbad42f193a85516eb527e0ca84feca060cb5370cbc74e332a7dcc2`  
		Last Modified: Fri, 27 Sep 2024 07:22:45 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74353b86439842c9b13e968a6b50774677e15759fb0cf22189dc97975efb5f39`  
		Last Modified: Fri, 27 Sep 2024 07:22:45 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37ac31ca535d8db783d51448243dc1afb5422fb96c19f58a7883f457826c047a`  
		Last Modified: Fri, 27 Sep 2024 10:58:06 GMT  
		Size: 2.3 MB (2254169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dca844a4ce665eb7865e3c38f4840c3f22ff97aaf507840434cd56fbf787463`  
		Last Modified: Fri, 27 Sep 2024 10:58:06 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f642b80720724abf1ccf20a298ce5b21bbf14ab3eb2385a0b7ccb556e198c25f`  
		Last Modified: Fri, 27 Sep 2024 10:58:07 GMT  
		Size: 3.4 MB (3427726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.2-apache-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:ae957f9f4e9eeaa07d0878f97707cb0d27614290e8f398fcb29a6218f30068b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6818134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18b5a6d16430c756f2d12ccbab7bd453e64dc2227e7d79eabd5bdfea0db81565`

```dockerfile
```

-	Layers:
	-	`sha256:3179072fe9130d2d21049720bbff550cfee69eaaa4ed12926d4fee8c5690a860`  
		Last Modified: Fri, 27 Sep 2024 10:58:05 GMT  
		Size: 6.8 MB (6791767 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c0e000341ce064412d21399a92a05187118df716d0fd7acfdfd13509cba8bc3`  
		Last Modified: Fri, 27 Sep 2024 10:58:04 GMT  
		Size: 26.4 KB (26367 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-php8.2-apache-bookworm` - linux; 386

```console
$ docker pull drupal@sha256:94ab04c0a2994d68cfda538a8ba10e936381689754809bbed9935feb44931819
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.1 MB (182067533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:315c12f31b40d06a8382f14ed1b094f14f4d7c8b2623e9ccba172698578e5809`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 05 Jun 2024 22:17:43 GMT
ADD file:7ad74dd13b6c84de2920c6d09de06e914d0b78ba06ae75260d6e6ff344a4b024 in / 
# Wed, 05 Jun 2024 22:17:43 GMT
CMD ["bash"]
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 05 Jun 2024 22:17:43 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 05 Jun 2024 22:17:43 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 05 Jun 2024 22:17:43 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 05 Jun 2024 22:17:43 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 05 Jun 2024 22:17:43 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_VERSION=8.2.24
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.24.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.24.tar.xz.asc
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_SHA256=80a5225746a9eb484475b312d4c626c63a88a037d8e56d214f30205e1ba1411a
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 05 Jun 2024 22:17:43 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 05 Jun 2024 22:17:43 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 05 Jun 2024 22:17:43 GMT
RUN docker-php-ext-enable sodium
# Wed, 05 Jun 2024 22:17:43 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 05 Jun 2024 22:17:43 GMT
STOPSIGNAL SIGWINCH
# Wed, 05 Jun 2024 22:17:43 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 05 Jun 2024 22:17:43 GMT
WORKDIR /var/www/html
# Wed, 05 Jun 2024 22:17:43 GMT
EXPOSE 80
# Wed, 05 Jun 2024 22:17:43 GMT
CMD ["apache2-foreground"]
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Jun 2024 22:17:43 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 05 Jun 2024 22:17:43 GMT
ENV DRUPAL_VERSION=7.101
# Wed, 05 Jun 2024 22:17:43 GMT
ENV DRUPAL_URL=https://ftp.drupal.org/files/projects/drupal-7.101.tar.gz
# Wed, 05 Jun 2024 22:17:43 GMT
ENV DRUPAL_MD5=ddcd8cb4e885ae865a3d1a8b06707a67
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	curl -fSL "$DRUPAL_URL" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:c953524ed27d53ce5e7d4e7487137789de73f4058e96b05284eefbcae1b47c26`  
		Last Modified: Fri, 27 Sep 2024 07:27:04 GMT  
		Size: 30.1 MB (30144216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:138795898cf1de35ac46bb272c1c2476a14caa25663387836c955b1d89e2f74e`  
		Last Modified: Fri, 27 Sep 2024 11:31:40 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ec2d8cda04ca38232896364bf367b18146c275503f43c81e6298173cc87253`  
		Last Modified: Fri, 27 Sep 2024 11:32:02 GMT  
		Size: 101.5 MB (101514377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b02e654bcb676bf538ed8701ea1e8b582043bd3457c58bfc84a0010d5d901176`  
		Last Modified: Fri, 27 Sep 2024 11:31:39 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ee4662d7837b680b2cf24f465f80bcef0300f1ec9bbb06e018c3978e371c90e`  
		Last Modified: Fri, 27 Sep 2024 11:32:30 GMT  
		Size: 20.8 MB (20842963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:615b9307c3c3e45c2cfbb1dd17c4ff6c4be3f73f822dd0da5db7f24a3821eae7`  
		Last Modified: Fri, 27 Sep 2024 11:32:24 GMT  
		Size: 437.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef1d934e341d81156439ae04b7ad4f0a24a93ed31030a9ca4125ebd8a4745c0d`  
		Last Modified: Fri, 27 Sep 2024 11:32:24 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:561f13185c087a79fc530e0ed7eeb43c9b00ba108a72cbbf8d847e436496c928`  
		Last Modified: Fri, 27 Sep 2024 11:38:59 GMT  
		Size: 12.4 MB (12442433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9ee77d2867650f5d0ee395cf3eab6fc4d26bf5668c4c4e39fc8d829070e5c55`  
		Last Modified: Fri, 27 Sep 2024 11:38:56 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d93e05390b3f91a4033a82c8f3866f29637272b66a4f744e92fe1764a87ebbcc`  
		Last Modified: Fri, 27 Sep 2024 11:38:59 GMT  
		Size: 11.6 MB (11641448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b384193b4d1845259a0626f62d93e5f4aca43c4963dcf826fbc2ba5f9c9a0463`  
		Last Modified: Fri, 27 Sep 2024 11:38:56 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10fc2478faa41313a1772a12469ae15c448e29f5bd6ca8dbdd47903438603be0`  
		Last Modified: Fri, 27 Sep 2024 11:38:56 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:937f269e68890d4e8fe8aec1c6482b95a6b6a9e80f584a55bb88e200c7bff387`  
		Last Modified: Fri, 27 Sep 2024 11:38:56 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:486cb3e9c695adf98e2a62af86678aea1a98bc051190893582f9bab61c193237`  
		Last Modified: Fri, 27 Sep 2024 12:58:09 GMT  
		Size: 2.0 MB (2048614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fcba8cf6ffb51775889ee3124e1ea0501f78e1ecaa82d8924eddd2147925bbf`  
		Last Modified: Fri, 27 Sep 2024 12:58:09 GMT  
		Size: 309.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b356d1b6d9512ddf40a4c28065f8cbc7881e081c211c1d992f9dbe06a28460b4`  
		Last Modified: Fri, 27 Sep 2024 12:58:09 GMT  
		Size: 3.4 MB (3427721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.2-apache-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:364318128ff1c9a869b1503184a46cc2ba5107fcb5765374700ed6bc734029a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6769752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1053f806b658dbd8b78dd87d9a18a583ce9c97f2dd9e1707e82fb74184bfbc1`

```dockerfile
```

-	Layers:
	-	`sha256:a6a5df3df20199beedd344e91bc85c139599ffdc83dd5592720efecc31eaab3a`  
		Last Modified: Fri, 27 Sep 2024 12:58:07 GMT  
		Size: 6.7 MB (6743761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d71395a17c90f58c5c9d0b538e07ca290c483ed119cd6080c68a191243419de7`  
		Last Modified: Fri, 27 Sep 2024 12:58:07 GMT  
		Size: 26.0 KB (25991 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-php8.2-apache-bookworm` - linux; mips64le

```console
$ docker pull drupal@sha256:d0fd7432ec25c5df6983a48bcf28666a9408e281d9056e139f9551171c79d542
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.6 MB (157594997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11438343c9312dab4f3454be24a193a0660819ab685ecf19c7641e5ad8531e30`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 05 Jun 2024 22:17:43 GMT
ADD file:673970f358f62b6b095139e9647b41b9af839d4e01f7698755b040f471ff80b2 in / 
# Wed, 05 Jun 2024 22:17:43 GMT
CMD ["bash"]
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 05 Jun 2024 22:17:43 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 05 Jun 2024 22:17:43 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 05 Jun 2024 22:17:43 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 05 Jun 2024 22:17:43 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 05 Jun 2024 22:17:43 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_VERSION=8.2.24
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.24.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.24.tar.xz.asc
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_SHA256=80a5225746a9eb484475b312d4c626c63a88a037d8e56d214f30205e1ba1411a
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 05 Jun 2024 22:17:43 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 05 Jun 2024 22:17:43 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 05 Jun 2024 22:17:43 GMT
RUN docker-php-ext-enable sodium
# Wed, 05 Jun 2024 22:17:43 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 05 Jun 2024 22:17:43 GMT
STOPSIGNAL SIGWINCH
# Wed, 05 Jun 2024 22:17:43 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 05 Jun 2024 22:17:43 GMT
WORKDIR /var/www/html
# Wed, 05 Jun 2024 22:17:43 GMT
EXPOSE 80
# Wed, 05 Jun 2024 22:17:43 GMT
CMD ["apache2-foreground"]
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Jun 2024 22:17:43 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 05 Jun 2024 22:17:43 GMT
ENV DRUPAL_VERSION=7.101
# Wed, 05 Jun 2024 22:17:43 GMT
ENV DRUPAL_URL=https://ftp.drupal.org/files/projects/drupal-7.101.tar.gz
# Wed, 05 Jun 2024 22:17:43 GMT
ENV DRUPAL_MD5=ddcd8cb4e885ae865a3d1a8b06707a67
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	curl -fSL "$DRUPAL_URL" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:75358c79454e0fed44aa25dd323536443b4a1230fc432aa226620e470d72cf5f`  
		Last Modified: Fri, 27 Sep 2024 09:11:36 GMT  
		Size: 29.1 MB (29124858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af5bc07367e99f8b3d37849edf8598b8b8dc860c49d5da934eca00acc807d99`  
		Last Modified: Fri, 27 Sep 2024 15:41:03 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4eca0e563a9f07292b1663ae5dfa7c783cbc0a92a6ba5d05b288972fb04e775`  
		Last Modified: Fri, 27 Sep 2024 15:42:01 GMT  
		Size: 80.7 MB (80667686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9156dcf9823554c8d34a92fdc097bd66f5c019cd7aaf13a36ad10f26246aefa`  
		Last Modified: Fri, 27 Sep 2024 15:41:03 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf2b3b50cb0cb73e94fc9bacab2655b94a7220edded2a4c7eaf3e8eb5045dc3`  
		Last Modified: Fri, 27 Sep 2024 15:42:41 GMT  
		Size: 20.1 MB (20069201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f49bc3e7d6cb95e2d77d06f2542a1a0512de39fede06dd9c8ec8e9d9a338b8`  
		Last Modified: Fri, 27 Sep 2024 15:42:27 GMT  
		Size: 438.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c71ff0ef306529b5f488b2a07fc5fc7891371b193a282d1187bd2a49c611643`  
		Last Modified: Fri, 27 Sep 2024 15:42:27 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33a1dab5712653a28b10e0435e259e202af62c9245787d05d3abd6978c36f598`  
		Last Modified: Fri, 27 Sep 2024 15:48:09 GMT  
		Size: 12.2 MB (12236930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2afce32a004eae5dc0f51f7d68837223fa4ef1d32638140750c7facc6057d19c`  
		Last Modified: Fri, 27 Sep 2024 15:48:03 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5f89be47e5116a194cb3455bfde6f64f74e95dbfb76bfb869c9b3bbe4360577`  
		Last Modified: Fri, 27 Sep 2024 15:48:11 GMT  
		Size: 10.5 MB (10491820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09bc8584e7c8ea7aeacbb8fb434ad624134b4f489a185c408d29ed940bbe6668`  
		Last Modified: Fri, 27 Sep 2024 15:48:03 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d420f4e05dcb35264dd5056cb9de713c77d70e09e22b2ae94f99bf53016efa5`  
		Last Modified: Fri, 27 Sep 2024 15:48:03 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f7e8becea9a241d0a65cf5513f3f192c4df1e2355261181f9760af77dfc23be`  
		Last Modified: Fri, 27 Sep 2024 15:48:03 GMT  
		Size: 895.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f40e74249c29f15747baed3f4ec5212a0e9a8087a3cf257a5d5a1bb827da42e`  
		Last Modified: Sat, 28 Sep 2024 12:58:20 GMT  
		Size: 1.6 MB (1570996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4824cd8943cd2b6f937432783bd832b9eabd7f0d60b1c97a9c40c9449999a25a`  
		Last Modified: Sat, 28 Sep 2024 12:58:19 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96da4440877a0099b7f639bb31516bef5e8a3bad661755ddc665cdbbaa350360`  
		Last Modified: Sat, 28 Sep 2024 12:58:20 GMT  
		Size: 3.4 MB (3427728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.2-apache-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:f8a2f71614859b15049876d726d209bd36801722c6a05dd2cd3ef3a8fe3c5395
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:102f0aeba02608acba717fab456fa54102e916bceb6b2e8a34d199ede0cc5d54`

```dockerfile
```

-	Layers:
	-	`sha256:e6cc2e1712bf1923aa13175ade956b47f42383e729ed522fb6061c51597b342e`  
		Last Modified: Sat, 28 Sep 2024 12:58:14 GMT  
		Size: 25.9 KB (25893 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-php8.2-apache-bookworm` - linux; ppc64le

```console
$ docker pull drupal@sha256:ccb053e4b9e44a53652d6c6d1993799736ed63bbc1ae4e569e7bd660c32f810d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.5 MB (187518977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99a1b14ea8a5b1040dc9235ef6cc2b8531e18de9d7b841c7fe1ec2e9accb0d3b`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 05 Jun 2024 22:17:43 GMT
ADD file:13ecda46acf717bc6e96c8ad429d6c14016514befca636a168655d0e5c9c4fbd in / 
# Wed, 05 Jun 2024 22:17:43 GMT
CMD ["bash"]
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 05 Jun 2024 22:17:43 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 05 Jun 2024 22:17:43 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 05 Jun 2024 22:17:43 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 05 Jun 2024 22:17:43 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 05 Jun 2024 22:17:43 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_VERSION=8.2.24
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.24.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.24.tar.xz.asc
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_SHA256=80a5225746a9eb484475b312d4c626c63a88a037d8e56d214f30205e1ba1411a
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 05 Jun 2024 22:17:43 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 05 Jun 2024 22:17:43 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 05 Jun 2024 22:17:43 GMT
RUN docker-php-ext-enable sodium
# Wed, 05 Jun 2024 22:17:43 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 05 Jun 2024 22:17:43 GMT
STOPSIGNAL SIGWINCH
# Wed, 05 Jun 2024 22:17:43 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 05 Jun 2024 22:17:43 GMT
WORKDIR /var/www/html
# Wed, 05 Jun 2024 22:17:43 GMT
EXPOSE 80
# Wed, 05 Jun 2024 22:17:43 GMT
CMD ["apache2-foreground"]
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Jun 2024 22:17:43 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 05 Jun 2024 22:17:43 GMT
ENV DRUPAL_VERSION=7.101
# Wed, 05 Jun 2024 22:17:43 GMT
ENV DRUPAL_URL=https://ftp.drupal.org/files/projects/drupal-7.101.tar.gz
# Wed, 05 Jun 2024 22:17:43 GMT
ENV DRUPAL_MD5=ddcd8cb4e885ae865a3d1a8b06707a67
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	curl -fSL "$DRUPAL_URL" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:c0db683897d16fe6e2869a351dbd5deac2268d5820d4b3c1cf93ec3bd69cafb5`  
		Last Modified: Fri, 27 Sep 2024 05:36:18 GMT  
		Size: 33.1 MB (33122163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bbb4ae861a643bc7004f9327fc7d89ac6f4ea4f5a77bfded69b88f585ea01e1`  
		Last Modified: Fri, 27 Sep 2024 07:02:41 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc16434a3ca8eec5c8933adec752fafcba89db0a65fc61746120478da09bca93`  
		Last Modified: Fri, 27 Sep 2024 07:02:58 GMT  
		Size: 103.3 MB (103326181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2051474fc72a079e1611119dde76deefb71f3b4b15e86c02c8e21198bcb9f249`  
		Last Modified: Fri, 27 Sep 2024 07:02:41 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e9589061db86204e594c406f6de20b8e8bc40c3bc4fbdff0ddcaf22b3253078`  
		Last Modified: Fri, 27 Sep 2024 07:03:25 GMT  
		Size: 21.5 MB (21511855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5201482f538d84823d22ea42aeaa4b071c48bc6693b7862c0a79bf390d689b6`  
		Last Modified: Fri, 27 Sep 2024 07:03:21 GMT  
		Size: 433.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2843dcc1fb30cdbf957b3c7273818bd5877c32b4dc91f2273111780f4eaae30b`  
		Last Modified: Fri, 27 Sep 2024 07:03:21 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d813628e013d7663e39adf1ebd1323cdd11b3c58a30a372f18d8eee63ed9e11`  
		Last Modified: Fri, 27 Sep 2024 07:07:19 GMT  
		Size: 12.4 MB (12442624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da6ae47d185ea74c696277a67f5e63bb39534b357e65564077b76db6d1c07371`  
		Last Modified: Fri, 27 Sep 2024 07:07:15 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9316162bc4d4f6a7fed0124b136ecd79bf288a5cd93f3fc82154167d7ffa5ff`  
		Last Modified: Fri, 27 Sep 2024 07:07:18 GMT  
		Size: 11.8 MB (11827343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97c5532898e7467372ef63509025ac2d7c86a310cb1c996b9679b4eef402dd83`  
		Last Modified: Fri, 27 Sep 2024 07:07:15 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f778f01f7fc101b62e9cb120708767d6e085b5958447266e42fd647972d90ce`  
		Last Modified: Fri, 27 Sep 2024 07:07:15 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beac6a6fe43d79c33a4bc98ab536ac2aa2ae7ac0f0dde11522778062b2252340`  
		Last Modified: Fri, 27 Sep 2024 07:07:15 GMT  
		Size: 895.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2907c2e0635c805721a7b6832fa8830afc71500a6cdbd327f71baaa343a30c8`  
		Last Modified: Fri, 27 Sep 2024 10:11:57 GMT  
		Size: 1.9 MB (1855316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:849de05b83f566b21991803727cbdcb0cfe277c7b72c8f2a2cf2b4e8a0d9dbfb`  
		Last Modified: Fri, 27 Sep 2024 10:11:56 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddf82b9576c197fbdc508601c0034b19461fc81b40e53781706e5ad45b3e3476`  
		Last Modified: Fri, 27 Sep 2024 13:31:49 GMT  
		Size: 3.4 MB (3427722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.2-apache-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:b420435b2339df4a0119b2496e6fb793c44fe8711ffad9e7c3baf7a518c98e28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6766556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6147748107560073d0b513685d6f5ec0377354b4b9b0074a2a17e0956b410f8a`

```dockerfile
```

-	Layers:
	-	`sha256:28e7cecad99bacda970c92643f24ac62680094975d23139888613bfed1e86998`  
		Last Modified: Fri, 27 Sep 2024 13:31:49 GMT  
		Size: 6.7 MB (6740467 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e8db6a0e8021b4e0306ca8414f64668d0bb252c8c5b4a22957556e9f5788ff5`  
		Last Modified: Fri, 27 Sep 2024 13:31:48 GMT  
		Size: 26.1 KB (26089 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-php8.2-apache-bookworm` - linux; s390x

```console
$ docker pull drupal@sha256:f79c626e1461b57b795ab9e02e9ccaa7415a2ec19118c26f7a7cf21bde392493
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156479384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4812291a7134f2c58d3169c7022aa3f7d578d9205910e4eb7de5e7ee63aad70e`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 05 Jun 2024 22:17:43 GMT
ADD file:ee3c94adee604dbcaddf5d6c372b1f325a4443f66bd717dedf1ff7d9fb1ba116 in / 
# Wed, 05 Jun 2024 22:17:43 GMT
CMD ["bash"]
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 05 Jun 2024 22:17:43 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 05 Jun 2024 22:17:43 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 05 Jun 2024 22:17:43 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 05 Jun 2024 22:17:43 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 05 Jun 2024 22:17:43 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_VERSION=8.2.24
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.24.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.24.tar.xz.asc
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_SHA256=80a5225746a9eb484475b312d4c626c63a88a037d8e56d214f30205e1ba1411a
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 05 Jun 2024 22:17:43 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 05 Jun 2024 22:17:43 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 05 Jun 2024 22:17:43 GMT
RUN docker-php-ext-enable sodium
# Wed, 05 Jun 2024 22:17:43 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 05 Jun 2024 22:17:43 GMT
STOPSIGNAL SIGWINCH
# Wed, 05 Jun 2024 22:17:43 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 05 Jun 2024 22:17:43 GMT
WORKDIR /var/www/html
# Wed, 05 Jun 2024 22:17:43 GMT
EXPOSE 80
# Wed, 05 Jun 2024 22:17:43 GMT
CMD ["apache2-foreground"]
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Jun 2024 22:17:43 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 05 Jun 2024 22:17:43 GMT
ENV DRUPAL_VERSION=7.101
# Wed, 05 Jun 2024 22:17:43 GMT
ENV DRUPAL_URL=https://ftp.drupal.org/files/projects/drupal-7.101.tar.gz
# Wed, 05 Jun 2024 22:17:43 GMT
ENV DRUPAL_MD5=ddcd8cb4e885ae865a3d1a8b06707a67
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	curl -fSL "$DRUPAL_URL" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:eca1e192de25fb56826ff7ed14b2e1532a49c27a08147a6249506eafd8ab4472`  
		Last Modified: Fri, 27 Sep 2024 02:47:22 GMT  
		Size: 27.5 MB (27490024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:263aaad988f988011e1356f427631505912e90651f05e9b8127e438710e3424d`  
		Last Modified: Fri, 27 Sep 2024 04:18:13 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fe6bbb4a2c701c2e428aa64af29de71f25f3955f023abedbd742ba882d648c4`  
		Last Modified: Fri, 27 Sep 2024 04:18:25 GMT  
		Size: 80.8 MB (80817788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d56dc43f4c20142326de61889c1d809b383f6aee30517f4872c80305147c993`  
		Last Modified: Fri, 27 Sep 2024 04:18:13 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c52c41590c8426047a15f1969a92ae4add1c9047e56460d92a094cd534bd822`  
		Last Modified: Fri, 27 Sep 2024 04:18:41 GMT  
		Size: 20.1 MB (20099019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0050a91c477b0c2256727ec363cb8333b14cd8993f235bf2e788825fea5ba66`  
		Last Modified: Fri, 27 Sep 2024 04:18:38 GMT  
		Size: 434.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baed063e13cf0353d5655d6198ed7df04fdaeb730279a099f051e683ada2311f`  
		Last Modified: Fri, 27 Sep 2024 04:18:38 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:245b009057a3c847137ba2e2e4012150b891e8db01823a6edd44f831a8a18f65`  
		Last Modified: Fri, 27 Sep 2024 04:21:15 GMT  
		Size: 12.4 MB (12441770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2844dd1ced33ed2075394f94731f7aa0ad263e992bf7dbc0a3f643c2ec4a6fd`  
		Last Modified: Fri, 27 Sep 2024 04:21:13 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f8158b01ff9b6e0fa7aa2f1ee7ac08c7a452b62cca10a417fdc051510b9666e`  
		Last Modified: Fri, 27 Sep 2024 04:21:15 GMT  
		Size: 10.6 MB (10644674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c7a4c8366b9700dbadc776b31d7362bdb4017c6222d6c9a76f35fe9e801f07d`  
		Last Modified: Fri, 27 Sep 2024 04:21:13 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b8725b76676d868f065476a88cc34d82a84d3ca056bb80bb4f82da322142976`  
		Last Modified: Fri, 27 Sep 2024 04:21:13 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9849ccdf4f53873810b66a3d5b59d4b773a8a3a2f21b83ca53235f17ef6c4276`  
		Last Modified: Fri, 27 Sep 2024 04:21:13 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdca0697cae0b512406289a694cd5ed9a409ae1a21479047964568ce56691ea8`  
		Last Modified: Fri, 27 Sep 2024 06:25:13 GMT  
		Size: 1.6 MB (1552618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe4489da65c81b17020ec2fdbd2f338931a612cf81cc7b2be92a0377ed4f9737`  
		Last Modified: Fri, 27 Sep 2024 06:25:14 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22d1469cf29e9e87df86df0b252e6f17a556d03b5ad5eec9dfa173b28916b4b2`  
		Last Modified: Fri, 27 Sep 2024 06:43:27 GMT  
		Size: 3.4 MB (3427727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.2-apache-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:ccb4871998dfe5dd656cb973e5e7a7955c8f52e8f501e3cd019cfac3936f0584
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6631180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bec548dd746d13f66f3b331a1586bc865756883797a52ed1407839d5da883e8`

```dockerfile
```

-	Layers:
	-	`sha256:9b3bf15bbedcec2f0b9050459453e6eb221773f3681734f1b26a4ddb2baad4ce`  
		Last Modified: Fri, 27 Sep 2024 06:43:27 GMT  
		Size: 6.6 MB (6605149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55d24de085f89076f6faf9c7c1ce540eb3defcd2d3b86a633a6714a3ffb540b4`  
		Last Modified: Fri, 27 Sep 2024 06:43:26 GMT  
		Size: 26.0 KB (26031 bytes)  
		MIME: application/vnd.in-toto+json
