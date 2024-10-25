## `yourls:latest`

```console
$ docker pull yourls@sha256:237a79ef444b94349b8352fc7a33f5eefd7fba43463185b9ed343a303d3832ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `yourls:latest` - linux; amd64

```console
$ docker pull yourls@sha256:d76fe92bc4df42b269974c6784da5ccad980d0af43ecf13489fa96834cd555e7
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.9 MB (182882138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fadc99eadc0647e260f6a18dc408d1a9701da8fb4cfc7b08549b2135826ef3d`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 17 Oct 2024 00:20:29 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Thu, 17 Oct 2024 00:20:30 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:17:27 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 17 Oct 2024 01:17:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 17 Oct 2024 01:17:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 01:17:45 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 17 Oct 2024 01:17:46 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 17 Oct 2024 01:21:50 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 17 Oct 2024 01:21:50 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 17 Oct 2024 01:21:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Thu, 17 Oct 2024 01:21:59 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Thu, 17 Oct 2024 01:22:00 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Thu, 17 Oct 2024 01:22:00 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Oct 2024 01:22:00 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Oct 2024 01:22:00 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 17 Oct 2024 01:52:33 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 17 Oct 2024 02:22:46 GMT
ENV PHP_VERSION=8.3.12
# Thu, 17 Oct 2024 02:22:46 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.12.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.12.tar.xz.asc
# Thu, 17 Oct 2024 02:22:46 GMT
ENV PHP_SHA256=f774e28633e26fc8c5197f4dae58ec9e3ff87d1b4311cbc61ab05a7ad24bd131
# Thu, 17 Oct 2024 02:22:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 17 Oct 2024 02:22:56 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 17 Oct 2024 02:26:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 17 Oct 2024 02:26:36 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Thu, 17 Oct 2024 02:26:37 GMT
RUN docker-php-ext-enable sodium
# Thu, 17 Oct 2024 02:26:37 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 17 Oct 2024 02:26:37 GMT
STOPSIGNAL SIGWINCH
# Thu, 17 Oct 2024 02:26:37 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 17 Oct 2024 02:26:37 GMT
WORKDIR /var/www/html
# Thu, 17 Oct 2024 02:26:38 GMT
EXPOSE 80
# Thu, 17 Oct 2024 02:26:38 GMT
CMD ["apache2-foreground"]
# Thu, 17 Oct 2024 07:01:01 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli
# Thu, 17 Oct 2024 07:01:01 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Thu, 17 Oct 2024 07:01:02 GMT
RUN a2enmod rewrite expires
# Thu, 17 Oct 2024 07:01:02 GMT
ARG YOURLS_VERSION=1.9.2
# Thu, 17 Oct 2024 07:01:02 GMT
ARG YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
# Thu, 17 Oct 2024 07:01:02 GMT
ENV YOURLS_VERSION=1.9.2
# Thu, 17 Oct 2024 07:01:03 GMT
ENV YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
# Thu, 17 Oct 2024 07:01:04 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Thu, 17 Oct 2024 07:01:05 GMT
COPY --chown=www-data:www-datafile:407fa98e3948ea07c2ff8bc30ad1b3b7b28a1c2b9b5d8e5ab87f9b317a2bac85 in /usr/src/yourls/user/ 
# Thu, 17 Oct 2024 07:01:05 GMT
COPY file:50b4d483341578e719ad63fd7aaea99a0d6d7cebfb7b43d6098a656a975ee0e3 in /usr/local/bin/ 
# Thu, 17 Oct 2024 07:01:05 GMT
COPY file:5b7ff05d0c98ad759c4bec0ef8a7ce74cae42e95b42564b55f43b341c2c3e3f5 in /usr/src/yourls/ 
# Thu, 17 Oct 2024 07:01:05 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Thu, 17 Oct 2024 07:01:05 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95ab1cc5ca33d8382a34578c5ac4fec4d1f4a381d747e3c9d2e8fd8bdc20b621`  
		Last Modified: Thu, 17 Oct 2024 04:18:59 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78ee5e1490ca9e76fb6078eb2581366decdceea48fa3e65583e2c80e10522849`  
		Last Modified: Thu, 17 Oct 2024 04:19:14 GMT  
		Size: 104.3 MB (104346971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e807ae4973d0b87fd52b4704132912240c54d7c5110dabfbd3e5032ca5249eec`  
		Last Modified: Thu, 17 Oct 2024 04:18:58 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a1846dfbe9adb998f8c506143dfcf02b7dee1b6b39ba6746202c87e2f3e41ff`  
		Last Modified: Thu, 17 Oct 2024 04:19:36 GMT  
		Size: 20.3 MB (20327779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27f1d0bbde8147dd947d4227d005cf449ab44cfefebf706b899000054185f9d7`  
		Last Modified: Thu, 17 Oct 2024 04:19:33 GMT  
		Size: 435.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fac5e585cd612eddd957e7c3edb4712bfabc4f504eb4a72e6dc5088776b51b0`  
		Last Modified: Thu, 17 Oct 2024 04:19:33 GMT  
		Size: 488.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a40b76f0a3f6708fe595f76bfc20f4c0c3386c39bacb44dae4a2d971ce83e706`  
		Last Modified: Thu, 17 Oct 2024 04:24:08 GMT  
		Size: 12.8 MB (12826903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77d531355483bd424851b38b0c85ae5c791a8955d74d6b7b09cadded20d79e37`  
		Last Modified: Thu, 17 Oct 2024 04:24:05 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4258870bf03446a12b4d3a85feb229f72d289cd4e8a8d8524c80c5f41a9eaafd`  
		Last Modified: Thu, 17 Oct 2024 04:24:07 GMT  
		Size: 11.6 MB (11644338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95a15750412b982666d918ab4ccada074414fe2afe3444fbb6e18b614bedb66`  
		Last Modified: Thu, 17 Oct 2024 04:24:05 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ed1ec2f8aa8102f199a93e5ad84171270a291a638b2859ec14b53112cce83fb`  
		Last Modified: Thu, 17 Oct 2024 04:24:05 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:418fb56ff4057895e8018012665e170931c27f3dd362d73ad4be5c95ebac69d1`  
		Last Modified: Thu, 17 Oct 2024 04:24:05 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da7ed1f4d91b09bdf4080b5bed63e65bfe004ad7d21e47700ced785763f033d8`  
		Last Modified: Thu, 17 Oct 2024 07:02:16 GMT  
		Size: 526.2 KB (526217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b00ad0d4490cb35c8f52cfa643adcfb5cf11f3454cae35d4f0e3e48b92f2819f`  
		Last Modified: Thu, 17 Oct 2024 07:02:16 GMT  
		Size: 324.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:966141e1a485fb7ce92b64dbf4b7aa2464184abc5db46a2bbdb1dabeebe24d2f`  
		Last Modified: Thu, 17 Oct 2024 07:02:14 GMT  
		Size: 346.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a116e28b5a5e8e20f0f798f1f0d49a9f97d56e3bd979d23c382f287bbcfef1a`  
		Last Modified: Thu, 17 Oct 2024 07:02:15 GMT  
		Size: 4.1 MB (4073440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca6c4d9a845bd9f35635de73c027ec37320620eb6bdf0da6b506fb06dc973ff5`  
		Last Modified: Thu, 17 Oct 2024 07:02:14 GMT  
		Size: 2.0 KB (2047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31ccde7b9d9c5e3d45493b2bb829ce4d8ba124724fb22399063d3c7e1c7384e3`  
		Last Modified: Thu, 17 Oct 2024 07:02:14 GMT  
		Size: 1.7 KB (1695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efc38868d75c2dc0630e02d13b3c84282f1e57ab9f8b7afa0664715a7ceef2d6`  
		Last Modified: Thu, 17 Oct 2024 07:02:14 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:latest` - linux; arm variant v5

```console
$ docker pull yourls@sha256:63b14e9f832da95bed36dea03565ac48b288ac23188eed6b042a99c97201e70f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.2 MB (156182135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27ede5116cbfa92ec1905ab7ff578a6bc5a31019933aae2c4f714749c58c6973`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 17 Oct 2024 00:54:28 GMT
ADD file:c8ec8d65b2f61866a2c6085ed61e936733bc484abeeba1b91d12b9f6a97e456b in / 
# Thu, 17 Oct 2024 00:54:29 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:39:29 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 17 Oct 2024 01:39:29 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 17 Oct 2024 01:40:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 01:40:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 17 Oct 2024 01:40:04 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 17 Oct 2024 01:48:22 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 17 Oct 2024 01:48:23 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 17 Oct 2024 01:48:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Thu, 17 Oct 2024 01:48:39 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Thu, 17 Oct 2024 01:48:40 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Thu, 17 Oct 2024 01:48:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Oct 2024 01:48:41 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Oct 2024 01:48:41 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 17 Oct 2024 02:20:58 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 17 Oct 2024 02:51:34 GMT
ENV PHP_VERSION=8.3.12
# Thu, 17 Oct 2024 02:51:34 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.12.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.12.tar.xz.asc
# Thu, 17 Oct 2024 02:51:34 GMT
ENV PHP_SHA256=f774e28633e26fc8c5197f4dae58ec9e3ff87d1b4311cbc61ab05a7ad24bd131
# Thu, 17 Oct 2024 02:51:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 17 Oct 2024 02:51:49 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 17 Oct 2024 02:59:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 17 Oct 2024 02:59:09 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Thu, 17 Oct 2024 02:59:11 GMT
RUN docker-php-ext-enable sodium
# Thu, 17 Oct 2024 02:59:11 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 17 Oct 2024 02:59:11 GMT
STOPSIGNAL SIGWINCH
# Thu, 17 Oct 2024 02:59:12 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 17 Oct 2024 02:59:12 GMT
WORKDIR /var/www/html
# Thu, 17 Oct 2024 02:59:12 GMT
EXPOSE 80
# Thu, 17 Oct 2024 02:59:13 GMT
CMD ["apache2-foreground"]
# Thu, 17 Oct 2024 04:18:06 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli
# Thu, 17 Oct 2024 04:18:07 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Thu, 17 Oct 2024 04:18:07 GMT
RUN a2enmod rewrite expires
# Thu, 17 Oct 2024 04:18:08 GMT
ARG YOURLS_VERSION=1.9.2
# Thu, 17 Oct 2024 04:18:08 GMT
ARG YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
# Thu, 17 Oct 2024 04:18:08 GMT
ENV YOURLS_VERSION=1.9.2
# Thu, 17 Oct 2024 04:18:08 GMT
ENV YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
# Thu, 17 Oct 2024 04:18:10 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Thu, 17 Oct 2024 04:18:10 GMT
COPY --chown=www-data:www-datafile:407fa98e3948ea07c2ff8bc30ad1b3b7b28a1c2b9b5d8e5ab87f9b317a2bac85 in /usr/src/yourls/user/ 
# Thu, 17 Oct 2024 04:18:11 GMT
COPY file:50b4d483341578e719ad63fd7aaea99a0d6d7cebfb7b43d6098a656a975ee0e3 in /usr/local/bin/ 
# Thu, 17 Oct 2024 04:18:11 GMT
COPY file:5b7ff05d0c98ad759c4bec0ef8a7ce74cae42e95b42564b55f43b341c2c3e3f5 in /usr/src/yourls/ 
# Thu, 17 Oct 2024 04:18:11 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Thu, 17 Oct 2024 04:18:11 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:e51d4479d9f15eaafec663087c05baede0a0724dc30787f7912ade3b686f46b1`  
		Last Modified: Thu, 17 Oct 2024 00:57:27 GMT  
		Size: 26.9 MB (26887306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcc5235299add7bb4a13b494a07f66eb5939b6cb20e1cc0d0f75550967a7376c`  
		Last Modified: Thu, 17 Oct 2024 03:45:03 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f8907632e889fbd259ac6ebe1d70401840bf18fb005d7c35952efd42916d520`  
		Last Modified: Thu, 17 Oct 2024 03:45:21 GMT  
		Size: 82.0 MB (81995968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd6a7f456b58f9278213fe4b51fb3844191e9e472c54adce160d2e3ebea1c81e`  
		Last Modified: Thu, 17 Oct 2024 03:45:02 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19743805d7cb37913f1b3f1b2cf18aa012ad377a421c22b0a52997bbc49d64e5`  
		Last Modified: Thu, 17 Oct 2024 03:45:46 GMT  
		Size: 19.6 MB (19624385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d056f964ef6cf0cfd02b1e7ab1e9df4a4500d9af80762867bf9f4da4ee999f9e`  
		Last Modified: Thu, 17 Oct 2024 03:45:42 GMT  
		Size: 437.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a567fd2c394a19ce53e7a88c0cef2c03c411330889c3b51677db7bd9d1fa408`  
		Last Modified: Thu, 17 Oct 2024 03:45:42 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43429895a95af4cdb790638d472a961bd0c7a9744826f7203d9d8a7e52190c2c`  
		Last Modified: Thu, 17 Oct 2024 03:48:29 GMT  
		Size: 12.8 MB (12824767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb3dba79250d004c8b74347a78de8732f0e3c918904743c137b01d7c0e4a98d4`  
		Last Modified: Thu, 17 Oct 2024 03:48:26 GMT  
		Size: 489.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf5810ba9f7134b64eafec073847240a90c5cbcfc116df4ee26ecdd4101a332a`  
		Last Modified: Thu, 17 Oct 2024 03:48:29 GMT  
		Size: 10.6 MB (10611651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc701d080e030c04ce0393a89b3f00c6b599074d7520779455498e0d622abd70`  
		Last Modified: Thu, 17 Oct 2024 03:48:26 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a6bcabbafb6cb0a533f2f2c8bbe8411037e29dd4e357500e6d260dabfd0c0b3`  
		Last Modified: Thu, 17 Oct 2024 03:48:26 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af2021ea067a09198dd701cd02ce807b0c474c607bb5abda05a9b0f3b2df12c2`  
		Last Modified: Thu, 17 Oct 2024 03:48:26 GMT  
		Size: 895.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57f9942a51860081e9ee251f94aee3532919f044ead92945bb79351b5034585b`  
		Last Modified: Thu, 17 Oct 2024 04:18:54 GMT  
		Size: 154.4 KB (154386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3bb35dfda1c89852e227a4effd41005a5a55de67b758dc9f2d55753e0d00965`  
		Last Modified: Thu, 17 Oct 2024 04:18:54 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f490b0a76b3356c4cd5237134abc88edf86b77ef493696378fb2be89db46e86`  
		Last Modified: Thu, 17 Oct 2024 04:18:52 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4896b2126e9c2df709ceb05f885de896030229197ec490606c904be529a2a01`  
		Last Modified: Thu, 17 Oct 2024 04:18:54 GMT  
		Size: 4.1 MB (4073453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32426a224db126169e6e22d625884603d46d9c316c4f8109b11120e6578dc765`  
		Last Modified: Thu, 17 Oct 2024 04:18:52 GMT  
		Size: 2.1 KB (2051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a56e83fcce62e80a8a7c3e1379ba2a8ede52725568064854d73cfa760156e0ad`  
		Last Modified: Thu, 17 Oct 2024 04:18:52 GMT  
		Size: 1.7 KB (1694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5cd5984fd749a31bb84ed40f617c9c128ebb3d79476702a045941a5533daedd`  
		Last Modified: Thu, 17 Oct 2024 04:18:52 GMT  
		Size: 333.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:latest` - linux; arm variant v7

```console
$ docker pull yourls@sha256:3d7ae68ef6b74ee7bbc43b458b62e378ff6b4f58f030d24ba2ef13d01fbf33f1
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.0 MB (147029323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e59f894ae6877c17fd66d7c861000fda84e124fc6dfc4de6899d1d82004c9d93`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 17 Oct 2024 03:03:21 GMT
ADD file:e76e8ba7ebca0b1dcaec16ad1e863ab59c7e155f0b95ba46f5543e418a904b35 in / 
# Thu, 17 Oct 2024 03:03:22 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 03:43:53 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 17 Oct 2024 03:43:53 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 17 Oct 2024 03:44:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 03:44:11 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 17 Oct 2024 03:44:12 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 17 Oct 2024 03:47:16 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 17 Oct 2024 03:47:16 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 17 Oct 2024 03:47:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Thu, 17 Oct 2024 03:47:25 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Thu, 17 Oct 2024 03:47:26 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Thu, 17 Oct 2024 03:47:26 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Oct 2024 03:47:26 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Oct 2024 03:47:26 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 17 Oct 2024 04:12:32 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 17 Oct 2024 04:33:46 GMT
ENV PHP_VERSION=8.3.12
# Thu, 17 Oct 2024 04:33:46 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.12.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.12.tar.xz.asc
# Thu, 17 Oct 2024 04:33:46 GMT
ENV PHP_SHA256=f774e28633e26fc8c5197f4dae58ec9e3ff87d1b4311cbc61ab05a7ad24bd131
# Thu, 17 Oct 2024 04:33:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 17 Oct 2024 04:33:57 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 17 Oct 2024 04:36:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 17 Oct 2024 04:36:41 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Thu, 17 Oct 2024 04:36:42 GMT
RUN docker-php-ext-enable sodium
# Thu, 17 Oct 2024 04:36:42 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 17 Oct 2024 04:36:42 GMT
STOPSIGNAL SIGWINCH
# Thu, 17 Oct 2024 04:36:42 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 17 Oct 2024 04:36:42 GMT
WORKDIR /var/www/html
# Thu, 17 Oct 2024 04:36:42 GMT
EXPOSE 80
# Thu, 17 Oct 2024 04:36:42 GMT
CMD ["apache2-foreground"]
# Thu, 17 Oct 2024 08:09:17 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli
# Thu, 17 Oct 2024 08:09:17 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Thu, 17 Oct 2024 08:09:18 GMT
RUN a2enmod rewrite expires
# Thu, 17 Oct 2024 08:09:18 GMT
ARG YOURLS_VERSION=1.9.2
# Thu, 17 Oct 2024 08:09:18 GMT
ARG YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
# Thu, 17 Oct 2024 08:09:18 GMT
ENV YOURLS_VERSION=1.9.2
# Thu, 17 Oct 2024 08:09:18 GMT
ENV YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
# Thu, 17 Oct 2024 08:09:20 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Thu, 17 Oct 2024 08:09:20 GMT
COPY --chown=www-data:www-datafile:407fa98e3948ea07c2ff8bc30ad1b3b7b28a1c2b9b5d8e5ab87f9b317a2bac85 in /usr/src/yourls/user/ 
# Thu, 17 Oct 2024 08:09:20 GMT
COPY file:50b4d483341578e719ad63fd7aaea99a0d6d7cebfb7b43d6098a656a975ee0e3 in /usr/local/bin/ 
# Thu, 17 Oct 2024 08:09:20 GMT
COPY file:5b7ff05d0c98ad759c4bec0ef8a7ce74cae42e95b42564b55f43b341c2c3e3f5 in /usr/src/yourls/ 
# Thu, 17 Oct 2024 08:09:21 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Thu, 17 Oct 2024 08:09:21 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:d6319e551f4eae5cadf245338228c7b7cbad94a77c481a88ccbffef7b89f0aee`  
		Last Modified: Thu, 17 Oct 2024 03:06:55 GMT  
		Size: 24.7 MB (24718197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57816ea258091707b20fd42869f1859c1543e794b483b8003de268daf39132a0`  
		Last Modified: Thu, 17 Oct 2024 06:00:20 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f29e3f6b59ec149599415083926b75214bfab19a179c7ef4d7535bbee364a84`  
		Last Modified: Thu, 17 Oct 2024 06:00:36 GMT  
		Size: 76.2 MB (76163462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ace57af7e6d627dfdf6574de994827570ba429858c8118ccf5028e7c121e0e9b`  
		Last Modified: Thu, 17 Oct 2024 06:00:20 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9863416241c1e20444861f13ebb223232950439972781be1e45b6704fee41682`  
		Last Modified: Thu, 17 Oct 2024 06:00:59 GMT  
		Size: 19.1 MB (19062321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:300e0800b02d2903ba85150c9b5f31cab1e364d99e199b1614838bb031e1116c`  
		Last Modified: Thu, 17 Oct 2024 06:00:56 GMT  
		Size: 434.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11748bf3dd7f577b46d343e58bff8badc4bb124233ef94312a971750f9db7079`  
		Last Modified: Thu, 17 Oct 2024 06:00:56 GMT  
		Size: 486.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d97495b6015931febd096725532a7f1e8beed5b2ae7564d39f92afe406973388`  
		Last Modified: Thu, 17 Oct 2024 06:05:42 GMT  
		Size: 12.8 MB (12824662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66d60d738d7854d3e58b6a8dd9f9512d48d84f3beb63ff04e9506c670d6ea906`  
		Last Modified: Thu, 17 Oct 2024 06:05:39 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b47da1e132b2972be9ba98a20508f9f262dc461342531be1cfa785fc2ddbfdff`  
		Last Modified: Thu, 17 Oct 2024 06:05:42 GMT  
		Size: 10.0 MB (10035389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c90a1f68f8b8e071e68c960893fcc9dfcbeb4297d1ca8eb077e74ee7c8674b7`  
		Last Modified: Thu, 17 Oct 2024 06:05:39 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:136becfad67cdc02558171f1c67a6b60e3db7b13e8c51dd5cef0075ca0626763`  
		Last Modified: Thu, 17 Oct 2024 06:05:40 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d21efe4a3505efde22e3d7017b7da51a5772f1c69ef4e7b7b389b8c222a0cfcf`  
		Last Modified: Thu, 17 Oct 2024 06:05:39 GMT  
		Size: 892.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cea996f23f1aaae7a73e601dadac6670d13aff34a171b6e828a1e6aabf1ba7ad`  
		Last Modified: Thu, 17 Oct 2024 08:09:59 GMT  
		Size: 141.7 KB (141664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea99c73d11ef6924d82ef487337b1364d1b2366521cdf72c5db93bd7394ab0d6`  
		Last Modified: Thu, 17 Oct 2024 08:09:59 GMT  
		Size: 323.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d99681b4e79283cd54c232143b52e09e27c2e483aa44eb17ff422aa502ea2869`  
		Last Modified: Thu, 17 Oct 2024 08:09:57 GMT  
		Size: 338.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c983a2db8f8cb3659a20aef2d717be23f65cb106db1fecb383e9355852ecf5c8`  
		Last Modified: Thu, 17 Oct 2024 08:09:58 GMT  
		Size: 4.1 MB (4073441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebf82e41afa354873df436403b94b8f41d797fc24b071febf24c59933c94f796`  
		Last Modified: Thu, 17 Oct 2024 08:09:57 GMT  
		Size: 2.1 KB (2052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97f155fd315d35827694f27230f14f1d519d2efc4324b5b9cf6d21c42b0f5f49`  
		Last Modified: Thu, 17 Oct 2024 08:09:57 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:524172f253593a9c0c0ab2314b1298f37d4cf41cdfbcb42aaab538326b509248`  
		Last Modified: Thu, 17 Oct 2024 08:09:57 GMT  
		Size: 332.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:latest` - linux; arm64 variant v8

```console
$ docker pull yourls@sha256:e2fc804c2e900cd20bb77c0b5c5dcbeda5bb90412b212fb8edbcfaa19bfd9c8b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.0 MB (176953922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d527136056720c259e5595555bc76aaba361f2317cea68da09c3e523f80334d`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 17 Oct 2024 01:11:59 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Thu, 17 Oct 2024 01:11:59 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:35:05 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 17 Oct 2024 01:35:05 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 17 Oct 2024 01:35:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 01:35:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 17 Oct 2024 01:35:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 17 Oct 2024 01:38:28 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 17 Oct 2024 01:38:28 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 17 Oct 2024 01:38:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Thu, 17 Oct 2024 01:38:35 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Thu, 17 Oct 2024 01:38:35 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Thu, 17 Oct 2024 01:38:36 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Oct 2024 01:38:36 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Oct 2024 01:38:36 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 17 Oct 2024 02:03:27 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 17 Oct 2024 02:31:56 GMT
ENV PHP_VERSION=8.3.12
# Thu, 17 Oct 2024 02:31:56 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.12.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.12.tar.xz.asc
# Thu, 17 Oct 2024 02:31:56 GMT
ENV PHP_SHA256=f774e28633e26fc8c5197f4dae58ec9e3ff87d1b4311cbc61ab05a7ad24bd131
# Thu, 17 Oct 2024 02:32:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 17 Oct 2024 02:32:05 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 17 Oct 2024 02:35:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 17 Oct 2024 02:35:39 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Thu, 17 Oct 2024 02:35:40 GMT
RUN docker-php-ext-enable sodium
# Thu, 17 Oct 2024 02:35:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 17 Oct 2024 02:35:40 GMT
STOPSIGNAL SIGWINCH
# Thu, 17 Oct 2024 02:35:40 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 17 Oct 2024 02:35:40 GMT
WORKDIR /var/www/html
# Thu, 17 Oct 2024 02:35:40 GMT
EXPOSE 80
# Thu, 17 Oct 2024 02:35:40 GMT
CMD ["apache2-foreground"]
# Thu, 17 Oct 2024 06:43:02 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli
# Thu, 17 Oct 2024 06:43:02 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Thu, 17 Oct 2024 06:43:03 GMT
RUN a2enmod rewrite expires
# Thu, 17 Oct 2024 06:43:03 GMT
ARG YOURLS_VERSION=1.9.2
# Thu, 17 Oct 2024 06:43:03 GMT
ARG YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
# Thu, 17 Oct 2024 06:43:03 GMT
ENV YOURLS_VERSION=1.9.2
# Thu, 17 Oct 2024 06:43:03 GMT
ENV YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
# Thu, 17 Oct 2024 06:43:05 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Thu, 17 Oct 2024 06:43:05 GMT
COPY --chown=www-data:www-datafile:407fa98e3948ea07c2ff8bc30ad1b3b7b28a1c2b9b5d8e5ab87f9b317a2bac85 in /usr/src/yourls/user/ 
# Thu, 17 Oct 2024 06:43:05 GMT
COPY file:50b4d483341578e719ad63fd7aaea99a0d6d7cebfb7b43d6098a656a975ee0e3 in /usr/local/bin/ 
# Thu, 17 Oct 2024 06:43:05 GMT
COPY file:5b7ff05d0c98ad759c4bec0ef8a7ce74cae42e95b42564b55f43b341c2c3e3f5 in /usr/src/yourls/ 
# Thu, 17 Oct 2024 06:43:05 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Thu, 17 Oct 2024 06:43:06 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6530e6e936cdf7969275d55704b89e0466613540a41ab09fa6edc24a35d57e8`  
		Last Modified: Thu, 17 Oct 2024 04:17:13 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22ffd48d74a0a5446013c25727b2812f6f385b0ffe0ff99f0439d18dad5e5e8c`  
		Last Modified: Thu, 17 Oct 2024 04:17:25 GMT  
		Size: 98.1 MB (98131870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7046151abb10af1a2158520721c2b5006584c918b2f36fdb943a5dc36edebe22`  
		Last Modified: Thu, 17 Oct 2024 04:17:13 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44cbece021606df0e0fd4b7b7123856cec73a741c16c93632a0050521f432385`  
		Last Modified: Thu, 17 Oct 2024 04:17:48 GMT  
		Size: 20.3 MB (20325322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce14de3b55afb7a464228d842abfe056cbe1fc2d0809fc69a0206aa13dbdc345`  
		Last Modified: Thu, 17 Oct 2024 04:17:45 GMT  
		Size: 436.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08f9962d8983968c3cbbc14b531cea8c72c6c3e0f3e8f36dd3838319b579fc16`  
		Last Modified: Thu, 17 Oct 2024 04:17:45 GMT  
		Size: 486.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4578253059e29ebac47aa22a312ae424ac781686153d9b3395455b2d4c131897`  
		Last Modified: Thu, 17 Oct 2024 04:22:05 GMT  
		Size: 12.8 MB (12826530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af1b2a592ce8fb821e7c3f01f4c3e7c710e677fe48e2fcc539f4c9f42d9cae40`  
		Last Modified: Thu, 17 Oct 2024 04:22:02 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f9d235e10cd0242a85a1272d80748391b47cf294929cf90e21a5d7d68a44a0e`  
		Last Modified: Thu, 17 Oct 2024 04:22:04 GMT  
		Size: 11.6 MB (11635924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1cda3882f41560558f2b0c10beedfd6e89c02c024e6b16f16fbced4027a18ef`  
		Last Modified: Thu, 17 Oct 2024 04:22:02 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15ed694f2abdad1bb30542119d7daaf1342ab3843eb6620a09b519ae9457104`  
		Last Modified: Thu, 17 Oct 2024 04:22:02 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19f502847316ff12c6242d3528d6a053ae704fdbe5f8ff2f5eb6c3bc207ace17`  
		Last Modified: Thu, 17 Oct 2024 04:22:02 GMT  
		Size: 890.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c154e46c581a47b562f71fa8ec0c305e1497e0d44c8ef3bcef41a8ad890da46`  
		Last Modified: Thu, 17 Oct 2024 06:44:29 GMT  
		Size: 794.3 KB (794296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dfbc55a44c286062a5b4fa3e126cb2b283335367533c22b094ab68fc2e02ca2`  
		Last Modified: Thu, 17 Oct 2024 06:44:29 GMT  
		Size: 324.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ab7887e6da0174466b8a33049c9cb44cc9b61dc52d9b9ad446210ac5f52aa4b`  
		Last Modified: Thu, 17 Oct 2024 06:44:27 GMT  
		Size: 344.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b17e32baddc289f2565a38505688e8fb3b6363394a1357da699c76ae97233694`  
		Last Modified: Thu, 17 Oct 2024 06:44:28 GMT  
		Size: 4.1 MB (4073454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24826a366318c87616e7da6a05f4eff562b8ca468804266e52f91cb4d1706cc2`  
		Last Modified: Thu, 17 Oct 2024 06:44:27 GMT  
		Size: 2.0 KB (2048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29af5d576b0bda5a304ce818cc90c0074ab8c296c89136e7095a00b3fc737064`  
		Last Modified: Thu, 17 Oct 2024 06:44:27 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7af64220210ab619a4f7ad857d005db93dbe6817d47185eefce4250bf2026aa`  
		Last Modified: Thu, 17 Oct 2024 06:44:27 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:latest` - linux; 386

```console
$ docker pull yourls@sha256:7b66d22afd3991744586b7f5a9b4914fd4e9296c768f2bd9e7ac89ba26faee9c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.8 MB (181781819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33ba712eafe66c6cc7f8db924faf0533e5a904cbf20a4083cecdd9d0cd2f79d6`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 17 Oct 2024 00:38:56 GMT
ADD file:9e1e244025374c1ce772075845b1331852635a8eb7d29e206c37cd9de6ad8617 in / 
# Thu, 17 Oct 2024 00:38:56 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:15:05 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 17 Oct 2024 01:15:05 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 17 Oct 2024 01:15:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 01:15:29 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 17 Oct 2024 01:15:30 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 17 Oct 2024 01:22:28 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 17 Oct 2024 01:22:28 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 17 Oct 2024 01:22:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Thu, 17 Oct 2024 01:22:38 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Thu, 17 Oct 2024 01:22:39 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Thu, 17 Oct 2024 01:22:39 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Oct 2024 01:22:39 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Oct 2024 01:22:39 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 17 Oct 2024 02:13:59 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 17 Oct 2024 03:02:46 GMT
ENV PHP_VERSION=8.3.12
# Thu, 17 Oct 2024 03:02:46 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.12.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.12.tar.xz.asc
# Thu, 17 Oct 2024 03:02:46 GMT
ENV PHP_SHA256=f774e28633e26fc8c5197f4dae58ec9e3ff87d1b4311cbc61ab05a7ad24bd131
# Thu, 17 Oct 2024 03:02:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 17 Oct 2024 03:02:58 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 17 Oct 2024 03:09:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 17 Oct 2024 03:09:12 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Thu, 17 Oct 2024 03:09:12 GMT
RUN docker-php-ext-enable sodium
# Thu, 17 Oct 2024 03:09:12 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 17 Oct 2024 03:09:13 GMT
STOPSIGNAL SIGWINCH
# Thu, 17 Oct 2024 03:09:13 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 17 Oct 2024 03:09:13 GMT
WORKDIR /var/www/html
# Thu, 17 Oct 2024 03:09:13 GMT
EXPOSE 80
# Thu, 17 Oct 2024 03:09:13 GMT
CMD ["apache2-foreground"]
# Thu, 17 Oct 2024 08:34:56 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli
# Thu, 17 Oct 2024 08:34:57 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Thu, 17 Oct 2024 08:34:57 GMT
RUN a2enmod rewrite expires
# Thu, 17 Oct 2024 08:34:57 GMT
ARG YOURLS_VERSION=1.9.2
# Thu, 17 Oct 2024 08:34:57 GMT
ARG YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
# Thu, 17 Oct 2024 08:34:58 GMT
ENV YOURLS_VERSION=1.9.2
# Thu, 17 Oct 2024 08:34:58 GMT
ENV YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
# Thu, 17 Oct 2024 08:35:00 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Thu, 17 Oct 2024 08:35:00 GMT
COPY --chown=www-data:www-datafile:407fa98e3948ea07c2ff8bc30ad1b3b7b28a1c2b9b5d8e5ab87f9b317a2bac85 in /usr/src/yourls/user/ 
# Thu, 17 Oct 2024 08:35:00 GMT
COPY file:50b4d483341578e719ad63fd7aaea99a0d6d7cebfb7b43d6098a656a975ee0e3 in /usr/local/bin/ 
# Thu, 17 Oct 2024 08:35:00 GMT
COPY file:5b7ff05d0c98ad759c4bec0ef8a7ce74cae42e95b42564b55f43b341c2c3e3f5 in /usr/src/yourls/ 
# Thu, 17 Oct 2024 08:35:00 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Thu, 17 Oct 2024 08:35:00 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:f1bcef69cca27061b771e6bb01a051f6879c730ec30ed4661fef463e7d798d9c`  
		Last Modified: Thu, 17 Oct 2024 00:42:33 GMT  
		Size: 30.1 MB (30144267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4ade5403812963eef73a48c4f07cea521affbaab25dbb28bfe5359cbc22bac9`  
		Last Modified: Thu, 17 Oct 2024 06:07:19 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e936af8dfe7f46433beca18a2d23ce12cc58b84c97bd759cde69ae04ffd1ef8f`  
		Last Modified: Thu, 17 Oct 2024 06:07:43 GMT  
		Size: 101.5 MB (101513470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6390a21b9a7d3612aec1c9c3ddfe5307169cf7c8fe4dd367e3bd5be8f7f53934`  
		Last Modified: Thu, 17 Oct 2024 06:07:19 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df26b407a97966ce11f72a59d30a9c0c723177d7b69a0565ecb1fcb3f09c1baf`  
		Last Modified: Thu, 17 Oct 2024 06:08:08 GMT  
		Size: 20.8 MB (20842838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8733f6ebe17cf6bd9288e771b20ef3e8623fb0118e887ac501fffddccd07ff5b`  
		Last Modified: Thu, 17 Oct 2024 06:08:03 GMT  
		Size: 437.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcf9132130b1c398a4e2da6fffcd1f6cdb97ae92cabd3573482cb658a1bf94c7`  
		Last Modified: Thu, 17 Oct 2024 06:08:03 GMT  
		Size: 486.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4976a9132224f324da4d05b0f5736dfadd7c9b968d057d0b3443b0e158afe72`  
		Last Modified: Thu, 17 Oct 2024 06:13:19 GMT  
		Size: 12.8 MB (12825802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10587c9fe223357ac06722bdddaa7c71002c5173670a703facc87ea8f7761094`  
		Last Modified: Thu, 17 Oct 2024 06:13:16 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e7ee5ab7adf9414cf0f4a2bea7cfbae68641e88679d34a02f2daf5a7140072f`  
		Last Modified: Thu, 17 Oct 2024 06:13:19 GMT  
		Size: 11.9 MB (11865170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:831cded3e19d6d6f67b418c8023dfab583d69b80551b01b83e3dcab37de7b938`  
		Last Modified: Thu, 17 Oct 2024 06:13:16 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f9c9d06368911ac3b127538d109b1a7ceedaeb324b4679e893aa5f94441e4c6`  
		Last Modified: Thu, 17 Oct 2024 06:13:16 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe05f34c60104c4dfedf187d9204a1e20e9421d5a530e5d172a2f0c4f869f4a9`  
		Last Modified: Thu, 17 Oct 2024 06:13:16 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b42758378db12d0a4bf6b28c87abf13ba2538f748c3e562195c1c8b5d294b69d`  
		Last Modified: Thu, 17 Oct 2024 08:36:17 GMT  
		Size: 506.6 KB (506620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6e70e569ca80528338008efabbe04d40f06cd4b9f51ec1a6f92b4948b1ac64d`  
		Last Modified: Thu, 17 Oct 2024 08:36:17 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae407a332987a9c8600b56f6cd01fd0649f5a5d8850431a526ea2f0c5e2a0c20`  
		Last Modified: Thu, 17 Oct 2024 08:36:15 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67348f2cffca42a64d5ce9623bf8823dc119aa5b3b744610c50f0cd37e23a4d9`  
		Last Modified: Thu, 17 Oct 2024 08:36:16 GMT  
		Size: 4.1 MB (4073442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6d30b63ae332b881dcf3803128cbec5df80885a0cc54a7b345150717bf6af08`  
		Last Modified: Thu, 17 Oct 2024 08:36:15 GMT  
		Size: 2.1 KB (2051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ff0a3cd692757ee1a847ae941716f240e2b8a107bf287fdea96a21ff5d6d7b5`  
		Last Modified: Thu, 17 Oct 2024 08:36:15 GMT  
		Size: 1.7 KB (1696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b1fb24fee84048da2abf9c18d6347140ccae9fcd67bc781a5658ff55e863ea8`  
		Last Modified: Thu, 17 Oct 2024 08:36:15 GMT  
		Size: 331.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:latest` - linux; mips64le

```console
$ docker pull yourls@sha256:bb5c78c1b998d09e1d879b57ab674916291bd08a8cb343c0611cf41a17ab66a0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.4 MB (157433650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73c6e498662b83db5c97a1446dd61c9ebf873bbe3a31ac5fa27f0968f324fd3d`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 17 Oct 2024 01:09:35 GMT
ADD file:6c11edc513b28b5a4034ee9c0d4cdcf019a82635ebb8a9e02732800fa457f683 in / 
# Thu, 17 Oct 2024 01:09:40 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 02:19:19 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 17 Oct 2024 02:19:22 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 17 Oct 2024 02:21:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 02:21:10 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 17 Oct 2024 02:21:16 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 17 Oct 2024 02:38:57 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 17 Oct 2024 02:39:01 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 17 Oct 2024 02:39:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Thu, 17 Oct 2024 02:39:56 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Thu, 17 Oct 2024 02:40:02 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Thu, 17 Oct 2024 02:40:06 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Oct 2024 02:40:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Oct 2024 02:40:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 17 Oct 2024 03:48:17 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 17 Oct 2024 04:52:50 GMT
ENV PHP_VERSION=8.3.12
# Thu, 17 Oct 2024 04:52:53 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.12.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.12.tar.xz.asc
# Thu, 17 Oct 2024 04:52:57 GMT
ENV PHP_SHA256=f774e28633e26fc8c5197f4dae58ec9e3ff87d1b4311cbc61ab05a7ad24bd131
# Thu, 17 Oct 2024 04:53:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 17 Oct 2024 04:53:49 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 17 Oct 2024 05:09:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 17 Oct 2024 05:09:17 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Thu, 17 Oct 2024 05:09:23 GMT
RUN docker-php-ext-enable sodium
# Thu, 17 Oct 2024 05:09:27 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 17 Oct 2024 05:09:31 GMT
STOPSIGNAL SIGWINCH
# Thu, 17 Oct 2024 05:09:34 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 17 Oct 2024 05:09:38 GMT
WORKDIR /var/www/html
# Thu, 17 Oct 2024 05:09:41 GMT
EXPOSE 80
# Thu, 17 Oct 2024 05:09:45 GMT
CMD ["apache2-foreground"]
# Thu, 17 Oct 2024 12:15:49 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli
# Thu, 17 Oct 2024 12:15:56 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Thu, 17 Oct 2024 12:16:02 GMT
RUN a2enmod rewrite expires
# Thu, 17 Oct 2024 12:16:06 GMT
ARG YOURLS_VERSION=1.9.2
# Thu, 17 Oct 2024 12:16:10 GMT
ARG YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
# Thu, 17 Oct 2024 12:16:14 GMT
ENV YOURLS_VERSION=1.9.2
# Thu, 17 Oct 2024 12:16:18 GMT
ENV YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
# Thu, 17 Oct 2024 12:16:28 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Thu, 17 Oct 2024 12:16:32 GMT
COPY --chown=www-data:www-datafile:407fa98e3948ea07c2ff8bc30ad1b3b7b28a1c2b9b5d8e5ab87f9b317a2bac85 in /usr/src/yourls/user/ 
# Thu, 17 Oct 2024 12:16:35 GMT
COPY file:50b4d483341578e719ad63fd7aaea99a0d6d7cebfb7b43d6098a656a975ee0e3 in /usr/local/bin/ 
# Thu, 17 Oct 2024 12:16:38 GMT
COPY file:5b7ff05d0c98ad759c4bec0ef8a7ce74cae42e95b42564b55f43b341c2c3e3f5 in /usr/src/yourls/ 
# Thu, 17 Oct 2024 12:16:42 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Thu, 17 Oct 2024 12:16:46 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:8f9d02f0305fc460f51690aebcb328c22e13a197228c0910e24b813db943a15b`  
		Last Modified: Thu, 17 Oct 2024 01:18:03 GMT  
		Size: 29.1 MB (29124779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3add5d8ad97d2ba7877924447ad98d789dbf096a71456bc495d0a7a74e8afb9`  
		Last Modified: Thu, 17 Oct 2024 08:52:22 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d206c68dc9357055fa42cdf1b67ba24c98962d0c7550f84933512d107f85a2c0`  
		Last Modified: Thu, 17 Oct 2024 08:53:18 GMT  
		Size: 80.7 MB (80667204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddd3adaa11daa51a3a26c065af83992847000612bf88e53a1dcb9feb819b02e3`  
		Last Modified: Thu, 17 Oct 2024 08:52:22 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1669fc913ce96fa2d4887bd63e3e183b72f0354914597276391ec0d6a3d04262`  
		Last Modified: Thu, 17 Oct 2024 08:53:57 GMT  
		Size: 20.1 MB (20068775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8771bdfe6c9af3f18291fcf55f0351d9928f5669267b76b3837a0e3a221e5b09`  
		Last Modified: Thu, 17 Oct 2024 08:53:44 GMT  
		Size: 437.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b19aed48dd02184a4d00c1fac98d6cebd3771223e6bd7e4189ad3650fb453a9c`  
		Last Modified: Thu, 17 Oct 2024 08:53:44 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2be6c000b654449ecd4f68a94692f1dc3cba025a75e1f546f54f9dcb88639a85`  
		Last Modified: Thu, 17 Oct 2024 08:58:51 GMT  
		Size: 12.6 MB (12619541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6bf210650a307de5596338c2058b9e8dca27bd6b9ba5f32f56968115de2efca`  
		Last Modified: Thu, 17 Oct 2024 08:58:46 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:218dbe5edf60ac6e1858030b4bfb285ebdcd4fb8a02387c9f331e9aad6e0742a`  
		Last Modified: Thu, 17 Oct 2024 08:58:54 GMT  
		Size: 10.7 MB (10716717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8f067b571c74bc036db926bb1d7a09b38736ce0c85e03e17edf75ca15a1d429`  
		Last Modified: Thu, 17 Oct 2024 08:58:45 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dae8a578534a78008c5c73bbcb318f1328b6309da371f96e09335c28c7624fbb`  
		Last Modified: Thu, 17 Oct 2024 08:58:45 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5d3e7520ee2c7120d27a1d17eda6afe9ec607239a1d4b731194217a7f649c83`  
		Last Modified: Thu, 17 Oct 2024 08:58:45 GMT  
		Size: 895.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ce2e7d89342c5a935c499e72fc07f11978a4b6433315a01645d52aa7e016c11`  
		Last Modified: Thu, 17 Oct 2024 12:19:20 GMT  
		Size: 153.0 KB (152975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:694a3f5898e218ce2862a571152c918ec9f302c867f3d0916a4fde45133368d7`  
		Last Modified: Thu, 17 Oct 2024 12:19:19 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecadcfaa672977193cb5e522766b38b37cbcd3904520eeca5038646e2b1a9e5e`  
		Last Modified: Thu, 17 Oct 2024 12:19:17 GMT  
		Size: 348.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43990fb312a035ba9e47e19543956413564455324d10e1dfdbf83c841a21ad15`  
		Last Modified: Thu, 17 Oct 2024 12:19:20 GMT  
		Size: 4.1 MB (4073437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d169912439d7c903052e16ed957e75d5ae4f493fd9fd5cd72a9409d6fe470ce8`  
		Last Modified: Thu, 17 Oct 2024 12:19:17 GMT  
		Size: 2.1 KB (2056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c5b591189d01b275810860200d5fa3fc45f16d58bb110a92f0bf3361ec343de`  
		Last Modified: Thu, 17 Oct 2024 12:19:17 GMT  
		Size: 1.7 KB (1693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aee65ee5af2f91221567d2fd069d14c9fb8760ae59e0074d8e5d8b7d7ece4971`  
		Last Modified: Thu, 17 Oct 2024 12:19:17 GMT  
		Size: 333.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:latest` - linux; ppc64le

```console
$ docker pull yourls@sha256:ef29180efcc944784df62c47afef73d6938306157e63d4d5636f27e59c95604a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.1 MB (187112776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38f6ca3275a39b953cabdd92e9c2495b2a20b3943f93782c490496a6c7b7b13b`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 17 Oct 2024 01:18:54 GMT
ADD file:92b9ed0a5c924ec85b272100ff6dc81f126c6bd277ec2b3782af1119f9e07391 in / 
# Thu, 17 Oct 2024 01:18:56 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:55:17 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 17 Oct 2024 01:55:17 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 17 Oct 2024 01:55:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 01:55:48 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 17 Oct 2024 01:55:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 17 Oct 2024 01:58:56 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 17 Oct 2024 01:58:56 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 17 Oct 2024 01:59:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Thu, 17 Oct 2024 01:59:12 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Thu, 17 Oct 2024 01:59:13 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Thu, 17 Oct 2024 01:59:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Oct 2024 01:59:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Oct 2024 01:59:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 17 Oct 2024 02:11:51 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 24 Oct 2024 23:55:07 GMT
ENV PHP_VERSION=8.3.13
# Thu, 24 Oct 2024 23:55:07 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Thu, 24 Oct 2024 23:55:07 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
# Thu, 24 Oct 2024 23:55:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 24 Oct 2024 23:55:22 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 24 Oct 2024 23:58:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 24 Oct 2024 23:58:17 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Thu, 24 Oct 2024 23:58:18 GMT
RUN docker-php-ext-enable sodium
# Thu, 24 Oct 2024 23:58:18 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 24 Oct 2024 23:58:18 GMT
STOPSIGNAL SIGWINCH
# Thu, 24 Oct 2024 23:58:19 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 24 Oct 2024 23:58:19 GMT
WORKDIR /var/www/html
# Thu, 24 Oct 2024 23:58:19 GMT
EXPOSE 80
# Thu, 24 Oct 2024 23:58:19 GMT
CMD ["apache2-foreground"]
# Fri, 25 Oct 2024 01:18:31 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli
# Fri, 25 Oct 2024 01:18:32 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 25 Oct 2024 01:18:33 GMT
RUN a2enmod rewrite expires
# Fri, 25 Oct 2024 01:18:33 GMT
ARG YOURLS_VERSION=1.9.2
# Fri, 25 Oct 2024 01:18:34 GMT
ARG YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
# Fri, 25 Oct 2024 01:18:34 GMT
ENV YOURLS_VERSION=1.9.2
# Fri, 25 Oct 2024 01:18:35 GMT
ENV YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
# Fri, 25 Oct 2024 01:18:37 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Fri, 25 Oct 2024 01:18:37 GMT
COPY --chown=www-data:www-datafile:407fa98e3948ea07c2ff8bc30ad1b3b7b28a1c2b9b5d8e5ab87f9b317a2bac85 in /usr/src/yourls/user/ 
# Fri, 25 Oct 2024 01:18:37 GMT
COPY file:50b4d483341578e719ad63fd7aaea99a0d6d7cebfb7b43d6098a656a975ee0e3 in /usr/local/bin/ 
# Fri, 25 Oct 2024 01:18:38 GMT
COPY file:5b7ff05d0c98ad759c4bec0ef8a7ce74cae42e95b42564b55f43b341c2c3e3f5 in /usr/src/yourls/ 
# Fri, 25 Oct 2024 01:18:38 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Fri, 25 Oct 2024 01:18:38 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:b5dc74e4487f0d4e25ed24462fe1564f5d931072ec24eeaee669f9cbe27f10c4`  
		Last Modified: Thu, 17 Oct 2024 01:21:56 GMT  
		Size: 33.1 MB (33122201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1107c787f39ae7163741fce22e3034e0e43a10e9cbe2ac207f64434e68645221`  
		Last Modified: Thu, 17 Oct 2024 03:11:57 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:627c9d0cca1e0cdb09f43b27bb6bf7d4cca0cad4afc8598940b57844dfe38615`  
		Last Modified: Thu, 17 Oct 2024 03:12:13 GMT  
		Size: 103.3 MB (103326981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cec6f65da0d52cc8cb283752415023a1057b44c8df8167e0417aa9e0b89f632`  
		Last Modified: Thu, 17 Oct 2024 03:11:55 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03a6c7dcb4627fcb50a0780a80643b33a0c7eb8fc97cde415a93b5d62392d81d`  
		Last Modified: Thu, 17 Oct 2024 03:12:38 GMT  
		Size: 21.5 MB (21512775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bafbf479aff109b64c60ed07d292ff0964425a857bdce0d29ae39eaa8c05d41c`  
		Last Modified: Thu, 17 Oct 2024 03:12:34 GMT  
		Size: 438.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fee26a079f6b552d2d32941008aecadbb3abf8951c2ad54afd96eb2589a1836`  
		Last Modified: Thu, 17 Oct 2024 03:12:34 GMT  
		Size: 488.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:584db09bea6ec6b6155fc3a623ecd51983cdbb1629cfc99cce71bfaf5d2ea196`  
		Last Modified: Fri, 25 Oct 2024 00:56:19 GMT  
		Size: 12.8 MB (12816277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4350e25eb1f98ee3dae5112c7d6459baf3d7aab40acc2f4ae85dda67798f0e6`  
		Last Modified: Fri, 25 Oct 2024 00:56:17 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b0886751c1238aab1e1ff3b740756fd5738877b92186c55cb723f2f9ac3ceab`  
		Last Modified: Fri, 25 Oct 2024 00:56:19 GMT  
		Size: 12.1 MB (12062124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25a500ffa840df619b013760299e9abb265522728209923622d20abaaceccd70`  
		Last Modified: Fri, 25 Oct 2024 00:56:17 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c53a0aeb45d95e5b75a8b318b775797e6ce15818dce1aebf0be8eb039b4a3139`  
		Last Modified: Fri, 25 Oct 2024 00:56:17 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a622f2db3910ea69f2c9584405e676089b7c2478eeb09405236597cdcd2326b`  
		Last Modified: Fri, 25 Oct 2024 00:56:17 GMT  
		Size: 892.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6a903898a393096c7b8ab4e88488650edd92be38e35a34a37f210d4b4e5c1bb`  
		Last Modified: Fri, 25 Oct 2024 01:20:07 GMT  
		Size: 188.8 KB (188766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b39a91f2cd9c6e3a2069d149daee5c716dd9e33a78319080327012fdf37120a4`  
		Last Modified: Fri, 25 Oct 2024 01:20:07 GMT  
		Size: 324.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e6b90fbffcc736a7309792d2d54b540ce1941533aeb2074c7868ff7f724f2b5`  
		Last Modified: Fri, 25 Oct 2024 01:20:05 GMT  
		Size: 351.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db90d7dd7be649677cbd106b1a6e8dd8c8af2bd9abfe74d50f11647467b8f478`  
		Last Modified: Fri, 25 Oct 2024 01:20:05 GMT  
		Size: 4.1 MB (4073442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d14e3085b2946376a32e82e3a4b922b07af864a83a9b6b6c07522986322b0f65`  
		Last Modified: Fri, 25 Oct 2024 01:20:04 GMT  
		Size: 2.1 KB (2052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54e0a6702ad9fe6dfcee636f99fde07c51409fbe81952ea0d995251b649a8cee`  
		Last Modified: Fri, 25 Oct 2024 01:20:04 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58e03ea7f100f37996e8813786e95b8ccace1a577c633b1bb50cecd3a4257ec5`  
		Last Modified: Fri, 25 Oct 2024 01:20:05 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:latest` - linux; s390x

```console
$ docker pull yourls@sha256:e168db51931c95c5bdc968c267e3c03e4585d587cb394310414b213d302a4d3b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.3 MB (156339386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf453493e2c1b4562af5856789d069e8dea92af80412483ec2ee89a80f5d4fc9`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 17 Oct 2024 01:46:19 GMT
ADD file:53293b1530bfd7e933ac5a321d4b0604f56c0fa25d3afeaedb0cec1938b938a3 in / 
# Thu, 17 Oct 2024 01:46:20 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 02:09:01 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 17 Oct 2024 02:09:01 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 17 Oct 2024 02:09:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 02:09:33 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 17 Oct 2024 02:09:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 17 Oct 2024 02:13:01 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 17 Oct 2024 02:13:01 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 17 Oct 2024 02:13:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Thu, 17 Oct 2024 02:13:13 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Thu, 17 Oct 2024 02:13:14 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Thu, 17 Oct 2024 02:13:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Oct 2024 02:13:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Oct 2024 02:13:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 17 Oct 2024 02:27:12 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 17 Oct 2024 02:39:32 GMT
ENV PHP_VERSION=8.3.12
# Thu, 17 Oct 2024 02:39:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.12.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.12.tar.xz.asc
# Thu, 17 Oct 2024 02:39:32 GMT
ENV PHP_SHA256=f774e28633e26fc8c5197f4dae58ec9e3ff87d1b4311cbc61ab05a7ad24bd131
# Thu, 17 Oct 2024 02:39:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 17 Oct 2024 02:39:39 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 17 Oct 2024 02:42:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 17 Oct 2024 02:42:08 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Thu, 17 Oct 2024 02:42:08 GMT
RUN docker-php-ext-enable sodium
# Thu, 17 Oct 2024 02:42:08 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 17 Oct 2024 02:42:08 GMT
STOPSIGNAL SIGWINCH
# Thu, 17 Oct 2024 02:42:08 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 17 Oct 2024 02:42:08 GMT
WORKDIR /var/www/html
# Thu, 17 Oct 2024 02:42:08 GMT
EXPOSE 80
# Thu, 17 Oct 2024 02:42:09 GMT
CMD ["apache2-foreground"]
# Thu, 17 Oct 2024 05:00:19 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli
# Thu, 17 Oct 2024 05:00:19 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Thu, 17 Oct 2024 05:00:20 GMT
RUN a2enmod rewrite expires
# Thu, 17 Oct 2024 05:00:20 GMT
ARG YOURLS_VERSION=1.9.2
# Thu, 17 Oct 2024 05:00:20 GMT
ARG YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
# Thu, 17 Oct 2024 05:00:20 GMT
ENV YOURLS_VERSION=1.9.2
# Thu, 17 Oct 2024 05:00:20 GMT
ENV YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
# Thu, 17 Oct 2024 05:00:21 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Thu, 17 Oct 2024 05:00:22 GMT
COPY --chown=www-data:www-datafile:407fa98e3948ea07c2ff8bc30ad1b3b7b28a1c2b9b5d8e5ab87f9b317a2bac85 in /usr/src/yourls/user/ 
# Thu, 17 Oct 2024 05:00:22 GMT
COPY file:50b4d483341578e719ad63fd7aaea99a0d6d7cebfb7b43d6098a656a975ee0e3 in /usr/local/bin/ 
# Thu, 17 Oct 2024 05:00:22 GMT
COPY file:5b7ff05d0c98ad759c4bec0ef8a7ce74cae42e95b42564b55f43b341c2c3e3f5 in /usr/src/yourls/ 
# Thu, 17 Oct 2024 05:00:22 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Thu, 17 Oct 2024 05:00:22 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:3544f1137f2bd42b766143fd0dc535d7e3a32f7fab936cdbc531329371bc5687`  
		Last Modified: Thu, 17 Oct 2024 01:50:31 GMT  
		Size: 27.5 MB (27490084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:641c5b42b9f8e9cc9d65697a8723928dceb047b06377f2d116b9c2a5512b08e6`  
		Last Modified: Thu, 17 Oct 2024 03:32:05 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd6e053e76a5c11aa5d9c2fad8f4e883c1ee8ecbb5f99da4b72f7d634499baa8`  
		Last Modified: Thu, 17 Oct 2024 03:32:17 GMT  
		Size: 80.8 MB (80817901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09024721ae9944c22f86461ed99527ff7d8bee6b9b1f1eff3cd1958f41748694`  
		Last Modified: Thu, 17 Oct 2024 03:32:05 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f6555ecb57349a77868c914c1f994918fb11b71be072532ae14ce8d6f30f680`  
		Last Modified: Thu, 17 Oct 2024 03:32:32 GMT  
		Size: 20.1 MB (20099005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6abd9390b6a7484b8a8e03acda3fa992d14c0fd34c5f02599c8c829380a9f9af`  
		Last Modified: Thu, 17 Oct 2024 03:32:30 GMT  
		Size: 436.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6b03dab143724a784bcb1c6b3d2011f7a1b4423744088d9ff791064fbb0355d`  
		Last Modified: Thu, 17 Oct 2024 03:32:30 GMT  
		Size: 489.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:176f8c72c85857eb6dc2ea6453992ec440206e806cf5540a82d7311ff21f1863`  
		Last Modified: Thu, 17 Oct 2024 03:34:36 GMT  
		Size: 12.8 MB (12825028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5db72fc72b018e0ab9b1d0e5b7f71c0c7134ec03d9d7c69de272986e92448fb9`  
		Last Modified: Thu, 17 Oct 2024 03:34:34 GMT  
		Size: 489.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4a39e200e5ffbd8acc6b09a944fb184550c8e54e16071c0d24d351d2746b212`  
		Last Modified: Thu, 17 Oct 2024 03:34:36 GMT  
		Size: 10.9 MB (10861738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd12bca05b392493bbd21996b98d32a777fecfa6f1bd212d2687cc568dd8efcf`  
		Last Modified: Thu, 17 Oct 2024 03:34:34 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:add332095491ad2908127a2fae1693d8d71ce82a702e57b643d93684aee676de`  
		Last Modified: Thu, 17 Oct 2024 03:34:34 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b8c823f984ee12a98362e11d2ec58f8d5c71ea28d2d7261e73c5ea8f913b47e`  
		Last Modified: Thu, 17 Oct 2024 03:34:34 GMT  
		Size: 895.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6af71793cace5fd0853a67ae5037c58b445b84365f216ed7ead31547ebab9d5`  
		Last Modified: Thu, 17 Oct 2024 05:01:11 GMT  
		Size: 162.0 KB (161983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e25d38a272ec299d057e8e1ce5c10074f6782080cd8838cf52a99549aee8d62`  
		Last Modified: Thu, 17 Oct 2024 05:01:11 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2136e6c5ee3c865dddcdd1b18df25899cedf6ba99f85e4666093e09abbf7ff81`  
		Last Modified: Thu, 17 Oct 2024 05:01:10 GMT  
		Size: 346.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:addd24e0c9b63c93847be8d76bc7cfe2edc4b33c488d1772daa7443e7ca00987`  
		Last Modified: Thu, 17 Oct 2024 05:01:11 GMT  
		Size: 4.1 MB (4073438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d5d44ca0ca4138bf71a7c5862560fd3f95e1b993974088e498d267e901e3142`  
		Last Modified: Thu, 17 Oct 2024 05:01:10 GMT  
		Size: 2.0 KB (2048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5957f71582d4bf3e675de0d44d81950b711ba25fe3ed35464d162ea8671c8cba`  
		Last Modified: Thu, 17 Oct 2024 05:01:10 GMT  
		Size: 1.7 KB (1696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fa1babc778a13818609e91a10631dd6ced9573268286aa0d1bfcc46bb52b7a0`  
		Last Modified: Thu, 17 Oct 2024 05:01:10 GMT  
		Size: 331.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
