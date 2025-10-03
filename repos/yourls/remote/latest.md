## `yourls:latest`

```console
$ docker pull yourls@sha256:4d352d48719d66fd799f557fc0ad36f780304f9aae6ac397b9d6ee98fcef23d9
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

### `yourls:latest` - linux; amd64

```console
$ docker pull yourls@sha256:835005a3fc243b47ef209f42c0963d653f35b59ff0b285e4c639063833bf16d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.9 MB (185934267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d17604003608d88c4153981f459ea10e52c2b2a16fbc8d423cdb2d88f7df148f`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 19 Aug 2025 10:14:17 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
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
ENV PHP_VERSION=8.4.13
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
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
	-	`sha256:8c7716127147648c1751940b9709b6325f2256290d3201662eca2701cadb2cdf`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 29.8 MB (29777766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65b4ef33f7b1ac07d3a9ba8baa88b77a9c50656f6502978e260811dbad851f37`  
		Last Modified: Mon, 29 Sep 2025 23:53:12 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6df07a1dd591279bca87fd190218995c93972a53dea28672db2cbd1831d4161`  
		Last Modified: Mon, 29 Sep 2025 23:54:21 GMT  
		Size: 117.8 MB (117836887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad0470c7237e5c936856acbbfe015e0d2066dc239362fdde911e131561a159ea`  
		Last Modified: Mon, 29 Sep 2025 23:54:08 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd065f60f510c64a620c6eded9f185b798935b07f04b0cf5d4b6cda38cc893a9`  
		Last Modified: Mon, 29 Sep 2025 23:54:02 GMT  
		Size: 4.2 MB (4224103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce9f805bd9f92a556e50e9c4b06b09a46796df3cb1832a41003f1e46c04a2466`  
		Last Modified: Mon, 29 Sep 2025 23:54:02 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e00e68947876ce82ae79175ae069263b355ad814ed2e01e2b984059422a8c2`  
		Last Modified: Mon, 29 Sep 2025 23:54:02 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9e308cc50b693957306e92ca58a13d5e76fa6062ce1183b80a4d58fbf4813cb`  
		Last Modified: Tue, 30 Sep 2025 00:00:06 GMT  
		Size: 13.8 MB (13812111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e087ba3bc8c57515c87d37baddfe40ed81116a0e3cf6a9ee53244cab83fac470`  
		Last Modified: Tue, 30 Sep 2025 00:00:06 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca534350e7ded62a7c4bff4b7dc033f2e48882ae3886211d33c74bec54278c1c`  
		Last Modified: Tue, 30 Sep 2025 00:00:10 GMT  
		Size: 13.5 MB (13528156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f9354b18f41807e1ffba980c274ba75ddaf2e93ace0be1328a1e41b5a9f70b`  
		Last Modified: Tue, 30 Sep 2025 00:00:06 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66e584db80115d9b76e08cbf59644ff6e1c29774803b273e7e9beb5bb813809d`  
		Last Modified: Tue, 30 Sep 2025 00:00:06 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd6af47d3e303e8b18124958d7bd9a82907c91dcc5f2e6b7ae0ea4e5da7b4ddc`  
		Last Modified: Tue, 30 Sep 2025 00:00:06 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e80f3ae94ca7eca6ab2eb920234e99c99fcb2aa5d46cbe933f6c56728a81e97e`  
		Last Modified: Tue, 30 Sep 2025 00:00:07 GMT  
		Size: 888.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cd0bfbbbed44764d87179eb5b04c7eb6e9d40abd230c87d897de9e320825d7a`  
		Last Modified: Tue, 30 Sep 2025 03:16:27 GMT  
		Size: 670.1 KB (670062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42ac13c2298e43e53be0aba1d1b4cc854c4602feeed1f4a2d5b2d592912279d9`  
		Last Modified: Tue, 30 Sep 2025 03:16:27 GMT  
		Size: 323.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d97cda868062e52de7e8e9c6f7bce2f82f63cae90d9eaa5a4a84be9c0a0f98f2`  
		Last Modified: Tue, 30 Sep 2025 03:16:27 GMT  
		Size: 345.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cc88acb7c5e52560a7cadef3865d853c270252ad4abb061717931750072b206`  
		Last Modified: Tue, 30 Sep 2025 03:16:27 GMT  
		Size: 6.1 MB (6073643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:166aec946a98d8a6e930c7d18cfc2ae5b5a7c88044e20f25a27811aa21c92622`  
		Last Modified: Tue, 30 Sep 2025 03:16:27 GMT  
		Size: 2.1 KB (2092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c94d2d4cd58ed4910b155dd29b8418b3f03a21d5daee0726a51a8c3c30e08e73`  
		Last Modified: Tue, 30 Sep 2025 03:16:27 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:897d74b6f216fb24a4234769946f15cb97448583500b564e3616a5e6ab4366db`  
		Last Modified: Tue, 30 Sep 2025 03:16:27 GMT  
		Size: 502.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91ac052f711130ea8d85a2050fc3f01faf5a2d2f40caa52f259d3e728454a1ff`  
		Last Modified: Tue, 30 Sep 2025 03:16:27 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4651372f7689b0236b44f48d223f25a8d5d7a031ed3f74683343d3d070d68d0a`  
		Last Modified: Tue, 30 Sep 2025 03:16:27 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:latest` - unknown; unknown

```console
$ docker pull yourls@sha256:d16f2980767f5be658181970594d43aaba916467617201d9ddddc056ed95d8c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 KB (49058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7018f1b406a7d130d4a6fe2f30d7a95c9c8dc18e8610345d6db409052b8df2c`

```dockerfile
```

-	Layers:
	-	`sha256:ec1ce661346377e0bee237b832273c6928df17a325c325cb0f05e5d52a7b73c3`  
		Last Modified: Wed, 01 Oct 2025 16:42:32 GMT  
		Size: 49.1 KB (49058 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:latest` - linux; arm variant v5

```console
$ docker pull yourls@sha256:fe2cd77a58cca46fb807ddac5234bbfcd26ea2b558675671cc17739eb40186b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.2 MB (159160463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe95e4380eafb197b67f65b032a8077ff12a56c87220c854c7663e173ee7ebd0`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 19 Aug 2025 10:14:17 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1759104000'
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
ENV PHP_VERSION=8.4.13
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
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
	-	`sha256:d2a243ecf382412941b4d6772dba911a8093cf3703c933872fbb7ecc21e27e20`  
		Last Modified: Mon, 29 Sep 2025 23:34:24 GMT  
		Size: 27.9 MB (27946145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4454155cd87487bba9a48307903d757a5d949a81cac4ea7181d21c768154709b`  
		Last Modified: Mon, 29 Sep 2025 23:53:03 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d20120918cfeb5173294cc1c08102ea1383c4e1df5d0e01d5e762648126321`  
		Last Modified: Mon, 29 Sep 2025 23:54:09 GMT  
		Size: 94.9 MB (94874441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02541a4d4fa81df6b424c500c3a4276614553df68e89f9b0165f90e5b56aebb6`  
		Last Modified: Mon, 29 Sep 2025 23:54:03 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a271e5d70023c4287902016e5804e71024f8dba60c93d744aa28db5149f91bb`  
		Last Modified: Tue, 30 Sep 2025 00:10:15 GMT  
		Size: 4.1 MB (4082030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2344cd86f4b68079123149852001ef42deae0ccdeebbd6317a6111a2106d2085`  
		Last Modified: Tue, 30 Sep 2025 00:10:15 GMT  
		Size: 432.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8588ca70d5d36b0643819ee7f13644dfabdb2a58c17f068be8593f4bd22bdb4e`  
		Last Modified: Tue, 30 Sep 2025 00:10:15 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10766c846a7e07f5db51a8f2c2055284c09c57043976684e371fb9c619ee5ad1`  
		Last Modified: Tue, 30 Sep 2025 00:10:17 GMT  
		Size: 13.8 MB (13809487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:475f266509bbd7928589204a5257b7b17ee0ef334ad7f3c86b62575aa3001cab`  
		Last Modified: Tue, 30 Sep 2025 00:10:16 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:516f5c6ea7b78380b0d11ec9a9fe08d89bbe1e079a108ee3af74c16e1c017f0b`  
		Last Modified: Tue, 30 Sep 2025 00:10:17 GMT  
		Size: 12.2 MB (12188407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6161b1b27fa761a54dc440483694913cc9acace7d0db28eb54f7b9aad971cd5`  
		Last Modified: Tue, 30 Sep 2025 00:10:16 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4170549d36c423513600e0da543b4115c1e39dfe21ee022e28497df79313a06d`  
		Last Modified: Tue, 30 Sep 2025 00:10:17 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28c4948c00b8f70d450f273b3f3d120a08b722c37e9998328d192b855f04e3f1`  
		Last Modified: Tue, 30 Sep 2025 00:10:16 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d5966883bce9f5e1d79b7582657029bc265ee1c0c172b66359cf36c09496d4`  
		Last Modified: Tue, 30 Sep 2025 00:10:16 GMT  
		Size: 887.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e3f6e5e00a2a6b4093339ab2c4e928842368b2e18658cc703fce43799fa75d9`  
		Last Modified: Tue, 30 Sep 2025 02:17:26 GMT  
		Size: 174.8 KB (174770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3d030d9723417d597723ec8e33622eda75824b362e12ceacf9e8f92111a6751`  
		Last Modified: Tue, 30 Sep 2025 02:17:26 GMT  
		Size: 323.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:190ca3ffffe693c5ae47ae4240ca67d2227fb012600824bd064f9ef10eefce67`  
		Last Modified: Tue, 30 Sep 2025 02:17:26 GMT  
		Size: 345.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9878cf727b7464d14232c9a8c44f5b38c872976b52796f94d527994740e47664`  
		Last Modified: Tue, 30 Sep 2025 02:17:27 GMT  
		Size: 6.1 MB (6073644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6723d962f4f439d56715d7bef581b4bd104bdba70dd6da52dae5d9c21397d831`  
		Last Modified: Tue, 30 Sep 2025 02:17:27 GMT  
		Size: 2.1 KB (2091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93f5c230da9908c47ea404e970315e477b875583d462aca016d4d573492595ec`  
		Last Modified: Tue, 30 Sep 2025 02:17:27 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c93b36dcea9f82b6e04d6b5a97361fda9a966cd3c5b1078b95ee24173b3734e3`  
		Last Modified: Tue, 30 Sep 2025 02:17:28 GMT  
		Size: 502.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:807be4692eb6e10fd517071a905d2d707ea572c0b93bc2369faac07b914b1ff2`  
		Last Modified: Tue, 30 Sep 2025 02:17:29 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8334ef64fb7e058751e7af8dcdde071fc851ba3cf6f859800e47c3b1d623fc38`  
		Last Modified: Tue, 30 Sep 2025 02:17:29 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:latest` - unknown; unknown

```console
$ docker pull yourls@sha256:6cb652e3a9fdff75f1595db6feba6025773ae2201720155b83cbaa6bb8ca01e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 KB (49199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ea0b7e3ca9a2dcaf8f21ffdbf0dd5e524b7851a841a9bbbbb31cbc59078b953`

```dockerfile
```

-	Layers:
	-	`sha256:7e20a41e916d9053c8ebc31154ac5b0b050b1fa0e044f1256525616bcd5c8b55`  
		Last Modified: Tue, 30 Sep 2025 07:42:26 GMT  
		Size: 49.2 KB (49199 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:latest` - linux; arm variant v7

```console
$ docker pull yourls@sha256:d5f48313a143b91f78f57fcf94692a4e3f79d85e0bfc02e1b1f1c7bf1cda754b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.9 MB (147874302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69861e34d63579918ddad55e2e1825b5a2dbd917f7c0ef7496ac208c0d7b9042`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 19 Aug 2025 10:14:17 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1759104000'
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
ENV PHP_VERSION=8.4.13
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
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
	-	`sha256:0289e98159900b326d4cedde367bf225e25835a3ad879647f17f922e43cfa884`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 26.2 MB (26212758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2124035b6df0178965919a1689b6d95bc60dad98b242a4f3d99f310ba260ae50`  
		Last Modified: Tue, 30 Sep 2025 00:12:14 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:554f6fed754e85d4fe404bdb7da53a97c211fe10064fbff863dde76db978d257`  
		Last Modified: Tue, 30 Sep 2025 00:12:20 GMT  
		Size: 86.2 MB (86245515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b95ba12bcb10e5e7a752090f559e99e8a257b19757a067f5c0d5dd98124a34bd`  
		Last Modified: Tue, 30 Sep 2025 00:12:10 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22e1eb50835480315e5804ed6760b6bcab513dfb44436d9b4b5c5e1a928babf5`  
		Last Modified: Tue, 30 Sep 2025 00:12:11 GMT  
		Size: 3.8 MB (3751924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c4ee34a6b1f51a913e8a1699b8ec4ae2c3d6fc376188fc887c9854139f72cb3`  
		Last Modified: Tue, 30 Sep 2025 00:12:10 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27abebc81e8353ec37041942291fa03bdfc6e9d44c5132cef69a70890589c98b`  
		Last Modified: Tue, 30 Sep 2025 00:12:11 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba2c6d0c63326aa657a5347e88dfd40e34270f3a74cc3955133cb4415b7c2a57`  
		Last Modified: Tue, 30 Sep 2025 00:12:13 GMT  
		Size: 13.8 MB (13809601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dc3a07bbf9dddb7902faf00c6dbdacda1c1011ce1c709370236248185addd7b`  
		Last Modified: Tue, 30 Sep 2025 00:12:11 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b259ca7bdbae055cba7ac6e424e8a05ee51b7758d1f248f9a628cd27c120500b`  
		Last Modified: Tue, 30 Sep 2025 00:12:12 GMT  
		Size: 11.6 MB (11607927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c92d71f8244c6c1d47f883dc61c7cf0bc2ac986599373a32c17c83865e11181a`  
		Last Modified: Tue, 30 Sep 2025 00:12:12 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc65729ddc6bc8e4833eadb695afff44779794f10b85d396601de0a439191360`  
		Last Modified: Tue, 30 Sep 2025 00:12:13 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e070b487f8fba9b27e4c93594175992ae61c03b2fb24ee4a8bc826450cd4fcb8`  
		Last Modified: Tue, 30 Sep 2025 00:12:13 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a01ea1bfe2315a7e44a7fe8caa79846318266a83ca26a50b9bba855610f3efea`  
		Last Modified: Tue, 30 Sep 2025 00:12:13 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b4694f86fd3c5ae5c79f91296e2bf405d45cbf18637caa3f0bd7f1ea05ed737`  
		Last Modified: Tue, 30 Sep 2025 02:39:05 GMT  
		Size: 161.4 KB (161393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01a666d73dc41f7ef59fa4b6cedb5d05076cc9299bf7a693d24ff4a26aa2dd1a`  
		Last Modified: Tue, 30 Sep 2025 02:39:04 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bd4cbe1d3f4983d29194dc824abf426c9b28ee2e94a85d5a21fd91602796dc6`  
		Last Modified: Tue, 30 Sep 2025 02:39:05 GMT  
		Size: 343.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbecd3acfdf51a50b05ccb81a5670a28808a998b8b6f7f92c905bf2c0eb192ee`  
		Last Modified: Tue, 30 Sep 2025 02:39:05 GMT  
		Size: 6.1 MB (6073643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:962c63f32d5b0c31a2d6c52115d24e788611005d5bc6677f11f80166609268b9`  
		Last Modified: Tue, 30 Sep 2025 02:39:05 GMT  
		Size: 2.1 KB (2089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ec85e264b31f8b735604b8716677d5ae3dd1a2d7280f80123f827f3127d8fde`  
		Last Modified: Tue, 30 Sep 2025 02:39:05 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c419be406f8586bd9dc87e481982a5ac729f9aac30789c342bfb2ce3cc19972`  
		Last Modified: Tue, 30 Sep 2025 02:39:05 GMT  
		Size: 501.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8942c9e69b09cf4b4430a9c74ffb55b6ca4c809368f4d4d7b2e486249cb8da77`  
		Last Modified: Tue, 30 Sep 2025 02:39:05 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1e0d8f62505d7ad5b595cf61a1ec7ddb4ab2fb02e011703785813ed1ae83fec`  
		Last Modified: Tue, 30 Sep 2025 02:39:05 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:latest` - unknown; unknown

```console
$ docker pull yourls@sha256:dedd9f9d4013377d51c9185ba560e004b0b6bff68086b0c1825ce62380d609e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 KB (49199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ba8d80cb595fa3e32c2ebda9ec56cfdbc11d235270cfd263f9c7e4a20545e96`

```dockerfile
```

-	Layers:
	-	`sha256:afdf39c273bc19bd281fb81127f62f896b0033e5102edac95bb838086f820548`  
		Last Modified: Wed, 01 Oct 2025 22:42:56 GMT  
		Size: 49.2 KB (49199 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:latest` - linux; arm64 variant v8

```console
$ docker pull yourls@sha256:90d02e4089660ef4cbfb3b65d656caaf92c1ecfe4694e04e315463a597634e29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.3 MB (178272288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abaac397d6dee44e5b036429f046cad29555c1d0f2af145bca46aab7945ac879`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 19 Aug 2025 10:14:17 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
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
ENV PHP_VERSION=8.4.13
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
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
	-	`sha256:e363695fcb930d5f18449254c0052117582c3de4263c91575b0a9040c986e412`  
		Last Modified: Mon, 29 Sep 2025 23:35:13 GMT  
		Size: 30.1 MB (30140842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c5501e469a82a20a58ec0fc8bcfad40177a1ab89429f441fb01016bf0795776`  
		Last Modified: Tue, 30 Sep 2025 00:01:12 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faa2771a9f5de236173f5205659980bcee0575d3c649e78ec890ac0f9c0badfe`  
		Last Modified: Tue, 30 Sep 2025 00:01:18 GMT  
		Size: 110.2 MB (110162764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b5bb4b80b4e06abfabeb44725f855f6bb4ad67606805f34d58b4b061b030f72`  
		Last Modified: Tue, 30 Sep 2025 00:01:13 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa82eedd9d9cd7396648838e2e4b2aee8d6e3fbb26188261712b8688ee1280c`  
		Last Modified: Tue, 30 Sep 2025 00:01:15 GMT  
		Size: 4.3 MB (4302071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7e2eb9f219546656a3dfd03216dee1c1f5dd0e385b03c6936d9e60189269f35`  
		Last Modified: Tue, 30 Sep 2025 00:01:13 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8596e9072025f4c902883e25562a3166670c91a0420c4b9d6aa80cd48f1e3267`  
		Last Modified: Tue, 30 Sep 2025 00:01:13 GMT  
		Size: 481.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdfcffdc1c1a0ddada9c800192cfc284ca6b2a45fae899fb7a3cb2bced32b54a`  
		Last Modified: Tue, 30 Sep 2025 00:01:17 GMT  
		Size: 13.8 MB (13811662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8052982e7d9a19fb3ffaa91afb21595c4614e7aea1a22a7d60d1e8a60bd12646`  
		Last Modified: Tue, 30 Sep 2025 00:01:13 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0b6a4d0cdfc71bcc753ef38662a63793047159fb717e9a6c6ca5ea629b767fe`  
		Last Modified: Tue, 30 Sep 2025 00:01:14 GMT  
		Size: 13.2 MB (13179369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c42945a27eef5064dcc44b6a22c716c4bc80b6bf87fa50ff68b0fabfe558f827`  
		Last Modified: Tue, 30 Sep 2025 00:01:13 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66400f9ae4fe0eb0fa7e66d045b1829100c43d66aa0f2afea39c5079634f3a42`  
		Last Modified: Tue, 30 Sep 2025 00:01:14 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0812ce9911dbc91f5e0bb89dc3f01d9d01e28d12f26b04d5758efd4ab35250b9`  
		Last Modified: Tue, 30 Sep 2025 00:01:15 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18fa9de00a95c368ae81c6113dc0ebf7f796f62ab2839617cba160bda00a1b28`  
		Last Modified: Tue, 30 Sep 2025 00:01:16 GMT  
		Size: 888.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c423c1a8387bf45b2318fddd99cd5c90f83dac1f2f751d1b6c475c7b3c3d42b0`  
		Last Modified: Tue, 30 Sep 2025 00:59:36 GMT  
		Size: 590.4 KB (590409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef5d3aa5531288f4c1aa63feb5797773ab5005c547f54a34256a7ef56d6bd70c`  
		Last Modified: Tue, 30 Sep 2025 00:59:35 GMT  
		Size: 323.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:456931fc15ab495e4aa40ec6827d67cc97fbf1fc9c16b92e14160408b07d8bd6`  
		Last Modified: Tue, 30 Sep 2025 00:59:36 GMT  
		Size: 342.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64ef138285f460dacd204c5672b33355f1aa2fc07ac75de559a72af60eabd88a`  
		Last Modified: Tue, 30 Sep 2025 00:59:36 GMT  
		Size: 6.1 MB (6073642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc33a8321db29cff3ae2a4cf62f66e4564d08f3067283121990331443c7e36a4`  
		Last Modified: Tue, 30 Sep 2025 00:59:36 GMT  
		Size: 2.1 KB (2092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8665f4799ea515fcbd5f9496864dd6846323a0c2b916f46405ebd6adb0f1ffe3`  
		Last Modified: Tue, 30 Sep 2025 00:59:36 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a04f616a5a22a4c2759d03b84bcdc034e0d1da641028d1fefb39e8d82670202b`  
		Last Modified: Tue, 30 Sep 2025 00:59:36 GMT  
		Size: 499.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9592aa727a181f60a118f78107c5dcc5ae272f7ae082ecba22dcb637b150185`  
		Last Modified: Tue, 30 Sep 2025 00:59:36 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98a851fac7961a585598e97ff20ba70a9ee68528abac7c3de8d8b4c86b5629b2`  
		Last Modified: Tue, 30 Sep 2025 00:59:36 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:latest` - unknown; unknown

```console
$ docker pull yourls@sha256:eec8f3eb533267af3ead766fdcdfaaaef7f36cdbcc4b2ebb2cf3eb1796e157c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 KB (49254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eea5354b056d376f7d75ec9e08d2240613b040ff565bf0a6418f9d8de4a0537b`

```dockerfile
```

-	Layers:
	-	`sha256:c4f4455850c3b4261120cddc7fccc60bab3a265d84e8c761ca07ae2c5e1b2275`  
		Last Modified: Wed, 01 Oct 2025 22:42:59 GMT  
		Size: 49.3 KB (49254 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:latest` - linux; 386

```console
$ docker pull yourls@sha256:02605942ce4f4b56c6c1bd7721b4de13b7c5c3165dbd484edefdfd6d4e6c0d04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.3 MB (186301778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50cb8c00a7469260f953d5131594123282573965fdba5a9d6f2fe366391959ee`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 19 Aug 2025 10:14:17 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1759104000'
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
ENV PHP_VERSION=8.4.13
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
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
	-	`sha256:ab4c7760f4a4bda4b0797f3f0b56bd90b9778b76fc8351f2e1bd7c332b9dcc92`  
		Last Modified: Mon, 29 Sep 2025 23:35:33 GMT  
		Size: 31.3 MB (31294536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49a4c35d0bfddec4447bf585ec1db319e667c821daf94d1eee8304481c5603a9`  
		Last Modified: Mon, 29 Sep 2025 23:55:01 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aebfc8668e9fef3e160082dadaa5cb789fbdb59022bd13284d80c574e51ac12c`  
		Last Modified: Mon, 29 Sep 2025 23:55:07 GMT  
		Size: 116.1 MB (116138105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b34a4da2b5f392d016cf8da13fd4037c7dc7f1454d1650678755add29cfb899b`  
		Last Modified: Mon, 29 Sep 2025 23:55:01 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fbabc713f4fb1e3f7def6ce3841e88068eb38fd74d0ce0a6c1e3d5a3745280b`  
		Last Modified: Mon, 29 Sep 2025 23:55:01 GMT  
		Size: 4.5 MB (4455491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d56610a2e15cc4264ec5c2f552040625b69c82968545443e0eb8cf38fe43511e`  
		Last Modified: Mon, 29 Sep 2025 23:55:01 GMT  
		Size: 426.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c14081f02b5a9c542bdfdc87b1fd64b9ed854bd7c52c3070686ed5f83c90ed77`  
		Last Modified: Mon, 29 Sep 2025 23:55:01 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:835db8a51816de2819e2c561cf404aea4d3933d7fbd0174d3b75a5c313fe9efa`  
		Last Modified: Mon, 29 Sep 2025 23:55:02 GMT  
		Size: 13.8 MB (13810964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0341d9571a415b8cfed57ba37776e15a3b1d8081918edb80dd5322a90545fb7b`  
		Last Modified: Mon, 29 Sep 2025 23:55:01 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e49b749e66eecde72e451509d94000ef20edf0a62adf9e60528b3e5296ccf087`  
		Last Modified: Mon, 29 Sep 2025 23:55:02 GMT  
		Size: 13.8 MB (13822530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25fce4eb5762ed400d215076ac1d89ee0958c65e07d810d88af3c53968456db1`  
		Last Modified: Mon, 29 Sep 2025 23:55:01 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42c6913541095d22863266d2e281dda3c5436c358a69ea73cffedb9b0f3f7a20`  
		Last Modified: Mon, 29 Sep 2025 23:55:01 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e3a8d7700e2529912c952022091b330321dfb4ad330c5d1d6b5683a77115a63`  
		Last Modified: Mon, 29 Sep 2025 23:55:01 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0683a200f16d6395e2e35780434c9daa0443469fcfd69e7368252930757e35ce`  
		Last Modified: Mon, 29 Sep 2025 23:55:01 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e2e7097536d9f90d7ccb0a8049e77f4b215d97095b54734f5bf1d43f0e05767`  
		Last Modified: Tue, 30 Sep 2025 00:50:31 GMT  
		Size: 695.0 KB (694968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8123125cf01a88a94efdb4ef44e51a57af4db9b1b5f2b6e7ef65b1d76022f6e6`  
		Last Modified: Tue, 30 Sep 2025 00:50:30 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d11345e3bebcd4fa6a1943bfca70cbf6114cb2474cba63e3b22c1500bb5ed1a4`  
		Last Modified: Tue, 30 Sep 2025 00:50:31 GMT  
		Size: 343.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72d416434252bd2a14805d6a55095cefd6a49f9f49d2becaf19d28ec2fc6dc79`  
		Last Modified: Tue, 30 Sep 2025 00:50:32 GMT  
		Size: 6.1 MB (6073642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b50c3bfbdaf7b4bf9eca923bf6d26e9410333813af12661c64992b47fcc26364`  
		Last Modified: Tue, 30 Sep 2025 00:50:31 GMT  
		Size: 2.1 KB (2091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f10a87aee151e7216f7a094b55c8b32c1999236a0351bf5ff926776ff1639084`  
		Last Modified: Tue, 30 Sep 2025 00:50:32 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70beccb691a46b8291f537afdb68c30be71d50086a65c11a761b4a771db25962`  
		Last Modified: Tue, 30 Sep 2025 00:50:32 GMT  
		Size: 500.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a55795e9fb48ecf8273bc47f3feb094e440ce68347e739e62d5f9671624db0b3`  
		Last Modified: Tue, 30 Sep 2025 00:50:32 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f67cb45f092e27d64e21292dfcb18987f3dfee38063c3f5fd2ef9b33cc32295`  
		Last Modified: Tue, 30 Sep 2025 00:50:32 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:latest` - unknown; unknown

```console
$ docker pull yourls@sha256:3680fba93756e1c85988b151f323a1f9ba3497322c86f4763cbb8389f12300b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 KB (49000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b010f3e0f18ba340cdaec119a1089ac67daf242a4db7051036e7e14c998e4343`

```dockerfile
```

-	Layers:
	-	`sha256:66466bf06c6aa64236298f1b5662996226529b67d70f2cb8ac864434dd5075c7`  
		Last Modified: Wed, 01 Oct 2025 22:43:02 GMT  
		Size: 49.0 KB (49000 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:latest` - linux; ppc64le

```console
$ docker pull yourls@sha256:9fa923b7a3f9184da6dfec66891c2350e35b3cc925275973f4c390928b849d75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.1 MB (182109733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80f0e813fe3566b3d9109a5933cf0057607bcff049039b00811e26bd3cb423e9`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 19 Aug 2025 10:14:17 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1759104000'
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
ENV PHP_VERSION=8.4.13
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
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
	-	`sha256:8bcecd3ced4047f6a4d35464fc2ee9b45e7fcc10b49690427794f4421b0552ab`  
		Last Modified: Mon, 29 Sep 2025 23:41:19 GMT  
		Size: 33.6 MB (33598454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d8f05f06dc824d87111df6e83c98b44d4b30120744017674fa115b47c2dbe6`  
		Last Modified: Tue, 30 Sep 2025 07:16:03 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75015a3f4b08f0357c989a4c27950c8a6de956a67874e0df0e8876482f1c6285`  
		Last Modified: Tue, 30 Sep 2025 07:16:10 GMT  
		Size: 109.6 MB (109597733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55bbf93152fe00ebb17d96bb0b9dce5763e9ee0f645695274ef06bcf783421bd`  
		Last Modified: Tue, 30 Sep 2025 07:16:03 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74cdaf3986afeff98ab8e26d5054958a0fddcd91c28e37dfca6c9bd1937c38c1`  
		Last Modified: Tue, 30 Sep 2025 07:21:18 GMT  
		Size: 4.9 MB (4875653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfd3405d5eef9a007a25174bf4a788fce2a6cb8f4d2a07d35b2433b2d1d52fb3`  
		Last Modified: Tue, 30 Sep 2025 07:21:18 GMT  
		Size: 432.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be0d88f08b4ee89f9ccb3d82e7e8a74e3a33d00089433c4500c8c0bf24c522e9`  
		Last Modified: Tue, 30 Sep 2025 07:21:18 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f7cda48bb202aea5bf34aa5dfe1088214699d2601a21865fc6ced18e64b6b6c`  
		Last Modified: Tue, 30 Sep 2025 07:40:27 GMT  
		Size: 13.8 MB (13811174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da6360d6c05e1fdccf553fa40c2342fd8432c753df26c5715160cb2b7558ab3`  
		Last Modified: Tue, 30 Sep 2025 07:40:27 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fa911083c906bb7772a5dc2034d6f2d54ca4679687e0a77715a93bb8900f9ac`  
		Last Modified: Tue, 30 Sep 2025 07:40:28 GMT  
		Size: 13.9 MB (13932181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c535efcd2036f1a21a14cfcec1d9be4f4a9f9867c07b7ecec9883aa23118746`  
		Last Modified: Tue, 30 Sep 2025 07:40:27 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53389cfa983b58a04e5af6191e82dcd866df266adad6963e7f456ba1befcd9f6`  
		Last Modified: Tue, 30 Sep 2025 07:40:27 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a494786173722902e80a4e5eece7870bef861c73143d4c06d7d9d969dad2aa29`  
		Last Modified: Tue, 30 Sep 2025 07:40:27 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9311274af906f42ec44ca3d75b25b3e66c9d14396e4923f01f59dd4e8404cd4`  
		Last Modified: Tue, 30 Sep 2025 07:40:28 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adedb096be10caaf17ae32e1d90669187273d2d50e41ef53ad375fc9442565f5`  
		Last Modified: Tue, 30 Sep 2025 18:58:35 GMT  
		Size: 209.3 KB (209316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc5b99bf663faa38881e84762e8db08c3ad7a0020312681139e0e4169b965d73`  
		Last Modified: Tue, 30 Sep 2025 18:58:35 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b7b05763a5c2b973f80b1ba81d511462e33c50acfd561a86ed874c335bd0e86`  
		Last Modified: Tue, 30 Sep 2025 18:58:35 GMT  
		Size: 347.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bfd775960a3a09d363c0f234c8177ef6cf1fab314b8572bddb9b685f716ae55`  
		Last Modified: Tue, 30 Sep 2025 18:58:36 GMT  
		Size: 6.1 MB (6073646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:010ef3fd4b60511d07b53f101dcfc22d98687ed44f3cf1b445ebb8dd239974ac`  
		Last Modified: Tue, 30 Sep 2025 18:58:35 GMT  
		Size: 2.1 KB (2090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f21b42b6b802481503c2b71697300e687c80926b6deee12297ee4c597e9326`  
		Last Modified: Tue, 30 Sep 2025 18:58:36 GMT  
		Size: 1.7 KB (1693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6a3682ccd3e282c0efaa6c07164f2e9fcc536b23f17bc2804fc22eff7b425d2`  
		Last Modified: Tue, 30 Sep 2025 18:58:33 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcc0661a49ccd80d18026991cb62634d09f411063f84d2d7910fa0b67b4a0de3`  
		Last Modified: Tue, 30 Sep 2025 18:58:33 GMT  
		Size: 549.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:246ecfe7f0e6a89ae431a1449c31b7a87bd7a5450212a1b0cc8ee13ced2a7e22`  
		Last Modified: Tue, 30 Sep 2025 18:58:33 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:latest` - unknown; unknown

```console
$ docker pull yourls@sha256:46023c9c5dc9a435acc1b8107d22f1fd3cdbc9012b9a02e5f3c67470a8bb6582
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 KB (49132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0747b68bfa87ef61ff2f4a7c2c5297e59743ca1a54f99b1a32af38e353799eff`

```dockerfile
```

-	Layers:
	-	`sha256:d7d8e8f69ad8f760895d386c9a719df8f06c010854fd24a51e44d5e288a82b5e`  
		Last Modified: Wed, 01 Oct 2025 22:43:05 GMT  
		Size: 49.1 KB (49132 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:latest` - linux; riscv64

```console
$ docker pull yourls@sha256:bb1ec42fa0aa43ba1d6c50fed242be903cfd5b053e093b71cbfa083d4e18ff3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.9 MB (211935419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0f148e43841c0f80a64c08a7d30af27390151ecd7663e21d460bb0eb651c1d9`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 19 Aug 2025 10:14:17 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1759104000'
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
ENV PHP_VERSION=8.4.13
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
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
	-	`sha256:ecc6f9aec21fb94a493c2875c244e720a2f7c6c034063ce87b2f5b6b46962ec9`  
		Last Modified: Tue, 30 Sep 2025 01:05:14 GMT  
		Size: 28.3 MB (28275502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e10c25f1d43bda19fe1addca79e55bd60680b6683c485853db1be0763dd7e2`  
		Last Modified: Tue, 30 Sep 2025 05:07:03 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03438fb8247e71c15afcd0508b678af32b8a41a4cd64dda788e8224b32557902`  
		Last Modified: Tue, 30 Sep 2025 15:10:17 GMT  
		Size: 146.6 MB (146579364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df117f051d654fe662d0af341155be2d955517920079566410cd20daddb0a237`  
		Last Modified: Tue, 30 Sep 2025 05:07:03 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5820c12643e6a3e49d793483aa7a8f0fc043801a3e3d7085a78a2243ac2efa0b`  
		Last Modified: Tue, 30 Sep 2025 06:10:09 GMT  
		Size: 4.0 MB (4026042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13195b106bcebf839d7af0f2269c2a442a10e9e41e345d562397fa27f3d35f90`  
		Last Modified: Tue, 30 Sep 2025 06:10:08 GMT  
		Size: 452.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:627b6eeabd2d7dec5e31e065537160dea1d3126b8ca00665c8bbb2aaace9b070`  
		Last Modified: Tue, 30 Sep 2025 06:10:08 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd1c0dcc3fb937418b0897cf4dd8a439cab9ab72629ab902f47fe05ca48015c9`  
		Last Modified: Tue, 30 Sep 2025 10:10:28 GMT  
		Size: 13.8 MB (13820288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12db6f9624d4a37a9ab59c03eaab84de59f91918773e77a7bb7adec5c3b085e8`  
		Last Modified: Tue, 30 Sep 2025 10:10:26 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:074154ebf34375a3d3705b2613fb650574f44f7d9e23edc52d00e2e5d04844eb`  
		Last Modified: Tue, 30 Sep 2025 10:10:30 GMT  
		Size: 13.0 MB (12963836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60d616dfe163e70564f2d8e53df1e55bcc8f6cc2b03abbbbdc6b0b1e47b34a93`  
		Last Modified: Tue, 30 Sep 2025 10:10:29 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:470ecd6e34f5d7146c87fb0c5e76690cd4aad09ae8a0c922d59dff5226b95155`  
		Last Modified: Tue, 30 Sep 2025 10:10:28 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be50faa30ec687dd8ec9a43ac6483f376aedbfa6d10296ea5a1ce3f3d7494246`  
		Last Modified: Tue, 30 Sep 2025 10:10:28 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fc662d233dfc6fe2dbb9351a550c2349adf87773451d9aeafe1681537df5909`  
		Last Modified: Tue, 30 Sep 2025 10:10:29 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37d8485bb041d7e910e5223f4662b020f87f7194ec0578d8a88e8436a5b72f76`  
		Last Modified: Fri, 03 Oct 2025 00:55:37 GMT  
		Size: 185.1 KB (185144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1870841512eae40155dd44dc0341d209ac291e06cf8063d6e15b4fe19ca00665`  
		Last Modified: Fri, 03 Oct 2025 00:07:56 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51949ee617e2c49dd96fc9755afb8e5274bf648ddd3242a4b8f5f3de87152856`  
		Last Modified: Fri, 03 Oct 2025 00:07:56 GMT  
		Size: 352.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2be7b29a546c3283ccd67b8d9f884db97ec31890926924c9269bd457b918f136`  
		Last Modified: Fri, 03 Oct 2025 00:07:57 GMT  
		Size: 6.1 MB (6073643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfd29f91d559e1e9ec9358ebc6feaf3a1679e8f690378d00f030f72cbd0b2c27`  
		Last Modified: Fri, 03 Oct 2025 00:07:56 GMT  
		Size: 2.1 KB (2092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbdea3629fb67453829dc580d761fdda1a4780227390f1d7e4e7e072efa20d80`  
		Last Modified: Fri, 03 Oct 2025 00:07:56 GMT  
		Size: 1.7 KB (1693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71e58c6d48af85ec991010f68a428197f3dd6ee70c0817a21abcd7d4616c2b6b`  
		Last Modified: Fri, 03 Oct 2025 00:07:56 GMT  
		Size: 502.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:483e6ed7417c271a427844f15a84754236002b28ccc6ad62ce17d2a3073a1500`  
		Last Modified: Fri, 03 Oct 2025 00:07:56 GMT  
		Size: 548.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f50f7d57b15078176ddf176e7a3bb07d45cc9d18f723452dcb9c9aff767884c4`  
		Last Modified: Fri, 03 Oct 2025 00:07:56 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:latest` - unknown; unknown

```console
$ docker pull yourls@sha256:e611d5a7013da34c0085a241256d82db51705ed30c8a3e94036dee0fea937e78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 KB (49132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e343138898c339788ddda27c62034d810d6bc62d654ae37ba8d62a8ec59a4bb9`

```dockerfile
```

-	Layers:
	-	`sha256:3eb275d942bb8ee46031bc6eedbb208328485de93edd93632efd777bf001266d`  
		Last Modified: Fri, 03 Oct 2025 01:42:34 GMT  
		Size: 49.1 KB (49132 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:latest` - linux; s390x

```console
$ docker pull yourls@sha256:4499293728e478b8ff7060bc9552d711ffa56e1e794a61a68c3a7d54f15c5457
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.1 MB (160118204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:876ff06e3dd52c72791c05362332bd34f4eb4c14a49253ddbb302c29d31b398f`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 19 Aug 2025 10:14:17 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1759104000'
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
ENV PHP_VERSION=8.4.13
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
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
	-	`sha256:924b0740f35a15fc20142be5c392f6b033c8051daecf16d2db38c22d6d73eb53`  
		Last Modified: Mon, 29 Sep 2025 23:41:29 GMT  
		Size: 29.8 MB (29837230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af9ee178226f7ea0f482af09b7dc3ba5fca7c07de96e60ad828b1737709e6b19`  
		Last Modified: Tue, 30 Sep 2025 06:40:13 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8b8c6f589e7cb0b9aff90a6df6a7cccfae60ed23d9fc4328b15d0c44aa0266e`  
		Last Modified: Tue, 30 Sep 2025 06:40:25 GMT  
		Size: 92.6 MB (92564454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:674ff7c7e8a7de8708af6056d40b56dffeb3ae246f618226bf482e0f207ff014`  
		Last Modified: Tue, 30 Sep 2025 06:40:14 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:763a4110d360212ee6e0ff8a1ea6d731b2aaff510a71163b8a748a26aa60e590`  
		Last Modified: Tue, 30 Sep 2025 06:44:29 GMT  
		Size: 4.3 MB (4320480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:763509a8474369ab3c7c1528f033ff966ec368402debfbc88d137b2f4ab19403`  
		Last Modified: Tue, 30 Sep 2025 06:44:30 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:263d5e9b63e43b1a0a70264c4610e6f5dd857a8d5245e08b172e026ecb396e1a`  
		Last Modified: Tue, 30 Sep 2025 06:44:30 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff2a8da208f5742ef485d7df3b045a3ee008dace4a0f3c74c21399cb0b4395bf`  
		Last Modified: Wed, 01 Oct 2025 09:57:26 GMT  
		Size: 13.8 MB (13810459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eef927aca5f2e77086c8d7e4876ac5d757d7ca47cfb930ff51450cb9ea0c88d9`  
		Last Modified: Tue, 30 Sep 2025 07:48:28 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6679c42a80b3f33645fbbc6946af479eb30c3716c48153751ea5099583628924`  
		Last Modified: Wed, 01 Oct 2025 08:22:03 GMT  
		Size: 13.3 MB (13299973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1095250d1ddd2cf072ceb920e16eae75200e297ddf141e948b3dcfd8faccde6`  
		Last Modified: Tue, 30 Sep 2025 07:48:27 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f19db5b2fd11ae4734c9d47c4c6a8873df725d1490f1b7908f714251b7289c2`  
		Last Modified: Tue, 30 Sep 2025 07:48:27 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2023b2b5bb2dbf59dc8cbfeca356804953fd26ee6277e94db1a5d83a92ebaeb2`  
		Last Modified: Tue, 30 Sep 2025 07:48:27 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:469f2b102920ac1d3d90e5efe4e20e323352e6ab10b70559622a26d509833068`  
		Last Modified: Tue, 30 Sep 2025 07:48:28 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ac07ec508ae8bbca78af58210c5b7e72a9cb2587e0e679521f01f4503904b6a`  
		Last Modified: Tue, 30 Sep 2025 15:44:06 GMT  
		Size: 200.4 KB (200407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b761d012687422a10fc6702e3339c6af594bf1b3348492a2ae4840f81931009`  
		Last Modified: Tue, 30 Sep 2025 15:44:06 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ab3def2753308a1b4e90fec5e402fe716fd27204311576741c283f91380c9a3`  
		Last Modified: Tue, 30 Sep 2025 15:44:06 GMT  
		Size: 342.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0957bfa440555a9e098aaa6e8b89afc81eaf3547a09250b162189dd0250f99d`  
		Last Modified: Tue, 30 Sep 2025 15:44:06 GMT  
		Size: 6.1 MB (6073646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d5fade08c60cf1cb29fb01493a0e8f6f805cd9f17fa7e998015ce10f16c2d3f`  
		Last Modified: Tue, 30 Sep 2025 15:44:06 GMT  
		Size: 2.1 KB (2094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d572b2ec88b95fcc791a7319ae7086570c48ec29bfaffc550564bb09c178c46c`  
		Last Modified: Tue, 30 Sep 2025 15:44:06 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:010ed3e52c1aca8c47640a4c07339807a6be7c11182e1acd3f986e6b04b271ff`  
		Last Modified: Tue, 30 Sep 2025 15:44:06 GMT  
		Size: 500.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:324e59aa4fe1295ce08807d9fa312ecabe350b9a9e03b416c3902e44002abb52`  
		Last Modified: Tue, 30 Sep 2025 15:44:07 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89470447f4acb9d755b02f10ce93a4cf5225d4215fd62428a320010da4b6d3a8`  
		Last Modified: Tue, 30 Sep 2025 15:44:07 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:latest` - unknown; unknown

```console
$ docker pull yourls@sha256:e3621b405e993050da52a7af9a4a86109c72aeb6caee7f681e7060b69dffdc02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 KB (49046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e426550b360a65e207f7de91b79c635ff37ebd49d32cfcc6733f8db94eb9146e`

```dockerfile
```

-	Layers:
	-	`sha256:17f5a6fb14de3dafb617ef9aae8b8f27fc999ae7552ce36a383e667bcad9409d`  
		Last Modified: Wed, 01 Oct 2025 22:43:09 GMT  
		Size: 49.0 KB (49046 bytes)  
		MIME: application/vnd.in-toto+json
