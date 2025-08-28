## `yourls:1-apache`

```console
$ docker pull yourls@sha256:a7f3a5edc7d115addb98a90c603571074dda426ea0b8242d512300bc4d93480d
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
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `yourls:1-apache` - linux; amd64

```console
$ docker pull yourls@sha256:c553458dff820580685e39b38027d3f9edfc3a1df88badd69288ae8965747c5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.6 MB (186604384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a980c734e7bae68a3dbebb5a15b07a007acea600c542d080dafae9e60d021f66`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 19 Aug 2025 10:14:17 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 19 Aug 2025 10:14:17 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_VERSION=8.4.12
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.12.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.12.tar.xz.asc
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_SHA256=c1b7978cbb5054eed6c749bde4444afc16a3f2268101fb70a7d5d9b1083b12ad
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 19 Aug 2025 10:14:17 GMT
STOPSIGNAL SIGWINCH
# Tue, 19 Aug 2025 10:14:17 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
WORKDIR /var/www/html
# Tue, 19 Aug 2025 10:14:17 GMT
EXPOSE map[80/tcp:{}]
# Tue, 19 Aug 2025 10:14:17 GMT
CMD ["apache2-foreground"]
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
RUN a2enmod rewrite expires # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
ARG YOURLS_VERSION=1.10.2
# Tue, 19 Aug 2025 10:14:17 GMT
ARG YOURLS_SHA256=c1a5c35d4f47c322d29adffb1a89642544e609808561cf340dc046af58a900e8
# Tue, 19 Aug 2025 10:14:17 GMT
ENV YOURLS_VERSION=1.10.2
# Tue, 19 Aug 2025 10:14:17 GMT
ENV YOURLS_SHA256=c1a5c35d4f47c322d29adffb1a89642544e609808561cf340dc046af58a900e8
# Tue, 19 Aug 2025 10:14:17 GMT
# ARGS: YOURLS_VERSION=1.10.2 YOURLS_SHA256=c1a5c35d4f47c322d29adffb1a89642544e609808561cf340dc046af58a900e8
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
COPY files/vhost.conf /etc/apache2/sites-available/000-default.conf # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
COPY files/vhost-https.conf /etc/apache2/sites-available/default-ssl.conf # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
COPY files/ports.conf /etc/apache2/ports.conf # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 19 Aug 2025 10:14:17 GMT
EXPOSE map[8443/tcp:{}]
# Tue, 19 Aug 2025 10:14:17 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Tue, 19 Aug 2025 10:14:17 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:396b1da7636e2dcd10565cb4f2f952cbb4a8a38b58d3b86a2cacb172fb70117c`  
		Last Modified: Tue, 12 Aug 2025 20:45:08 GMT  
		Size: 29.8 MB (29773285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be7d57eb145c727fd42bea60344c7374f0d3436415e0d8fea06bab5f9dcc9c45`  
		Last Modified: Thu, 28 Aug 2025 18:19:05 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83e84808a09800799297467cf6757d23c36562d0421500eaa8009eb830ff25f6`  
		Last Modified: Thu, 28 Aug 2025 18:19:18 GMT  
		Size: 117.8 MB (117834245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4f3f0775bd8677e6d9afebece0e64068654133cca804a58a4142c5cc0ba3acd`  
		Last Modified: Thu, 28 Aug 2025 18:19:05 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c6890624c3adfd3a1bdc9a1ef87167aba9c9bd9382f349d8a8c55bc069d1114`  
		Last Modified: Thu, 28 Aug 2025 18:19:06 GMT  
		Size: 4.2 MB (4223789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98bd81635072caae8c0b139876c6d9b269da7bf704e28c802cb1e0e7fff6a831`  
		Last Modified: Thu, 28 Aug 2025 18:19:05 GMT  
		Size: 426.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf3904703ccac320dcd3fea48bf1395eeb0af10650168ea9027fadc28d22d4af`  
		Last Modified: Thu, 28 Aug 2025 18:19:06 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0b15de76778c4ac6b1ce195f0b9d465a745e80b364692f2ce9bb2c5e88d0a1a`  
		Last Modified: Thu, 28 Aug 2025 18:19:07 GMT  
		Size: 13.8 MB (13802580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c67916c4c9c0b021b7f6e8c647f0e89e2e8b33471b32a11bc8fa6eb9d333a6bb`  
		Last Modified: Thu, 28 Aug 2025 18:19:06 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fc7f2ed1b3a7ee51cacd4118eb95dffd40d1c2e75da8974f19a337b2085330a`  
		Last Modified: Thu, 28 Aug 2025 18:19:07 GMT  
		Size: 14.2 MB (14213470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd3ca3df03da55c3ccd7f38281517a945a9586d7712f53b567c2036805b06722`  
		Last Modified: Thu, 28 Aug 2025 18:19:06 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72763bb5b9c3240e370543e7c38685af83c59973aeaa4704bdf092769c0f09e4`  
		Last Modified: Thu, 28 Aug 2025 18:19:06 GMT  
		Size: 253.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2215e01ad48ec0310d339a14ec84809a59d1a851365e368eb4cf3d2a2d5cfafb`  
		Last Modified: Thu, 28 Aug 2025 18:19:06 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02a5f0483900ed4d9e0c336398717361227c642959be4e5925d0723ea85069ee`  
		Last Modified: Thu, 28 Aug 2025 18:19:06 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7837a013a6248f3fc8ad7804b4bb76f17cff1fec1b8eb230f512c50c9359e7b3`  
		Last Modified: Thu, 28 Aug 2025 18:55:32 GMT  
		Size: 671.8 KB (671815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d147bf7116f35f30312fc2dc3e3aa05587b5f13956f35056010cf9fcc369b3a`  
		Last Modified: Thu, 28 Aug 2025 18:55:32 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e2f57d0574f69b6c3244c7fbeae5aa7339d463b51e2e14777a57a441b5f0b76`  
		Last Modified: Thu, 28 Aug 2025 18:55:32 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10c5e5b6a7dbb34923f4d2e5d2806f8b235379421342ee91ea8d33802cbf14bd`  
		Last Modified: Thu, 28 Aug 2025 18:55:32 GMT  
		Size: 6.1 MB (6073643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d28829cb5a6f8aa72eb1fa5dcfd30b592ff60135f26f107a9cf94aca9998402`  
		Last Modified: Thu, 28 Aug 2025 18:55:32 GMT  
		Size: 2.1 KB (2095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31d8c3764e4ece0f2195945b9458ba024b6efcc4d9240567d4da05d00306bf0e`  
		Last Modified: Thu, 28 Aug 2025 18:55:32 GMT  
		Size: 1.7 KB (1694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:919fa98af4aa39a60e3a7a79736e827789b8029e1122356384166e0c87a605b7`  
		Last Modified: Thu, 28 Aug 2025 18:55:32 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b10f30037e1303f0697249a932a3006aa5013d9ab60c5866742f7566e36414e4`  
		Last Modified: Thu, 28 Aug 2025 18:55:32 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:528c60060404e9fb152decd61d819c975755a7c86b806c1821d5f4172647455e`  
		Last Modified: Thu, 28 Aug 2025 18:55:33 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:1-apache` - unknown; unknown

```console
$ docker pull yourls@sha256:1cf614fd2d19612cb08cce79efc0b21297b9c834d083c7d3bf3b198f7f0c16da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 KB (49058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c03c5444f8410ac257db945bd9f236193986d0edb7d5c1e218e963fba851b705`

```dockerfile
```

-	Layers:
	-	`sha256:a49c53b48f269b060ad13d2b0d7bed8120ac86d99ce6205737dae13a618e3663`  
		Last Modified: Thu, 28 Aug 2025 19:42:31 GMT  
		Size: 49.1 KB (49058 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:1-apache` - linux; arm variant v5

```console
$ docker pull yourls@sha256:a2b1e687913288fb3e9e7dcd6051d960f5c23b70f8016d8041b65b45bb18b134
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.8 MB (159847429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:751a667b7460987b04cb157a1dcf15a91baac5c9dd00bcbb6e6d6205bd987707`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1754870400'
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 19 Aug 2025 10:14:17 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 19 Aug 2025 10:14:17 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_VERSION=8.4.12
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.12.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.12.tar.xz.asc
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_SHA256=c1b7978cbb5054eed6c749bde4444afc16a3f2268101fb70a7d5d9b1083b12ad
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 19 Aug 2025 10:14:17 GMT
STOPSIGNAL SIGWINCH
# Tue, 19 Aug 2025 10:14:17 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
WORKDIR /var/www/html
# Tue, 19 Aug 2025 10:14:17 GMT
EXPOSE map[80/tcp:{}]
# Tue, 19 Aug 2025 10:14:17 GMT
CMD ["apache2-foreground"]
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
RUN a2enmod rewrite expires # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
ARG YOURLS_VERSION=1.10.2
# Tue, 19 Aug 2025 10:14:17 GMT
ARG YOURLS_SHA256=c1a5c35d4f47c322d29adffb1a89642544e609808561cf340dc046af58a900e8
# Tue, 19 Aug 2025 10:14:17 GMT
ENV YOURLS_VERSION=1.10.2
# Tue, 19 Aug 2025 10:14:17 GMT
ENV YOURLS_SHA256=c1a5c35d4f47c322d29adffb1a89642544e609808561cf340dc046af58a900e8
# Tue, 19 Aug 2025 10:14:17 GMT
# ARGS: YOURLS_VERSION=1.10.2 YOURLS_SHA256=c1a5c35d4f47c322d29adffb1a89642544e609808561cf340dc046af58a900e8
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
COPY files/vhost.conf /etc/apache2/sites-available/000-default.conf # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
COPY files/vhost-https.conf /etc/apache2/sites-available/default-ssl.conf # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
COPY files/ports.conf /etc/apache2/ports.conf # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 19 Aug 2025 10:14:17 GMT
EXPOSE map[8443/tcp:{}]
# Tue, 19 Aug 2025 10:14:17 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Tue, 19 Aug 2025 10:14:17 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:498399880872f14c562c46bd2a1ef4cfcf3c2a1453514ff0d0f6b7d89f8010dd`  
		Last Modified: Tue, 12 Aug 2025 22:02:01 GMT  
		Size: 27.9 MB (27941706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b826fc1a1d535eacc028e3d956ad4684d2277457bc010244dfb267e133817510`  
		Last Modified: Wed, 13 Aug 2025 02:04:17 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e5554cad66c2c0be3db0dee9e2828bb1216178113d28498a470e272f7c87a2e`  
		Last Modified: Wed, 13 Aug 2025 04:31:51 GMT  
		Size: 94.9 MB (94871877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bad6001493531fd836717f5de4d6b19cb18c7fe4e2c9d0cbbcb80e66609bd4b`  
		Last Modified: Wed, 13 Aug 2025 02:04:23 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b50afdc142e6451ef7d9c32421123cfbe0fab27ee11ac3d01ad799f077fac415`  
		Last Modified: Wed, 13 Aug 2025 01:57:53 GMT  
		Size: 4.1 MB (4081709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17530c1a395b92b1493543369514c8f70e81f42721c7499a87f81b39f1f89d21`  
		Last Modified: Wed, 13 Aug 2025 01:57:52 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fb201a9f7aa65c612ce8382e34904f44e078b655ce6f72b1852a84c50f00e8f`  
		Last Modified: Wed, 13 Aug 2025 01:57:53 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e36a512e25c5e9aede0185ef0a8bdc8004b95ac3ee5d595140f1aab0b9c3fbd`  
		Last Modified: Thu, 28 Aug 2025 18:27:44 GMT  
		Size: 13.8 MB (13813231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa2d245e1d6ac5985a9cb5c306c35373f641fddc324cd3fd1efbdeffcd43e899`  
		Last Modified: Thu, 28 Aug 2025 18:27:38 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61c6d5bfe44dc003ca361372b6d2d958bc9a5b936f5762a20b485de4fc4dfbaf`  
		Last Modified: Thu, 28 Aug 2025 18:27:39 GMT  
		Size: 12.9 MB (12878879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93b789fa480c610fb53b2dc0cc453ed1827b98b62f4eb42a7e1fdf76317b84e9`  
		Last Modified: Thu, 28 Aug 2025 18:27:38 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61874435906c90634188db8426824b0627d4f6708f8d8db1a2b79e13de94712c`  
		Last Modified: Thu, 28 Aug 2025 18:27:38 GMT  
		Size: 253.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c704a47563339084e7074780a866a73c84da2e515b563a4c70d3d671b056e095`  
		Last Modified: Thu, 28 Aug 2025 18:27:38 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02c6815014cf87aff61acc72c33379fd16c9eb2ade1f72af85e4f47425abf6d5`  
		Last Modified: Thu, 28 Aug 2025 18:27:38 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01cde207a8ebb6120fb5f57ec18a57aab6711400c1ac4b91c81c73ebd4126842`  
		Last Modified: Thu, 28 Aug 2025 19:54:04 GMT  
		Size: 174.8 KB (174782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0532f6e91e378c0d7ef73bacc2ee5a6f468bc4e54625320cc5cdf3b7be736ed`  
		Last Modified: Thu, 28 Aug 2025 19:54:03 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c6a375f025e163ae104df05abcd70340bb633ee78c9856457d394ac6b985a18`  
		Last Modified: Thu, 28 Aug 2025 19:54:03 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6705dfbf4b12e1263b08d5bdd381dc86fa4719aa809568f1e896ed60aa80351c`  
		Last Modified: Thu, 28 Aug 2025 19:54:04 GMT  
		Size: 6.1 MB (6073642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:617dd777c79720c6059bec1387b1e8abc34ccbd62a35838ab5601b2e9ffcbd0b`  
		Last Modified: Thu, 28 Aug 2025 19:54:03 GMT  
		Size: 2.1 KB (2095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9aeae45a8328bc43f17d4985721f33c448b2d2dc1ed3261369490a69d7b263d`  
		Last Modified: Thu, 28 Aug 2025 19:54:03 GMT  
		Size: 1.7 KB (1697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a5307504f4a688db5cdd6f6d4df4a3d248d3a1265508101286c7a6c438248db`  
		Last Modified: Thu, 28 Aug 2025 19:54:03 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1691dff51b4e0ecf86efafe64f1ea2a59f7b793e692587c57ce84f5bee0a04c1`  
		Last Modified: Thu, 28 Aug 2025 19:54:04 GMT  
		Size: 553.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4697dcb896c9081519649df08696011460ade3ccf58395b1ebc40c9a1662e31`  
		Last Modified: Thu, 28 Aug 2025 19:54:04 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:1-apache` - unknown; unknown

```console
$ docker pull yourls@sha256:aa49aa50db4de731a841c173de0f1a6c96c4f0cf5ec2317aafa20fb9bfd2dd0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 KB (49195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83a410fd8137fcf42cf0e60ad3f3229e84595e6fce9d1bd296281b7015a6aa21`

```dockerfile
```

-	Layers:
	-	`sha256:fd4d35dff1c8651d0097bc5e69ed77da8da739c1d79918feb984cb9116bd07a7`  
		Last Modified: Thu, 28 Aug 2025 22:42:46 GMT  
		Size: 49.2 KB (49195 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:1-apache` - linux; arm variant v7

```console
$ docker pull yourls@sha256:3d20f7fd9427223ab305395bc6fd0a915bb5bf3df827a3f739a6088bf790cb43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.5 MB (148548930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:010cf3a28aae6b7eabd03d31da5204549f7ab48cd2089f5391b4d5f3f792b26c`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1754870400'
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 19 Aug 2025 10:14:17 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 19 Aug 2025 10:14:17 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_VERSION=8.4.12
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.12.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.12.tar.xz.asc
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_SHA256=c1b7978cbb5054eed6c749bde4444afc16a3f2268101fb70a7d5d9b1083b12ad
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 19 Aug 2025 10:14:17 GMT
STOPSIGNAL SIGWINCH
# Tue, 19 Aug 2025 10:14:17 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
WORKDIR /var/www/html
# Tue, 19 Aug 2025 10:14:17 GMT
EXPOSE map[80/tcp:{}]
# Tue, 19 Aug 2025 10:14:17 GMT
CMD ["apache2-foreground"]
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
RUN a2enmod rewrite expires # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
ARG YOURLS_VERSION=1.10.2
# Tue, 19 Aug 2025 10:14:17 GMT
ARG YOURLS_SHA256=c1a5c35d4f47c322d29adffb1a89642544e609808561cf340dc046af58a900e8
# Tue, 19 Aug 2025 10:14:17 GMT
ENV YOURLS_VERSION=1.10.2
# Tue, 19 Aug 2025 10:14:17 GMT
ENV YOURLS_SHA256=c1a5c35d4f47c322d29adffb1a89642544e609808561cf340dc046af58a900e8
# Tue, 19 Aug 2025 10:14:17 GMT
# ARGS: YOURLS_VERSION=1.10.2 YOURLS_SHA256=c1a5c35d4f47c322d29adffb1a89642544e609808561cf340dc046af58a900e8
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
COPY files/vhost.conf /etc/apache2/sites-available/000-default.conf # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
COPY files/vhost-https.conf /etc/apache2/sites-available/default-ssl.conf # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
COPY files/ports.conf /etc/apache2/ports.conf # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 19 Aug 2025 10:14:17 GMT
EXPOSE map[8443/tcp:{}]
# Tue, 19 Aug 2025 10:14:17 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Tue, 19 Aug 2025 10:14:17 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:d480d07cd33d2a61cb24d871a17254661d250ae887a2db15a7e99cb67383a74e`  
		Last Modified: Tue, 12 Aug 2025 20:52:10 GMT  
		Size: 26.2 MB (26207488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f783066fe233d49b725a424d9e4e2edf03ec368e8008a7100235b31d55c72428`  
		Last Modified: Wed, 13 Aug 2025 03:03:11 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:def7928390388cc2020246549215f695478752f6ae67568af1344eee2f6088ce`  
		Last Modified: Wed, 13 Aug 2025 03:03:28 GMT  
		Size: 86.2 MB (86243176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5decd14e90655d8988225e174f3bef3fbd8abee342388203104f64e9516432f7`  
		Last Modified: Wed, 13 Aug 2025 03:03:11 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:372110111ee86e66c1b99c7148a9a3a4e350c9b9c4843f501f3c831128011fe3`  
		Last Modified: Wed, 13 Aug 2025 03:08:13 GMT  
		Size: 3.8 MB (3751774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:721b3bcfb16aff30d3a16d797f1847f5686541c5e5390e6d2d1d8e947baa2f68`  
		Last Modified: Wed, 13 Aug 2025 03:08:11 GMT  
		Size: 434.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0fb1db8d532ffaa5e1f6b0f06e0e76396d505ed544ca2b1636fa7de235e998e`  
		Last Modified: Wed, 13 Aug 2025 03:08:11 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15c8bcfc0b5f2af29c6fa2719fa75049aac7700b0afaf910dc1eedc2a344ca9e`  
		Last Modified: Thu, 28 Aug 2025 18:27:09 GMT  
		Size: 13.8 MB (13813356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb11a6d60f7744c66b32a9231ddd8f24fb1dd77dc27e5f6d03697492c885d8b9`  
		Last Modified: Thu, 28 Aug 2025 18:27:07 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56fb861533277915a1de63fb5de3ca7c1d9eb3e64a898026370c9516dce108f0`  
		Last Modified: Thu, 28 Aug 2025 18:27:08 GMT  
		Size: 12.3 MB (12286498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29d8fe9f632da0ebf1a625dd1ee712095009d54c73cc05cbff939284013e94b0`  
		Last Modified: Thu, 28 Aug 2025 18:27:07 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e5c2bc75353a0f2e1d1ebcbcfeb7479dba1c366382ee31f4788f3724e478965`  
		Last Modified: Thu, 28 Aug 2025 18:27:07 GMT  
		Size: 253.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ce23df2cebdad049308df94268747e4b32c14ad6fc68a17bd114ee5eaf9f776`  
		Last Modified: Thu, 28 Aug 2025 18:27:07 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f23eefdc8501db9313e0feb50cea365dd37c9ecf8e529ba136ad4f1eafcd87de`  
		Last Modified: Thu, 28 Aug 2025 18:27:07 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39197ecabb10d4824e0b8c32faaa79acbcfbe70b3cbf59bf563068c076971c31`  
		Last Modified: Thu, 28 Aug 2025 20:42:45 GMT  
		Size: 161.4 KB (161411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a88298436a48693e54d04f07db402b2b04732dcc172153e63dbd97fe4f64d58`  
		Last Modified: Thu, 28 Aug 2025 20:42:45 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:467d61963fc2ca5355aedf9dd861fee3e456d2fb2b3bfa84fc256c283ba9f32b`  
		Last Modified: Thu, 28 Aug 2025 20:42:45 GMT  
		Size: 354.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bb8fe54bc36c6d58f4428f3c943a028bbf4becd6d362431584aa99b2dcfb154`  
		Last Modified: Thu, 28 Aug 2025 20:42:46 GMT  
		Size: 6.1 MB (6073642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c878372f6987a3fc9a8cf623dcca3c08fa28fe90caa55a8d1db84f0ee83424e`  
		Last Modified: Thu, 28 Aug 2025 20:42:45 GMT  
		Size: 2.1 KB (2092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52c8ccbc874e117fcc717d6c1055e473f4e61d1d8efc73b288d7c3715c5b9dcd`  
		Last Modified: Thu, 28 Aug 2025 20:42:46 GMT  
		Size: 1.7 KB (1693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bfea8ea2482e3790ede3d75dd6615df166836469949c65a198c8ebdc9ded8b8`  
		Last Modified: Thu, 28 Aug 2025 20:42:46 GMT  
		Size: 502.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbd506bc63541b5607e34d88a84b9f2b5fad81827dfd4e47a26ebc29c7605c8c`  
		Last Modified: Thu, 28 Aug 2025 20:42:45 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0ee03a4b58877fe1d7f4fbd42f8100f0c8e255dc9db18d541e42b2e36bba214`  
		Last Modified: Thu, 28 Aug 2025 20:42:46 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:1-apache` - unknown; unknown

```console
$ docker pull yourls@sha256:69042b8becda8bd9618c4cf0b21a5934251473ddd5b7c59e2217760bbc9c2cfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 KB (49195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b57af3d30bdfedbe626f71172f714a09cd7c11ace46289b0b4f765a84df5574d`

```dockerfile
```

-	Layers:
	-	`sha256:1443eda86a3258e5ece097fc5264b033b0e9f2a94ea90809027dedeb5a7b90c8`  
		Last Modified: Thu, 28 Aug 2025 22:42:49 GMT  
		Size: 49.2 KB (49195 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:1-apache` - linux; arm64 variant v8

```console
$ docker pull yourls@sha256:3f1c76a79c92f82bbad1562e3dad2ec1ed440ad42728e6b3e7a4e4ce660e0902
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.9 MB (178948800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cd62238177ab3c69c79bb59c7764acde9092e533456b989be01daba42c2946f`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 19 Aug 2025 10:14:17 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 19 Aug 2025 10:14:17 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_VERSION=8.4.12
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.12.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.12.tar.xz.asc
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_SHA256=c1b7978cbb5054eed6c749bde4444afc16a3f2268101fb70a7d5d9b1083b12ad
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 19 Aug 2025 10:14:17 GMT
STOPSIGNAL SIGWINCH
# Tue, 19 Aug 2025 10:14:17 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
WORKDIR /var/www/html
# Tue, 19 Aug 2025 10:14:17 GMT
EXPOSE map[80/tcp:{}]
# Tue, 19 Aug 2025 10:14:17 GMT
CMD ["apache2-foreground"]
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
RUN a2enmod rewrite expires # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
ARG YOURLS_VERSION=1.10.2
# Tue, 19 Aug 2025 10:14:17 GMT
ARG YOURLS_SHA256=c1a5c35d4f47c322d29adffb1a89642544e609808561cf340dc046af58a900e8
# Tue, 19 Aug 2025 10:14:17 GMT
ENV YOURLS_VERSION=1.10.2
# Tue, 19 Aug 2025 10:14:17 GMT
ENV YOURLS_SHA256=c1a5c35d4f47c322d29adffb1a89642544e609808561cf340dc046af58a900e8
# Tue, 19 Aug 2025 10:14:17 GMT
# ARGS: YOURLS_VERSION=1.10.2 YOURLS_SHA256=c1a5c35d4f47c322d29adffb1a89642544e609808561cf340dc046af58a900e8
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
COPY files/vhost.conf /etc/apache2/sites-available/000-default.conf # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
COPY files/vhost-https.conf /etc/apache2/sites-available/default-ssl.conf # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
COPY files/ports.conf /etc/apache2/ports.conf # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 19 Aug 2025 10:14:17 GMT
EXPOSE map[8443/tcp:{}]
# Tue, 19 Aug 2025 10:14:17 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Tue, 19 Aug 2025 10:14:17 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef1ee6d029e615fa2b873890f1011a42f1c5f78b2d100eaed3bc1df5bb73d212`  
		Last Modified: Thu, 14 Aug 2025 22:21:29 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a472e922e809f2164e7de33f1a04d157980da1614d66407be60d248980ca8453`  
		Last Modified: Thu, 14 Aug 2025 22:21:38 GMT  
		Size: 110.2 MB (110160334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48fe053e93cb40a6c44acd9d0ab0ee960880abe08bd106a21947710df1e0399e`  
		Last Modified: Thu, 14 Aug 2025 22:21:29 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc43ae40cfafdbc816c6ef33e29cb3a5b1fcd866e77ed316da93e7ac7be457bc`  
		Last Modified: Thu, 14 Aug 2025 22:29:04 GMT  
		Size: 4.3 MB (4301251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c0c909ee690af4ad403bf2728df6cf54495afc197ec0612503debdb1a0d47a`  
		Last Modified: Thu, 14 Aug 2025 22:29:05 GMT  
		Size: 436.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5af3640212feddb52a07b6b7e3a5ba254dfe8302593969022dfcddb394f0e87`  
		Last Modified: Thu, 14 Aug 2025 22:29:05 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1daf55e39b8126f74c52f6253c906ea84934371c6a272c67689d11c8fc8829e`  
		Last Modified: Thu, 28 Aug 2025 19:14:38 GMT  
		Size: 13.8 MB (13815497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aa06473af9f67a470b5836fa9b35aa11379ce2596782cc5894c150f0f2a2deb`  
		Last Modified: Thu, 28 Aug 2025 19:14:37 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b009c6bfbc2ef0214cceff30da2d6f09600ff62e478178de9bcdb99bca857132`  
		Last Modified: Thu, 28 Aug 2025 19:14:38 GMT  
		Size: 13.9 MB (13862809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7b879e84d791419704f93b2a6eac9a44bee31143f9dacae08b2d1f2111260ab`  
		Last Modified: Thu, 28 Aug 2025 19:14:37 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce23f515033bf0a548f09833ff8d89fc5ca6d406a8d7c9009db570707fc680f1`  
		Last Modified: Thu, 28 Aug 2025 19:14:37 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b848ff217f15bc996ee6025a4b101c6d48c5b5607715eecfd95a0d83de02c92`  
		Last Modified: Thu, 28 Aug 2025 19:14:38 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a341f2f20c41eec58aa194f9baf64e2a60bef69d9b5185c144e4221b6c31cfe6`  
		Last Modified: Thu, 28 Aug 2025 19:14:38 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f16543ad3e9afbcaef20ae4873da3dd99f9e7f0fd1fc809a994ee4b5635d18cb`  
		Last Modified: Thu, 28 Aug 2025 20:48:55 GMT  
		Size: 587.7 KB (587654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7de237653effca7fedaa4897b10dc4db010890979b9d49652afaeac75116eab5`  
		Last Modified: Thu, 28 Aug 2025 20:48:55 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fdbda08ee278a8d63df26de8592a9ff1bd17546dcda38577d77be744c9dea47`  
		Last Modified: Thu, 28 Aug 2025 20:48:55 GMT  
		Size: 347.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9e35c9ced973f459710ea52db5a6a83f34c54a1b4575e3a6c90204eca29280e`  
		Last Modified: Thu, 28 Aug 2025 20:48:55 GMT  
		Size: 6.1 MB (6073646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb0e915731bf670767a187004395bb3493f2a6c187e5c1a587860925e361f1ff`  
		Last Modified: Thu, 28 Aug 2025 20:48:54 GMT  
		Size: 2.1 KB (2092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20da5faed11192dda7f5dfaa0749cc769cce00644646ba273ce3d56b75eb0a47`  
		Last Modified: Thu, 28 Aug 2025 20:48:55 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c553eea8c0c51a564a39965a302807cbdb1266060eb15fe68f0fa9f6823e48bc`  
		Last Modified: Thu, 28 Aug 2025 20:48:55 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d308e803686608d046981138454f4d663f23dfc318bd6c114bc9799849bd0995`  
		Last Modified: Thu, 28 Aug 2025 20:48:55 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aed6dadd3d0ffd4f00046157394ff6e0890eac86fe0ae7d70a0c524a25c87c3`  
		Last Modified: Thu, 28 Aug 2025 20:48:55 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:1-apache` - unknown; unknown

```console
$ docker pull yourls@sha256:776c523407d2f4e2d738d30e3dfad19af22122cfc41160cccb60cd36ebadda4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 KB (49255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1f57f5dfe2bc171a3174e8665fe4dc6ad9050e2bf6a07a01a549ef312e05e08`

```dockerfile
```

-	Layers:
	-	`sha256:1f6a6285f48e919c38dc82699b896c826667c0fe9fb3b4013a1f6ff521927481`  
		Last Modified: Thu, 28 Aug 2025 22:42:53 GMT  
		Size: 49.3 KB (49255 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:1-apache` - linux; 386

```console
$ docker pull yourls@sha256:732af9ff4237d0d9545d48ba4b3e61b88497a559737a35ea410b8df5c5c0296b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.0 MB (186967508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58d3554bd339bc1f79b5dc67b1f8f569f27748188445709eb7918d61d8973c88`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1754870400'
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 19 Aug 2025 10:14:17 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 19 Aug 2025 10:14:17 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_VERSION=8.4.12
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.12.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.12.tar.xz.asc
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_SHA256=c1b7978cbb5054eed6c749bde4444afc16a3f2268101fb70a7d5d9b1083b12ad
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 19 Aug 2025 10:14:17 GMT
STOPSIGNAL SIGWINCH
# Tue, 19 Aug 2025 10:14:17 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
WORKDIR /var/www/html
# Tue, 19 Aug 2025 10:14:17 GMT
EXPOSE map[80/tcp:{}]
# Tue, 19 Aug 2025 10:14:17 GMT
CMD ["apache2-foreground"]
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
RUN a2enmod rewrite expires # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
ARG YOURLS_VERSION=1.10.2
# Tue, 19 Aug 2025 10:14:17 GMT
ARG YOURLS_SHA256=c1a5c35d4f47c322d29adffb1a89642544e609808561cf340dc046af58a900e8
# Tue, 19 Aug 2025 10:14:17 GMT
ENV YOURLS_VERSION=1.10.2
# Tue, 19 Aug 2025 10:14:17 GMT
ENV YOURLS_SHA256=c1a5c35d4f47c322d29adffb1a89642544e609808561cf340dc046af58a900e8
# Tue, 19 Aug 2025 10:14:17 GMT
# ARGS: YOURLS_VERSION=1.10.2 YOURLS_SHA256=c1a5c35d4f47c322d29adffb1a89642544e609808561cf340dc046af58a900e8
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
COPY files/vhost.conf /etc/apache2/sites-available/000-default.conf # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
COPY files/vhost-https.conf /etc/apache2/sites-available/default-ssl.conf # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
COPY files/ports.conf /etc/apache2/ports.conf # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 19 Aug 2025 10:14:17 GMT
EXPOSE map[8443/tcp:{}]
# Tue, 19 Aug 2025 10:14:17 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Tue, 19 Aug 2025 10:14:17 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:346d0c953bdbc38917a27a6f30726e5b46419d98ecaf4d2d8f201bc3b7025e57`  
		Last Modified: Tue, 12 Aug 2025 20:45:00 GMT  
		Size: 31.3 MB (31289378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba52183d0662821bae443d97871b085d0bc60505c7deb7b350f08ccf9621a3b4`  
		Last Modified: Thu, 28 Aug 2025 18:19:48 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b81b95736d42dcad298b1a99ec5d7cf65d7a1a2057b9fd4902f6d39e1cc322b`  
		Last Modified: Thu, 28 Aug 2025 18:20:00 GMT  
		Size: 116.1 MB (116135170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a65d9e7bf4a5d2c5719dca9109f0e7737c76b663d170c9615fcc8c7abef84625`  
		Last Modified: Thu, 28 Aug 2025 18:19:49 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16d6d52760a95f9b3ddac4226928965599cf7a6efe654fb36a28b834937184eb`  
		Last Modified: Thu, 28 Aug 2025 18:19:50 GMT  
		Size: 4.5 MB (4455055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f61d06578fdbacc02983e45f0477e6dfb98ff4ceb7248025d60c0e97c78d83a8`  
		Last Modified: Thu, 28 Aug 2025 18:19:49 GMT  
		Size: 427.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb9da60ef281aea664c931de61ad8f417b406e38eaeb38aec7671793f580c5b2`  
		Last Modified: Thu, 28 Aug 2025 18:19:49 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bfd27741aa2ca7d1b6e75e31854baafa672a628e07f436d6ec00ad347bfddc5`  
		Last Modified: Thu, 28 Aug 2025 18:19:52 GMT  
		Size: 13.8 MB (13801472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb4220e66a6bf35b34a3bb5baeb56f91170408b9ab942fd847656d2269db9b3d`  
		Last Modified: Thu, 28 Aug 2025 18:19:49 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73a81d9c2a6514d42205201ffa10bd82e75e6afde82f6879c06a34389fdd35ad`  
		Last Modified: Thu, 28 Aug 2025 18:19:51 GMT  
		Size: 14.5 MB (14506072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83f805e0a1ecac6676d1958760954d8079c5012f082801852ed352b91fead4c6`  
		Last Modified: Thu, 28 Aug 2025 18:19:50 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:649f19a8e86e798e66b31ac499b953a5bc361deef04309a6be4455054e1cd34b`  
		Last Modified: Thu, 28 Aug 2025 18:19:50 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0323412794631e0e5a6ee30ff4bf2c610a01b536eff6a8eff11e02dcf52c0642`  
		Last Modified: Thu, 28 Aug 2025 18:19:50 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33b650e102499a255a77af1c27412e31dc58585043eb876ec12784751cf1ab5b`  
		Last Modified: Thu, 28 Aug 2025 18:19:50 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:665b7a513d904f8b78ffe3152609931e88e60a189e8027d529a8797398f1e1d0`  
		Last Modified: Thu, 28 Aug 2025 18:55:33 GMT  
		Size: 695.2 KB (695157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d152850b84acf57789a8156e6e8e73bac353c1581611c14604ae81b95da8399c`  
		Last Modified: Thu, 28 Aug 2025 18:55:33 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7d2ded9485158b1442b3ec2d806adb6a32f61e192440b57333587d0a7c26893`  
		Last Modified: Thu, 28 Aug 2025 18:55:33 GMT  
		Size: 342.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2f9f66322d0fdb3c5d9be9364d4fd5f7f4c885b3ca621ec40cc7a6c835c88d8`  
		Last Modified: Thu, 28 Aug 2025 18:55:35 GMT  
		Size: 6.1 MB (6073643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5128ee2978e3c64a20e45877aa3bb261ee4bcc946aaeeecbefa1e27142dde82d`  
		Last Modified: Thu, 28 Aug 2025 18:55:33 GMT  
		Size: 2.1 KB (2095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c354f0c429c214123120d978d63a0f7f2e3794c20678d5d7a6470acba2af0518`  
		Last Modified: Thu, 28 Aug 2025 18:55:34 GMT  
		Size: 1.7 KB (1694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b99a571f5062553b1c3dce024ad05880d78965cd95bfd9595788a48bf7e1d419`  
		Last Modified: Thu, 28 Aug 2025 18:55:33 GMT  
		Size: 501.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5a40d2a745b4f03fd8a4d2c5e1c94a70872420fea462280af98ca7643c3662e`  
		Last Modified: Thu, 28 Aug 2025 18:55:33 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35ac405efe950cbac19b8ea3b8bc2ac075159ae37a1edddf48aa59e0c3e1e6f0`  
		Last Modified: Thu, 28 Aug 2025 18:55:33 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:1-apache` - unknown; unknown

```console
$ docker pull yourls@sha256:409f9369776fc15bd7d0e84ece4d22d938fd48c5eafa2b72db52e977de33fccb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 KB (49000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e589384ffc32488d833661e3da844af3dfa020a2e8424d36a7389f1a81b09942`

```dockerfile
```

-	Layers:
	-	`sha256:833dca4b9940d132fbd629f7a730414fb847af90c73cd5fc1023175021b30ca2`  
		Last Modified: Thu, 28 Aug 2025 19:42:41 GMT  
		Size: 49.0 KB (49000 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:1-apache` - linux; ppc64le

```console
$ docker pull yourls@sha256:1721db6c90f716862c0f783a5126fcf6730189c8d7a10c9665e2dc241294dde2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.8 MB (182789101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1151b2e9b7e4bcc202207f5a8cc82b964b63720b22f793388f811ad9da789c03`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1754870400'
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 19 Aug 2025 10:14:17 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 19 Aug 2025 10:14:17 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_VERSION=8.4.12
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.12.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.12.tar.xz.asc
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_SHA256=c1b7978cbb5054eed6c749bde4444afc16a3f2268101fb70a7d5d9b1083b12ad
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 19 Aug 2025 10:14:17 GMT
STOPSIGNAL SIGWINCH
# Tue, 19 Aug 2025 10:14:17 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
WORKDIR /var/www/html
# Tue, 19 Aug 2025 10:14:17 GMT
EXPOSE map[80/tcp:{}]
# Tue, 19 Aug 2025 10:14:17 GMT
CMD ["apache2-foreground"]
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
RUN a2enmod rewrite expires # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
ARG YOURLS_VERSION=1.10.2
# Tue, 19 Aug 2025 10:14:17 GMT
ARG YOURLS_SHA256=c1a5c35d4f47c322d29adffb1a89642544e609808561cf340dc046af58a900e8
# Tue, 19 Aug 2025 10:14:17 GMT
ENV YOURLS_VERSION=1.10.2
# Tue, 19 Aug 2025 10:14:17 GMT
ENV YOURLS_SHA256=c1a5c35d4f47c322d29adffb1a89642544e609808561cf340dc046af58a900e8
# Tue, 19 Aug 2025 10:14:17 GMT
# ARGS: YOURLS_VERSION=1.10.2 YOURLS_SHA256=c1a5c35d4f47c322d29adffb1a89642544e609808561cf340dc046af58a900e8
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
COPY files/vhost.conf /etc/apache2/sites-available/000-default.conf # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
COPY files/vhost-https.conf /etc/apache2/sites-available/default-ssl.conf # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
COPY files/ports.conf /etc/apache2/ports.conf # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 19 Aug 2025 10:14:17 GMT
EXPOSE map[8443/tcp:{}]
# Tue, 19 Aug 2025 10:14:17 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Tue, 19 Aug 2025 10:14:17 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:52a4daa8724e9e1632306e15fe478aa26ff0ebcb7ba924cb168e9b6738c239d5`  
		Last Modified: Wed, 13 Aug 2025 01:42:36 GMT  
		Size: 33.6 MB (33594213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebe95aaa1875d4c50c764ba29c6f95cc470f62d9ac88ad9109e0cd4505d319b5`  
		Last Modified: Wed, 13 Aug 2025 05:31:58 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e0ffef807c2273a22858b85bf52a5cbb82101766a6dfce24ba2f8e3ca25f228`  
		Last Modified: Wed, 13 Aug 2025 08:03:15 GMT  
		Size: 109.6 MB (109595127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b5e8a64ac10b73fd871320ade0ad956a6b2aeb6e2c3151d32095cad855bbccb`  
		Last Modified: Wed, 13 Aug 2025 05:32:01 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd42c19a20ac483aec1baacbb7b775bf9031104d0a0f064b9f0867d3ccc76220`  
		Last Modified: Wed, 13 Aug 2025 05:31:06 GMT  
		Size: 4.9 MB (4875422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cfcf6e5878ff7716cc38c54c9c5482a97442ddcdd8c0aabd868a7d11ed49b7e`  
		Last Modified: Wed, 13 Aug 2025 05:31:07 GMT  
		Size: 439.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:983399591a61da466bb4e672cad02d507232883ed14732dd13f80ac851284879`  
		Last Modified: Wed, 13 Aug 2025 05:31:02 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd811f69e256cec99901017a757476b26842c217d4d7fda51a62333dbcb02863`  
		Last Modified: Thu, 28 Aug 2025 19:22:07 GMT  
		Size: 13.8 MB (13814767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a4c3907298777422962099425e4022edbd688e4f5446d715060cafd67b6d2fc`  
		Last Modified: Thu, 28 Aug 2025 19:15:48 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:820b64fb70e9659ce604d010aedece0c94492b0015943a94940a6e0419fd1734`  
		Last Modified: Thu, 28 Aug 2025 19:22:09 GMT  
		Size: 14.6 MB (14615019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a4db9a86f5fc06d6303e00e75375cc8c98b430fec78d90b050e7c400eb825c`  
		Last Modified: Thu, 28 Aug 2025 19:15:47 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a134ec3245fe7772dccccd70eb6d471ba4305b57ac04079226f5a0e50f32229e`  
		Last Modified: Thu, 28 Aug 2025 19:15:47 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:363753331dcde726b0f412d6913299943e9af62133fc9ca668d89d3f065f2aaa`  
		Last Modified: Thu, 28 Aug 2025 19:15:46 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a3f6da3e8c7a55c40f2e543e70e2fc04a561de92d9c6b2cd4aef1d64c26f4e0`  
		Last Modified: Thu, 28 Aug 2025 19:15:46 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47dd37112d5df98a9211ca1a556d858879910008eb104b1492ee4897c3e5f840`  
		Last Modified: Thu, 28 Aug 2025 21:16:47 GMT  
		Size: 209.3 KB (209315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba3f99ab43bb9c20d5380d01007619aa8fa682530b260f44f279bea73134cc13`  
		Last Modified: Thu, 28 Aug 2025 21:16:50 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:771079d26c676a27ccce6c015aa0b16b6b862e6506459c34e955729b02506c13`  
		Last Modified: Thu, 28 Aug 2025 21:16:54 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b86eeb51d0376283e4583201aeaba1ac98c6bb60196bdf0183003aa20f914a5`  
		Last Modified: Thu, 28 Aug 2025 22:43:25 GMT  
		Size: 6.1 MB (6073643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b80131efb216cbd81582b5cc6e9693bc9387b5eb3d655a254482499101c179a9`  
		Last Modified: Thu, 28 Aug 2025 21:16:57 GMT  
		Size: 2.1 KB (2099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79a8bffa539c24cc43f5a928a484b5735f23ae2e35df58f1a7f851e955225097`  
		Last Modified: Thu, 28 Aug 2025 21:17:00 GMT  
		Size: 1.7 KB (1693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:903293d8397f26502510e33227901f78ca37a0b41904b850b81a3d0e21bd624a`  
		Last Modified: Thu, 28 Aug 2025 21:17:03 GMT  
		Size: 502.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87214d3cf70e9e0a6c8617ec6d28d778a2992ab157ca0fa9b0d48f0a84f29223`  
		Last Modified: Thu, 28 Aug 2025 21:17:06 GMT  
		Size: 548.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34d37c6d3600200bba5823b271a52f78683a6dd179f2b8f635d79415dea650ed`  
		Last Modified: Thu, 28 Aug 2025 21:17:10 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:1-apache` - unknown; unknown

```console
$ docker pull yourls@sha256:409fe600f887711f6b52a5c02384c50885504b017424ffe3f511585e3de22bff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 KB (49132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:704b18033b99324fa8e2efe39b37db6f032ef97e39144d2073917bdc4e76dec9`

```dockerfile
```

-	Layers:
	-	`sha256:81aa30f5e743d3f77ca523125ed1970ca77677b741043d9bb2644669ceb5db4d`  
		Last Modified: Thu, 28 Aug 2025 22:42:58 GMT  
		Size: 49.1 KB (49132 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:1-apache` - linux; riscv64

```console
$ docker pull yourls@sha256:051b58d6ace21bc9b6ea541410e11c83bb8da7a8386e3b8b6136dccac46fc759
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.6 MB (212601113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a69022d6df4c355fb65e57bdd5b84a06e897af44788ccf7b77c9fef31a6ec241`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 08 Aug 2025 00:02:22 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1754870400'
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 08 Aug 2025 00:02:22 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 08 Aug 2025 00:02:22 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_VERSION=8.4.11
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.11.tar.xz.asc
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_SHA256=04cd331380a8683a5c2503938eb51764d48d507c53ad4208d2c82e0eed779a00
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 Aug 2025 00:02:22 GMT
STOPSIGNAL SIGWINCH
# Fri, 08 Aug 2025 00:02:22 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
WORKDIR /var/www/html
# Fri, 08 Aug 2025 00:02:22 GMT
EXPOSE map[80/tcp:{}]
# Fri, 08 Aug 2025 00:02:22 GMT
CMD ["apache2-foreground"]
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
RUN a2enmod rewrite expires # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
ARG YOURLS_VERSION=1.10.2
# Tue, 19 Aug 2025 10:14:17 GMT
ARG YOURLS_SHA256=c1a5c35d4f47c322d29adffb1a89642544e609808561cf340dc046af58a900e8
# Tue, 19 Aug 2025 10:14:17 GMT
ENV YOURLS_VERSION=1.10.2
# Tue, 19 Aug 2025 10:14:17 GMT
ENV YOURLS_SHA256=c1a5c35d4f47c322d29adffb1a89642544e609808561cf340dc046af58a900e8
# Tue, 19 Aug 2025 10:14:17 GMT
# ARGS: YOURLS_VERSION=1.10.2 YOURLS_SHA256=c1a5c35d4f47c322d29adffb1a89642544e609808561cf340dc046af58a900e8
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
COPY files/vhost.conf /etc/apache2/sites-available/000-default.conf # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
COPY files/vhost-https.conf /etc/apache2/sites-available/default-ssl.conf # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
COPY files/ports.conf /etc/apache2/ports.conf # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 19 Aug 2025 10:14:17 GMT
EXPOSE map[8443/tcp:{}]
# Tue, 19 Aug 2025 10:14:17 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Tue, 19 Aug 2025 10:14:17 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:a37386b9234ad75f65b5aa72f3d919ff0eb3bb18978566fa959d6e357480594c`  
		Last Modified: Wed, 13 Aug 2025 04:01:43 GMT  
		Size: 28.3 MB (28271623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40e74ecc2368ed7bf14f15784d294255a507b61c121584b8889b54497f586460`  
		Last Modified: Wed, 13 Aug 2025 11:14:45 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44ba9332bf4f75d23eae5411f58fe1a55971f98de6873eba08746a8a1042d175`  
		Last Modified: Wed, 13 Aug 2025 11:43:11 GMT  
		Size: 146.6 MB (146577824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05acfa088a6e9eb3845fc5011b31ba6a62983f44944e2347f32361bf21d8f85`  
		Last Modified: Wed, 13 Aug 2025 11:14:48 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:437ee082f6fa69e7faad8700545098a6fe52d7039873614c52058e758703420b`  
		Last Modified: Wed, 13 Aug 2025 11:57:42 GMT  
		Size: 4.0 MB (4025653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5398f81f2b0b9d166065f2794959e13fe5cef571690a888e526a297344cb648`  
		Last Modified: Wed, 13 Aug 2025 11:57:42 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7320c702209633ef3bb6abda50aa7d4faab29f17f69247e387513e5af1004ed`  
		Last Modified: Wed, 13 Aug 2025 11:57:42 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42cddc700ba0cb108198a5a00e1def0c2af7bdbe4fe485ab8d91c640a321a73d`  
		Last Modified: Wed, 13 Aug 2025 17:05:11 GMT  
		Size: 13.8 MB (13810719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7ec14e885eeb0d5b2317ab7a2c3d4e12796be0833b0f9585a694ab2ec3d706a`  
		Last Modified: Wed, 13 Aug 2025 16:16:13 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fe0e86774f6c6ec93e9bc7d2328a65a1a82bbe8267508a443c6e56d36776512`  
		Last Modified: Wed, 13 Aug 2025 17:05:17 GMT  
		Size: 13.6 MB (13644924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:680b340ffb03bdc0b96c9aa4f464a5a3041272e42eeec4ae1b226daf8b3e1279`  
		Last Modified: Wed, 13 Aug 2025 16:16:16 GMT  
		Size: 2.5 KB (2464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1560aeec2511b0a1fb912a9f9c4a378248f0b2d368d04192e3215e60f002eb8`  
		Last Modified: Wed, 13 Aug 2025 16:16:19 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d5f7b555c1e6beea9777086dd273c6d2bec21d788655edcd044cc34d74c0e80`  
		Last Modified: Wed, 13 Aug 2025 16:16:23 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf9ae7b15094360374526a467b26cd186b321b527583245240db442766926703`  
		Last Modified: Wed, 13 Aug 2025 16:16:27 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5bef51621d6f0c215020c8dba42933c8bef1d00891165b16153217a862f4bd1`  
		Last Modified: Fri, 22 Aug 2025 02:38:13 GMT  
		Size: 185.1 KB (185104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336ca30cb1ef897c4f3cbca2b1f8ccfd51b620a3749b316f0860a7caec1755d6`  
		Last Modified: Fri, 22 Aug 2025 02:38:13 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81aee594ae2ac5f4e2a3c23cf6b0a82c3ef71bae75bd0611472558616c19af56`  
		Last Modified: Fri, 22 Aug 2025 02:38:13 GMT  
		Size: 352.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14965634a2eef2aa99ca2d9504257a6067eda1014ad1e4d765a097677a1f135b`  
		Last Modified: Fri, 22 Aug 2025 02:38:14 GMT  
		Size: 6.1 MB (6073643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e954b25f2d565de3b39c42486fef7a4cdf694559541e70f226524737bc5ade2`  
		Last Modified: Fri, 22 Aug 2025 02:38:14 GMT  
		Size: 2.1 KB (2097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e95d94d15cf2c9b5783ee6b895829de34354c8b67affaaa29fea6c444c37e58`  
		Last Modified: Fri, 22 Aug 2025 02:38:14 GMT  
		Size: 1.7 KB (1697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f687f2ac289f7bf7d7018abeab7034d0674dd3df979951448945502379c5939`  
		Last Modified: Fri, 22 Aug 2025 02:38:14 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21fed73811d03faad702e9e6db8c5e2b8ff72e4d843a7c69e95facaa68dee768`  
		Last Modified: Fri, 22 Aug 2025 02:38:14 GMT  
		Size: 548.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dbb70dc7b25feda9c0adc9890afe1f613871d51ea051934fc0973de3d8ea44a`  
		Last Modified: Fri, 22 Aug 2025 02:38:15 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:1-apache` - unknown; unknown

```console
$ docker pull yourls@sha256:9a16ed47dbfc40e5c2b8c6b936abca27c23011621bbed45d4966ad6f9a0f2a9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 KB (49132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c49bfdc2386c54bf69507c73509175b4cd83f6279c0fa76fe297924ca9e5b1da`

```dockerfile
```

-	Layers:
	-	`sha256:e4e9cf32bfc408cd124f61f3c5967a51594c05fc184f766cfca23ca51143154b`  
		Last Modified: Fri, 22 Aug 2025 04:42:34 GMT  
		Size: 49.1 KB (49132 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:1-apache` - linux; s390x

```console
$ docker pull yourls@sha256:605a09b973745e68ece204d559fb8285fedf381a87196aef0fef4c666e28076a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.1 MB (161102090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c091bcfd36ae687cf4f6bb5092dbe13d6c47adc3e8ee203b871ebf62b0d9df35`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1754870400'
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 19 Aug 2025 10:14:17 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 19 Aug 2025 10:14:17 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_VERSION=8.4.12
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.12.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.12.tar.xz.asc
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_SHA256=c1b7978cbb5054eed6c749bde4444afc16a3f2268101fb70a7d5d9b1083b12ad
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 19 Aug 2025 10:14:17 GMT
STOPSIGNAL SIGWINCH
# Tue, 19 Aug 2025 10:14:17 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
WORKDIR /var/www/html
# Tue, 19 Aug 2025 10:14:17 GMT
EXPOSE map[80/tcp:{}]
# Tue, 19 Aug 2025 10:14:17 GMT
CMD ["apache2-foreground"]
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
RUN a2enmod rewrite expires # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
ARG YOURLS_VERSION=1.10.2
# Tue, 19 Aug 2025 10:14:17 GMT
ARG YOURLS_SHA256=c1a5c35d4f47c322d29adffb1a89642544e609808561cf340dc046af58a900e8
# Tue, 19 Aug 2025 10:14:17 GMT
ENV YOURLS_VERSION=1.10.2
# Tue, 19 Aug 2025 10:14:17 GMT
ENV YOURLS_SHA256=c1a5c35d4f47c322d29adffb1a89642544e609808561cf340dc046af58a900e8
# Tue, 19 Aug 2025 10:14:17 GMT
# ARGS: YOURLS_VERSION=1.10.2 YOURLS_SHA256=c1a5c35d4f47c322d29adffb1a89642544e609808561cf340dc046af58a900e8
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
COPY files/vhost.conf /etc/apache2/sites-available/000-default.conf # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
COPY files/vhost-https.conf /etc/apache2/sites-available/default-ssl.conf # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
COPY files/ports.conf /etc/apache2/ports.conf # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 19 Aug 2025 10:14:17 GMT
EXPOSE map[8443/tcp:{}]
# Tue, 19 Aug 2025 10:14:17 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Tue, 19 Aug 2025 10:14:17 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:bfe4d60a27c9392ab729f16b50a763cda36622d744066c3cf029a072133f2907`  
		Last Modified: Tue, 12 Aug 2025 20:59:52 GMT  
		Size: 29.8 MB (29833057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2d672c8320b5c626e155e165336b2569c5c22cfbda44788e2e9dd0b175c8a1e`  
		Last Modified: Tue, 12 Aug 2025 23:44:44 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b06790e9e58c7a87421168e1b912411e592f3adbcdce2412a5541e72fa8de3f1`  
		Last Modified: Tue, 12 Aug 2025 23:44:49 GMT  
		Size: 92.6 MB (92562072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:019838dc72213baa0c7fefd5773b69a921a755553c45ef473aea40f478c95cb3`  
		Last Modified: Tue, 12 Aug 2025 23:44:45 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7420b950475ba12842aacb09ab6fc12c17aed6a94e8f7425f2d9023a527d61d9`  
		Last Modified: Tue, 12 Aug 2025 23:51:06 GMT  
		Size: 4.3 MB (4320335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2286236b154642f4dfec098836badaf56b6f5891dfe3de1dd729e687339006a8`  
		Last Modified: Tue, 12 Aug 2025 23:51:05 GMT  
		Size: 435.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93d32f90a36507f204f3058a0f5e737aa20705dbfb0fceb4bbcaba30b59ab9c8`  
		Last Modified: Tue, 12 Aug 2025 23:51:05 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f3ec08fb00212070b8b2cd4643636f1b5d20a822f7b322448a32fff14898c80`  
		Last Modified: Thu, 28 Aug 2025 18:44:06 GMT  
		Size: 13.8 MB (13814231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08425b481f78bfab49b7cdb450300a773b28d96a658c58b674def6d4bff9693b`  
		Last Modified: Thu, 28 Aug 2025 18:44:05 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15b7e2fb32797d4f3337214f556d943df6ab26907ead23c353f8f9cd2263834b`  
		Last Modified: Thu, 28 Aug 2025 18:44:07 GMT  
		Size: 14.3 MB (14286758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78bb368214f21bc80efbac7d78f1046aacefa31571fc09c51184d4cd7e41e89d`  
		Last Modified: Thu, 28 Aug 2025 18:44:05 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cc23a71ab3b32855f94af7a480089d055f2da5b9fd84cc931dde0d2fbe9d123`  
		Last Modified: Thu, 28 Aug 2025 18:44:05 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccf2a2bc50eb8166d36b59a8253260bcaa6fe5978109d59c9abd54cdac07b02d`  
		Last Modified: Thu, 28 Aug 2025 18:44:05 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe6b5e0d68d1f0a8f9680c8beb33ae44cf08aba79000f248e3200e96b4d9a946`  
		Last Modified: Thu, 28 Aug 2025 18:44:05 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b8c156e2f38445c117f842ab525a0e4e0854c3d3030eb16b1a6f73271d7e4fa`  
		Last Modified: Thu, 28 Aug 2025 21:01:40 GMT  
		Size: 200.4 KB (200400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:115255a2d271925ecc92fdb9b0135105c9049d57d96c48b0179c897eeb564a80`  
		Last Modified: Thu, 28 Aug 2025 21:01:40 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e7b79d232bc63f6acc4a373e8625f314824b8ce1ef85697002df06009de9eb7`  
		Last Modified: Thu, 28 Aug 2025 21:01:40 GMT  
		Size: 353.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d58c61301e3e1f0aab89200642be4278d23e7944ceef25a03fc0b5ee73e6ed75`  
		Last Modified: Thu, 28 Aug 2025 21:01:41 GMT  
		Size: 6.1 MB (6073643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f03590ae62f0a3e95a7557ac9098eeb6660732aed7a3fdb256c1ca5bd99ac34a`  
		Last Modified: Thu, 28 Aug 2025 21:01:40 GMT  
		Size: 2.1 KB (2099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e187bde5b0a3dffc305015036db5b423109a5aebf679d8f96b49e3f994f57026`  
		Last Modified: Thu, 28 Aug 2025 21:01:40 GMT  
		Size: 1.7 KB (1695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8539546868b654a9137eec572683f0614a4fb6599941571c689585d91ca2fbd`  
		Last Modified: Thu, 28 Aug 2025 21:01:40 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9257d76bc4df702074acc82556a8b6310c1a0a15f89f0b4e31057cc85c7ab798`  
		Last Modified: Thu, 28 Aug 2025 21:01:40 GMT  
		Size: 548.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae1805193a43702d3be7c177e2cb1ad4d1d2e1fe666af25cfa05beef50ac88ae`  
		Last Modified: Thu, 28 Aug 2025 21:01:40 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:1-apache` - unknown; unknown

```console
$ docker pull yourls@sha256:56dc450e58c157316fee30bd9faee48becaa650d5a31aaddf56156117c529983
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 KB (49047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75cd64355945b25081c1060a25ab9c2c5238cedb11bebfb3cfb1fe97edc97db8`

```dockerfile
```

-	Layers:
	-	`sha256:9a873cba19821df758e0443283841d5d8fa6b4cf14be2eaefa268c4a67ba63ef`  
		Last Modified: Thu, 28 Aug 2025 22:43:03 GMT  
		Size: 49.0 KB (49047 bytes)  
		MIME: application/vnd.in-toto+json
