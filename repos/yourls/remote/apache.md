## `yourls:apache`

```console
$ docker pull yourls@sha256:136a2c95bf362cd3aa6043f31e19f38f91237fbd57fd298a85fb31793041a2f5
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

### `yourls:apache` - linux; amd64

```console
$ docker pull yourls@sha256:fef31aacc6782b3ee2a4632c96d68a6bf31845c8438accea177212a7647defc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.5 MB (187509148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:893f62dc8a3063a3e3b098b72af775bfc34bb356c816cade49b30d1923f3042d`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:05:12 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 24 Feb 2026 19:05:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 24 Feb 2026 19:05:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 19:05:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 24 Feb 2026 19:05:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 24 Feb 2026 19:05:28 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 24 Feb 2026 19:05:28 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 24 Feb 2026 19:05:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 24 Feb 2026 19:05:34 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 24 Feb 2026 19:05:34 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 24 Feb 2026 19:05:34 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 24 Feb 2026 19:05:34 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 24 Feb 2026 19:05:34 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 24 Feb 2026 19:05:34 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Tue, 24 Feb 2026 19:05:34 GMT
ENV PHP_VERSION=8.5.3
# Tue, 24 Feb 2026 19:05:34 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.3.tar.xz.asc
# Tue, 24 Feb 2026 19:05:34 GMT
ENV PHP_SHA256=ce65725b8af07356b69a6046d21487040b11f2acfde786de38b2bfb712c36eb9
# Tue, 24 Feb 2026 19:05:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 24 Feb 2026 19:05:42 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:08:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 24 Feb 2026 19:08:23 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:08:24 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 24 Feb 2026 19:08:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 24 Feb 2026 19:08:24 GMT
STOPSIGNAL SIGWINCH
# Tue, 24 Feb 2026 19:08:24 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:08:24 GMT
WORKDIR /var/www/html
# Tue, 24 Feb 2026 19:08:24 GMT
EXPOSE map[80/tcp:{}]
# Tue, 24 Feb 2026 19:08:24 GMT
CMD ["apache2-foreground"]
# Tue, 24 Feb 2026 20:02:14 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)"     bcmath     pdo_mysql     mysqli # buildkit
# Tue, 24 Feb 2026 20:02:14 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Tue, 24 Feb 2026 20:02:14 GMT
RUN a2enmod rewrite expires # buildkit
# Tue, 24 Feb 2026 20:02:15 GMT
ARG YOURLS_VERSION=1.10.3
# Tue, 24 Feb 2026 20:02:15 GMT
ARG YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
# Tue, 24 Feb 2026 20:02:15 GMT
ENV YOURLS_VERSION=1.10.3
# Tue, 24 Feb 2026 20:02:15 GMT
ENV YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
# Tue, 24 Feb 2026 20:02:15 GMT
# ARGS: YOURLS_VERSION=1.10.3 YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Tue, 24 Feb 2026 20:02:15 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Tue, 24 Feb 2026 20:02:15 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 20:02:15 GMT
COPY files/vhost.conf /etc/apache2/sites-available/000-default.conf # buildkit
# Tue, 24 Feb 2026 20:02:15 GMT
COPY files/vhost-https.conf /etc/apache2/sites-available/default-ssl.conf # buildkit
# Tue, 24 Feb 2026 20:02:15 GMT
COPY files/ports.conf /etc/apache2/ports.conf # buildkit
# Tue, 24 Feb 2026 20:02:15 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 24 Feb 2026 20:02:15 GMT
EXPOSE map[8443/tcp:{}]
# Tue, 24 Feb 2026 20:02:15 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Tue, 24 Feb 2026 20:02:15 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0611f64ef45fd78ef77f69e1995f558d81144c9dc878ca8ad9cc586003480c2f`  
		Last Modified: Tue, 24 Feb 2026 19:08:45 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5252fd260ba37956ebfa8da863076c0d00d82e0fd13023735c64e595833f3a37`  
		Last Modified: Tue, 24 Feb 2026 19:08:48 GMT  
		Size: 117.8 MB (117842080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:168aadd03370254c93a5e16724e8b610b6285b185b2dac60048168f6dd7d1e08`  
		Last Modified: Tue, 24 Feb 2026 19:08:45 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa3c80b0439a3562a4f66c482a6c5a52bc239e30587f9111376230934899e5f5`  
		Last Modified: Tue, 24 Feb 2026 19:08:45 GMT  
		Size: 4.2 MB (4226882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c22de04ade796bff6c9e06ade2bb3e782049b667433d09577fa0e10436dcdc0b`  
		Last Modified: Tue, 24 Feb 2026 19:08:46 GMT  
		Size: 435.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9cff660e7f87eefeeedc1123e4ae16265a8baa78446b432f914632eac1af7e2`  
		Last Modified: Tue, 24 Feb 2026 19:08:46 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6e63e0f7a6c20792db383cc2fb62e0002e7b2860db4d6d43bd42d1e3c7669e0`  
		Last Modified: Tue, 24 Feb 2026 19:08:47 GMT  
		Size: 14.5 MB (14499815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:449561b0f49137a1412cd5897646a956651b0b013ddafeae61f496e71b3d8227`  
		Last Modified: Tue, 24 Feb 2026 19:08:47 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b6b8f3b26f603b85b1c79e941ddae399b5e8a73e6f6bd811ff54b63875837ea`  
		Last Modified: Tue, 24 Feb 2026 19:08:48 GMT  
		Size: 15.0 MB (14993115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79ddc08849ab3c8f98cfe74453f5bcd386e54b3cec03b0a93c2bba8fab63c198`  
		Last Modified: Tue, 24 Feb 2026 19:08:48 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0151a0053bd37ede0826c76f388645166d5ad7c0d9186677c2124d805326b448`  
		Last Modified: Tue, 24 Feb 2026 19:08:49 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e8a4ce29dfe4efe5201a140b785d65b94a9805068ea509b23208b0195cef0bc`  
		Last Modified: Tue, 24 Feb 2026 19:08:49 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:974e4368c17c5709f29383e0caed9b3bce5dfec9d104c89ecf48d45cda962c80`  
		Last Modified: Tue, 24 Feb 2026 20:02:20 GMT  
		Size: 108.4 KB (108375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d241644c9a4d9ebc979b3efb8db9474e469eb12be057498a1446e4ee3457af0c`  
		Last Modified: Tue, 24 Feb 2026 20:02:20 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d805e7e3c5bc13a6b0a07e4839655d5aa9a880ebbb89c820488a57e6a4fc2933`  
		Last Modified: Tue, 24 Feb 2026 20:02:20 GMT  
		Size: 342.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61596bbf50b1ec0cf3b2ae3cb6bdfbe2ad7efa24da77858c7fa937d09b2f3bd1`  
		Last Modified: Tue, 24 Feb 2026 20:02:21 GMT  
		Size: 6.0 MB (6048926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19746c27606f4e1a0a4f767bc510f9683855417c1714f037f10449f9e4db9936`  
		Last Modified: Tue, 24 Feb 2026 20:02:21 GMT  
		Size: 2.1 KB (2096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7158eb9ffd4e5be8028efb72f2cae345304659f7f52f9e90bf5a69bf74224b71`  
		Last Modified: Tue, 24 Feb 2026 20:02:21 GMT  
		Size: 1.7 KB (1695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cdfdcb93a4f47081ceb6d5a56c796eb78f88ca4f5724ba7bff35849b50e8371`  
		Last Modified: Tue, 24 Feb 2026 20:02:22 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20c5e0a38f49ec89fc72aa805cc662cfda0416afe18613d29f74ae387e63f7c4`  
		Last Modified: Tue, 24 Feb 2026 20:02:22 GMT  
		Size: 548.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d95f994abced3cb8d31562508a08ed7f5fdecd79dc7083f6363637f1cea21e74`  
		Last Modified: Tue, 24 Feb 2026 20:02:23 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:apache` - unknown; unknown

```console
$ docker pull yourls@sha256:a998fbabfe79c83cd5b57d85401ec66383549bf167c6c122670e727bf2e06914
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.6 KB (47589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdcb3dd678d0cfb804a7b9b743068aedc8c511ecc4a7a1a030389749c2131103`

```dockerfile
```

-	Layers:
	-	`sha256:38384693e4131c3f31d035a29dc484474ed1f6a9a8bb4983a0e27cd6ccca9339`  
		Last Modified: Tue, 24 Feb 2026 20:02:20 GMT  
		Size: 47.6 KB (47589 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:apache` - linux; arm variant v5

```console
$ docker pull yourls@sha256:ca580a3a73aacc0d02b17f92b7c2f7418cba15fb858f1f41761c6c4062325eda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.7 MB (160686792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a395368e6a7fa8283649b4165e9a2c2f1a67f3f5c0734cb941bcb776aec1a6f3`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:01:03 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 24 Feb 2026 19:01:25 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 24 Feb 2026 19:01:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 19:01:25 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 24 Feb 2026 19:01:25 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 24 Feb 2026 19:01:25 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 24 Feb 2026 19:01:25 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 24 Feb 2026 19:01:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 24 Feb 2026 19:01:36 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 24 Feb 2026 19:01:36 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 24 Feb 2026 19:01:36 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 24 Feb 2026 19:01:36 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 24 Feb 2026 19:01:36 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 24 Feb 2026 19:01:36 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Tue, 24 Feb 2026 19:01:36 GMT
ENV PHP_VERSION=8.5.3
# Tue, 24 Feb 2026 19:01:36 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.3.tar.xz.asc
# Tue, 24 Feb 2026 19:01:36 GMT
ENV PHP_SHA256=ce65725b8af07356b69a6046d21487040b11f2acfde786de38b2bfb712c36eb9
# Tue, 24 Feb 2026 19:01:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 24 Feb 2026 19:01:49 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:05:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 24 Feb 2026 19:05:19 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:05:19 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 24 Feb 2026 19:05:19 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 24 Feb 2026 19:05:19 GMT
STOPSIGNAL SIGWINCH
# Tue, 24 Feb 2026 19:05:19 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:05:19 GMT
WORKDIR /var/www/html
# Tue, 24 Feb 2026 19:05:19 GMT
EXPOSE map[80/tcp:{}]
# Tue, 24 Feb 2026 19:05:19 GMT
CMD ["apache2-foreground"]
# Tue, 24 Feb 2026 21:14:42 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)"     bcmath     pdo_mysql     mysqli # buildkit
# Tue, 24 Feb 2026 21:14:42 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Tue, 24 Feb 2026 21:14:42 GMT
RUN a2enmod rewrite expires # buildkit
# Tue, 24 Feb 2026 21:14:44 GMT
ARG YOURLS_VERSION=1.10.3
# Tue, 24 Feb 2026 21:14:44 GMT
ARG YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
# Tue, 24 Feb 2026 21:14:44 GMT
ENV YOURLS_VERSION=1.10.3
# Tue, 24 Feb 2026 21:14:44 GMT
ENV YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
# Tue, 24 Feb 2026 21:14:44 GMT
# ARGS: YOURLS_VERSION=1.10.3 YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Tue, 24 Feb 2026 21:14:44 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Tue, 24 Feb 2026 21:14:44 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 21:14:44 GMT
COPY files/vhost.conf /etc/apache2/sites-available/000-default.conf # buildkit
# Tue, 24 Feb 2026 21:14:44 GMT
COPY files/vhost-https.conf /etc/apache2/sites-available/default-ssl.conf # buildkit
# Tue, 24 Feb 2026 21:14:44 GMT
COPY files/ports.conf /etc/apache2/ports.conf # buildkit
# Tue, 24 Feb 2026 21:14:44 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 24 Feb 2026 21:14:44 GMT
EXPOSE map[8443/tcp:{}]
# Tue, 24 Feb 2026 21:14:44 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Tue, 24 Feb 2026 21:14:44 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:280a075cc1d2a97445b9f4430aa9774bfc38fc4217b7fc9d6a7b04e7e431cb65`  
		Last Modified: Tue, 24 Feb 2026 18:42:44 GMT  
		Size: 27.9 MB (27947608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dd3ffaae4db8d4d193f68a92da67ec3b7a69eaea4ce3e6023fdb125156bb47d`  
		Last Modified: Tue, 24 Feb 2026 19:05:39 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3c565f50bf180f2fb2aa586a88b356e0c22803e7b8d0d85c74f93b10229d5a6`  
		Last Modified: Tue, 24 Feb 2026 19:05:42 GMT  
		Size: 94.9 MB (94884182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03f318ec1fe3c296306ee9a5d7bf4364177c3fe97a1c8b15af6256088d2f5170`  
		Last Modified: Tue, 24 Feb 2026 19:05:13 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:313c2c5d45f0e41b2d8aa0d16f4010707da6cdc68ba4e77dc9ea96542e2807b1`  
		Last Modified: Tue, 24 Feb 2026 19:05:40 GMT  
		Size: 4.1 MB (4088889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5873bee331f7a6f26373ea45ef14e843dd6489674ac806e3d1e948f6ce0e1a54`  
		Last Modified: Tue, 24 Feb 2026 19:05:40 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5db5cd29f45d937dd542498d94a91e09e4a8d029645924a89e9371f4784a9d01`  
		Last Modified: Tue, 24 Feb 2026 19:05:41 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af0cdb780ff24b02540c8cda9b61fc758c3cccdc6c8e827a7c9607b59616a0fc`  
		Last Modified: Tue, 24 Feb 2026 19:05:41 GMT  
		Size: 14.5 MB (14497090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9dbbaf214ba692dee5da588de721f90459711181d116b36dccc91af16be5ef1`  
		Last Modified: Tue, 24 Feb 2026 19:05:42 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac6e37c08ac1bafaf430bb892155f8a0e18965400466d914684b5e4fabca316c`  
		Last Modified: Tue, 24 Feb 2026 19:05:42 GMT  
		Size: 13.1 MB (13111807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86dc9e34e9d18d9779e4c42bd012f9c2d484b4370e75ed343cf65f15c0d5ef52`  
		Last Modified: Tue, 24 Feb 2026 19:05:43 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e28ab4e62e8181c84a1cf143f6dc01bc517b252fa93373a69f0c2083d28d074d`  
		Last Modified: Tue, 24 Feb 2026 19:05:43 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:063c2ee3e43ce9b5115f5eb836aebd36b75092934d1b68a04076ccaa6ecd4726`  
		Last Modified: Tue, 24 Feb 2026 19:05:43 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:165820368a5c5f620b9a4a919370b3da3790f4c3b6236b2011246632be9d6ed0`  
		Last Modified: Tue, 24 Feb 2026 21:14:49 GMT  
		Size: 97.0 KB (96974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4664dc0a1c7f2ad8bcd11ef242f49b45993792d77eb47b88a4ee9b2c202d6eb6`  
		Last Modified: Tue, 24 Feb 2026 21:14:49 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:637043f8ffb7490640836aadb6492959a4874490d318942b75137743e2537f07`  
		Last Modified: Tue, 24 Feb 2026 21:14:49 GMT  
		Size: 346.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35dd934f323434463332b462cca01b64f94a4f5e0cfab9ffb3776925396cd030`  
		Last Modified: Tue, 24 Feb 2026 21:14:50 GMT  
		Size: 6.0 MB (6048925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15bc94532737599886dcc21a80f0ce35f936e10567177805b214cf501929db81`  
		Last Modified: Tue, 24 Feb 2026 21:14:50 GMT  
		Size: 2.1 KB (2095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:906304cb117439412afb1cb9e215da4ecbe3fcf51ba77c7b2523e2fcdb2b4e69`  
		Last Modified: Tue, 24 Feb 2026 21:14:50 GMT  
		Size: 1.7 KB (1693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:095b8cd02ffbbd16eb14a55b575e7067e99f162083a56062a0f00f0f4fbf80ce`  
		Last Modified: Tue, 24 Feb 2026 21:14:50 GMT  
		Size: 502.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73116d38d02638e51004026640f0046f25bb758a5ed6ee4e2c884ebad4b8b00f`  
		Last Modified: Tue, 24 Feb 2026 21:14:51 GMT  
		Size: 548.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47886347fb487f550ae0a75f710bd898d1fac28abbd7fefbe5e0575572b254b2`  
		Last Modified: Tue, 24 Feb 2026 21:14:52 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:apache` - unknown; unknown

```console
$ docker pull yourls@sha256:553e09c684156d2f4069d5eb80a0c7e823543b1101beade961a9d74fd35387a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 KB (47721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:505e29b823432110fd21c15ff7fa899433e13ee1fb9e43af6a2125385d27c818`

```dockerfile
```

-	Layers:
	-	`sha256:68dc28d74932f0c10d9b54e5bcaf27f3b76bcfeed4861499f8cedf2fc370b030`  
		Last Modified: Tue, 24 Feb 2026 21:14:49 GMT  
		Size: 47.7 KB (47721 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:apache` - linux; arm variant v7

```console
$ docker pull yourls@sha256:d8c48b1e8e25a31a392eff99936c5e3e013bcf40ad097031ec49a9cbfcad25a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.4 MB (149363820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c12c7498a0340ac8dfca36d7a625c5df1840c4222f10487516f4dce46f5dc4c2`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:07:10 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 24 Feb 2026 19:07:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 24 Feb 2026 19:07:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 19:07:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 24 Feb 2026 19:07:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 24 Feb 2026 19:07:27 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 24 Feb 2026 19:07:27 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 24 Feb 2026 19:07:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 24 Feb 2026 19:07:35 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 24 Feb 2026 19:07:35 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 24 Feb 2026 19:07:35 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 24 Feb 2026 19:07:35 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 24 Feb 2026 19:07:35 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 24 Feb 2026 19:07:35 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Tue, 24 Feb 2026 19:07:35 GMT
ENV PHP_VERSION=8.5.3
# Tue, 24 Feb 2026 19:07:35 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.3.tar.xz.asc
# Tue, 24 Feb 2026 19:07:35 GMT
ENV PHP_SHA256=ce65725b8af07356b69a6046d21487040b11f2acfde786de38b2bfb712c36eb9
# Tue, 24 Feb 2026 19:07:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 24 Feb 2026 19:07:46 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:10:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 24 Feb 2026 19:10:46 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:10:47 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 24 Feb 2026 19:10:47 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 24 Feb 2026 19:10:47 GMT
STOPSIGNAL SIGWINCH
# Tue, 24 Feb 2026 19:10:47 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:10:47 GMT
WORKDIR /var/www/html
# Tue, 24 Feb 2026 19:10:47 GMT
EXPOSE map[80/tcp:{}]
# Tue, 24 Feb 2026 19:10:47 GMT
CMD ["apache2-foreground"]
# Tue, 24 Feb 2026 21:33:09 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)"     bcmath     pdo_mysql     mysqli # buildkit
# Tue, 24 Feb 2026 21:33:09 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Tue, 24 Feb 2026 21:33:09 GMT
RUN a2enmod rewrite expires # buildkit
# Tue, 24 Feb 2026 21:33:11 GMT
ARG YOURLS_VERSION=1.10.3
# Tue, 24 Feb 2026 21:33:11 GMT
ARG YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
# Tue, 24 Feb 2026 21:33:11 GMT
ENV YOURLS_VERSION=1.10.3
# Tue, 24 Feb 2026 21:33:11 GMT
ENV YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
# Tue, 24 Feb 2026 21:33:11 GMT
# ARGS: YOURLS_VERSION=1.10.3 YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Tue, 24 Feb 2026 21:33:11 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Tue, 24 Feb 2026 21:33:11 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 21:33:11 GMT
COPY files/vhost.conf /etc/apache2/sites-available/000-default.conf # buildkit
# Tue, 24 Feb 2026 21:33:11 GMT
COPY files/vhost-https.conf /etc/apache2/sites-available/default-ssl.conf # buildkit
# Tue, 24 Feb 2026 21:33:11 GMT
COPY files/ports.conf /etc/apache2/ports.conf # buildkit
# Tue, 24 Feb 2026 21:33:11 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 24 Feb 2026 21:33:11 GMT
EXPOSE map[8443/tcp:{}]
# Tue, 24 Feb 2026 21:33:11 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Tue, 24 Feb 2026 21:33:11 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:be1f02cfc6708a9e39fcae481bc45544f342901641dd63341104a8ef3fa3cde9`  
		Last Modified: Tue, 24 Feb 2026 18:42:48 GMT  
		Size: 26.2 MB (26213745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b6636b876bece8c836f6910807082ab17b34c13cfdc952a478bbf4353921abf`  
		Last Modified: Tue, 24 Feb 2026 19:11:04 GMT  
		Size: 229.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34efc6e916bbabcb0aff2603abf63130df04d671d870577129a0ec91061dc555`  
		Last Modified: Tue, 24 Feb 2026 19:11:06 GMT  
		Size: 86.2 MB (86246140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82f86a71f509d2bf86922105d26eb06efb86b1eedfbeb3336db0fbf69122a693`  
		Last Modified: Tue, 24 Feb 2026 19:11:04 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b760ca4d7665fb7537b87dbb24d1ac236936362bf5b54b4e3abf1edad1b862c`  
		Last Modified: Tue, 24 Feb 2026 19:11:04 GMT  
		Size: 3.8 MB (3757558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3db9ce0f06d8140bcbe9dd190b1b0ee424d9fe3aab898f0bc5e8d59744bafc18`  
		Last Modified: Tue, 24 Feb 2026 19:11:05 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33f46002b29792f1f5c6fc21cd1453926c5c20559f937392180979fc4558cc10`  
		Last Modified: Tue, 24 Feb 2026 19:11:05 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3506b2fca9d8c63bb87f2200cc1ca22da9b5d87f8926a393ac3f6f7944491ebc`  
		Last Modified: Tue, 24 Feb 2026 19:11:06 GMT  
		Size: 14.5 MB (14497210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:350537f51fd37fd21d4d474945a2e49131175e6a30a3473df9733a2ff3f88aa8`  
		Last Modified: Tue, 24 Feb 2026 19:11:06 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdfea2e27efc630ffae903961e6564a3f6d31bac8b74e51fe29188632cc2584b`  
		Last Modified: Tue, 24 Feb 2026 19:11:07 GMT  
		Size: 12.5 MB (12498056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:132f645ab2b08b7815a9afaee951d4cd37f4ea9e2767cf3d6350735eb9af2f96`  
		Last Modified: Tue, 24 Feb 2026 19:11:07 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:204279542b2470dab3a8f8d58e752ee53934f41babda73c21b6e96f34f0fbe98`  
		Last Modified: Tue, 24 Feb 2026 19:11:07 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:497a4e0c8e7f03eed5cbcd36895db8c8c303ea9846cfbaec3cbf508d67d50d7d`  
		Last Modified: Tue, 24 Feb 2026 19:11:08 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:391df7bdf006d0d3e6c333a908e683d62ef22484622ace18f1a235ab40794de0`  
		Last Modified: Tue, 24 Feb 2026 21:33:16 GMT  
		Size: 90.9 KB (90866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93ce53b297e7687630c1c7a5d47fc304a9266a4f5d8e6aebf867679721c7eb2c`  
		Last Modified: Tue, 24 Feb 2026 21:33:16 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:110d27acedd9888fa668b32a4e185b81b153b6b1d53d025c79fcaf18868b3798`  
		Last Modified: Tue, 24 Feb 2026 21:33:16 GMT  
		Size: 343.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d406155427b8fd1a3c20de85ba5fc4d62bb39f966afc8230628549e23350c1b5`  
		Last Modified: Tue, 24 Feb 2026 21:33:17 GMT  
		Size: 6.0 MB (6048924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bd125b7e150cf27adaaa4ce9a04e3816282f5f7464b9813d5064195835994ea`  
		Last Modified: Tue, 24 Feb 2026 21:33:17 GMT  
		Size: 2.1 KB (2093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d876aecbb0ea87bfcda4bf802df4457a6e75b51a99828fcaaf288ffcd4429df2`  
		Last Modified: Tue, 24 Feb 2026 21:33:17 GMT  
		Size: 1.7 KB (1694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdea2624c5e7f51a6a609644f566ef276a5458850ce71e2afe3614aa10eb6e85`  
		Last Modified: Tue, 24 Feb 2026 21:33:17 GMT  
		Size: 501.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53475d42b5a34a048c0da3995aebe5682de172a5716ddd11564d655a85fab0f0`  
		Last Modified: Tue, 24 Feb 2026 21:33:18 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c590c06cf279ffc7a1a915b44782ccd8913fc5852d7864961b8710aac1c624b0`  
		Last Modified: Tue, 24 Feb 2026 21:33:18 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:apache` - unknown; unknown

```console
$ docker pull yourls@sha256:7ae242d7db4d4825dc2743482033a30f8a06398620f6d636b3ef0ab20901d37a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 KB (47720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71b2381bfdeb56367b657051fedf93d884422fd7d5610d7f0cdfe6b582c57551`

```dockerfile
```

-	Layers:
	-	`sha256:4b9c69ba82d053b722013c4caa7005e26b7f91003b26a4aec19fe86ba5b846e0`  
		Last Modified: Tue, 24 Feb 2026 21:33:16 GMT  
		Size: 47.7 KB (47720 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:apache` - linux; arm64 variant v8

```console
$ docker pull yourls@sha256:7de713bd3c69ca9ec65367f596f899b240c473d064e6d0a515abfdf0629c5ca9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.8 MB (179835837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1d2b296a677452efb0cbed6b451d0e7c25e119dbf184917fce0abfe6fb2b216`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:08:44 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 24 Feb 2026 19:09:00 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 24 Feb 2026 19:09:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 19:09:00 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 24 Feb 2026 19:09:00 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 24 Feb 2026 19:09:00 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 24 Feb 2026 19:09:00 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 24 Feb 2026 19:09:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 24 Feb 2026 19:09:07 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 24 Feb 2026 19:09:07 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 24 Feb 2026 19:09:07 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 24 Feb 2026 19:09:07 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 24 Feb 2026 19:09:07 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 24 Feb 2026 19:09:07 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Tue, 24 Feb 2026 19:09:07 GMT
ENV PHP_VERSION=8.5.3
# Tue, 24 Feb 2026 19:09:07 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.3.tar.xz.asc
# Tue, 24 Feb 2026 19:09:07 GMT
ENV PHP_SHA256=ce65725b8af07356b69a6046d21487040b11f2acfde786de38b2bfb712c36eb9
# Tue, 24 Feb 2026 19:09:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 24 Feb 2026 19:09:16 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:12:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 24 Feb 2026 19:12:34 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:12:34 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 24 Feb 2026 19:12:34 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 24 Feb 2026 19:12:34 GMT
STOPSIGNAL SIGWINCH
# Tue, 24 Feb 2026 19:12:34 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:12:34 GMT
WORKDIR /var/www/html
# Tue, 24 Feb 2026 19:12:34 GMT
EXPOSE map[80/tcp:{}]
# Tue, 24 Feb 2026 19:12:34 GMT
CMD ["apache2-foreground"]
# Tue, 24 Feb 2026 20:12:49 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)"     bcmath     pdo_mysql     mysqli # buildkit
# Tue, 24 Feb 2026 20:12:49 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Tue, 24 Feb 2026 20:12:50 GMT
RUN a2enmod rewrite expires # buildkit
# Tue, 24 Feb 2026 20:12:52 GMT
ARG YOURLS_VERSION=1.10.3
# Tue, 24 Feb 2026 20:12:52 GMT
ARG YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
# Tue, 24 Feb 2026 20:12:52 GMT
ENV YOURLS_VERSION=1.10.3
# Tue, 24 Feb 2026 20:12:52 GMT
ENV YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
# Tue, 24 Feb 2026 20:12:52 GMT
# ARGS: YOURLS_VERSION=1.10.3 YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Tue, 24 Feb 2026 20:12:52 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Tue, 24 Feb 2026 20:12:52 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 20:12:52 GMT
COPY files/vhost.conf /etc/apache2/sites-available/000-default.conf # buildkit
# Tue, 24 Feb 2026 20:12:52 GMT
COPY files/vhost-https.conf /etc/apache2/sites-available/default-ssl.conf # buildkit
# Tue, 24 Feb 2026 20:12:52 GMT
COPY files/ports.conf /etc/apache2/ports.conf # buildkit
# Tue, 24 Feb 2026 20:12:52 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 24 Feb 2026 20:12:52 GMT
EXPOSE map[8443/tcp:{}]
# Tue, 24 Feb 2026 20:12:52 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Tue, 24 Feb 2026 20:12:52 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f84db7efb4ab0d35e2e7f90e8e455de30b3a419634b894869cf27223fc554a7`  
		Last Modified: Tue, 24 Feb 2026 19:12:39 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3006e7dcf927a0151a097d4e7a80d1ef67f10f67fbf45cd9fde14354c7c2b0cc`  
		Last Modified: Tue, 24 Feb 2026 19:12:58 GMT  
		Size: 110.2 MB (110163199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03cace87c54d8810ebc82d7af3004a30d2f140d6040d9c5924bfc83feeda4f62`  
		Last Modified: Tue, 24 Feb 2026 19:12:39 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f414f8e4718df621fbe574248a5857ebc6ca88c796b5f764de5498b2b3dd4e6`  
		Last Modified: Tue, 24 Feb 2026 19:12:55 GMT  
		Size: 4.3 MB (4304900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbd77879a3701ed26ce7fa841eecf26475221efbdfab94cf410fed33ac342df1`  
		Last Modified: Tue, 24 Feb 2026 19:12:55 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12fc87bcf688383779927482b8e2ca72e587e32a01b95838162bb4489acc9725`  
		Last Modified: Tue, 24 Feb 2026 19:12:54 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:370a796d49c4fa6f261b1f63b939da1fcaca8641135f356d3c5a6585ba89a3b8`  
		Last Modified: Tue, 24 Feb 2026 19:12:56 GMT  
		Size: 14.5 MB (14499146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97ff788784287f3e7431d59bef2f19e31e2fcc07b2f5174b349f4fc1abb0c94d`  
		Last Modified: Tue, 24 Feb 2026 19:12:56 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee8f5103ad36076f49cf9c0fbc53c628e964d12b4e86683dc078253438b2ede`  
		Last Modified: Tue, 24 Feb 2026 19:12:57 GMT  
		Size: 14.6 MB (14562484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9f2ce81e164c4470eeed927e8225e9e417cc32bc70e201209a6b635103fad68`  
		Last Modified: Tue, 24 Feb 2026 19:12:57 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c70d743b7ee06ec8ac7bef3c35b3cc66b6ba31704c4446ebbf900a918af11ff`  
		Last Modified: Tue, 24 Feb 2026 19:12:58 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa48d74cda88d88ba72c58eec66e5f040e6272ec1f8c3d64240bc68a581c270e`  
		Last Modified: Tue, 24 Feb 2026 19:12:58 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd1014453eaa4fd5d798a095f48e81531bd7d1054865354316246d74e791c51a`  
		Last Modified: Tue, 24 Feb 2026 20:12:57 GMT  
		Size: 105.8 KB (105754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35050d0b6450b7bdfc1c67230a3746f15d4975b171cf210d7a3d1ac84a0898fb`  
		Last Modified: Tue, 24 Feb 2026 20:12:57 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40c8a912c8acd5e280cd5debb9ebaa92c5dc00debd1225e98ea2a2482777d221`  
		Last Modified: Tue, 24 Feb 2026 20:12:57 GMT  
		Size: 344.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35996612b8f29e735b85196641c53ac9b982009f6a8a2c0da32af51b2fa4cba4`  
		Last Modified: Tue, 24 Feb 2026 20:12:57 GMT  
		Size: 6.0 MB (6048926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:090d70052cfd31d7010b8057d7d38b1f754f509d7cca70f6a3524acc6b8ed538`  
		Last Modified: Tue, 24 Feb 2026 20:12:58 GMT  
		Size: 2.1 KB (2099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:317c7f5abb07899743f17711a55edd68bb523ef11d3923200feff461ee126109`  
		Last Modified: Tue, 24 Feb 2026 20:12:58 GMT  
		Size: 1.7 KB (1694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c061e7ab691902b608e23bb1475552cbb4d964ab54cc2304f8927a911ab48f0`  
		Last Modified: Tue, 24 Feb 2026 20:12:58 GMT  
		Size: 501.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82812b293a5643c4aa912ed95be76366bd06bee0fa84c5a7118361d8c927ea28`  
		Last Modified: Tue, 24 Feb 2026 20:12:58 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32ff8adc349f75ffcdfede8d599c2662f17e8806a910411c3411cd50523fd39e`  
		Last Modified: Tue, 24 Feb 2026 20:12:59 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:apache` - unknown; unknown

```console
$ docker pull yourls@sha256:d024857df66b02c76e3af77436704390b0f5dc6da07d07c2c2a7c44de93722c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 KB (47786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cbd0b6341729d644f7ef059546649c1c2b3c60f57dc54aabaf15f7f7cc3172f`

```dockerfile
```

-	Layers:
	-	`sha256:d6c16d72880e01679b5f673a34d342b6c65430c7cd61d6de6d7e11531ef1cd08`  
		Last Modified: Tue, 24 Feb 2026 20:12:57 GMT  
		Size: 47.8 KB (47786 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:apache` - linux; 386

```console
$ docker pull yourls@sha256:f3eae3d1ff39d237cfacd370f736cb0f0b0a0c975263cc9137fa33c28b98488e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.9 MB (187910445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3114023fbf8153512a6b6433f9a513174cc53940df7a0892077aa783fa03c2aa`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 18:59:40 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 24 Feb 2026 18:59:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 24 Feb 2026 18:59:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 18:59:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 24 Feb 2026 18:59:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 24 Feb 2026 18:59:58 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 24 Feb 2026 18:59:58 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 24 Feb 2026 19:00:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 24 Feb 2026 19:00:05 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 24 Feb 2026 19:00:05 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 24 Feb 2026 19:00:05 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 24 Feb 2026 19:00:05 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 24 Feb 2026 19:00:05 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 24 Feb 2026 19:00:05 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Tue, 24 Feb 2026 19:00:05 GMT
ENV PHP_VERSION=8.5.3
# Tue, 24 Feb 2026 19:00:05 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.3.tar.xz.asc
# Tue, 24 Feb 2026 19:00:05 GMT
ENV PHP_SHA256=ce65725b8af07356b69a6046d21487040b11f2acfde786de38b2bfb712c36eb9
# Tue, 24 Feb 2026 19:00:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 24 Feb 2026 19:00:15 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:03:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 24 Feb 2026 19:03:30 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:03:30 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 24 Feb 2026 19:03:30 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 24 Feb 2026 19:03:30 GMT
STOPSIGNAL SIGWINCH
# Tue, 24 Feb 2026 19:03:30 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:03:30 GMT
WORKDIR /var/www/html
# Tue, 24 Feb 2026 19:03:30 GMT
EXPOSE map[80/tcp:{}]
# Tue, 24 Feb 2026 19:03:30 GMT
CMD ["apache2-foreground"]
# Tue, 24 Feb 2026 19:56:05 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)"     bcmath     pdo_mysql     mysqli # buildkit
# Tue, 24 Feb 2026 19:56:05 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Tue, 24 Feb 2026 19:56:05 GMT
RUN a2enmod rewrite expires # buildkit
# Tue, 24 Feb 2026 19:56:07 GMT
ARG YOURLS_VERSION=1.10.3
# Tue, 24 Feb 2026 19:56:07 GMT
ARG YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
# Tue, 24 Feb 2026 19:56:07 GMT
ENV YOURLS_VERSION=1.10.3
# Tue, 24 Feb 2026 19:56:07 GMT
ENV YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
# Tue, 24 Feb 2026 19:56:07 GMT
# ARGS: YOURLS_VERSION=1.10.3 YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Tue, 24 Feb 2026 19:56:07 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Tue, 24 Feb 2026 19:56:07 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:56:07 GMT
COPY files/vhost.conf /etc/apache2/sites-available/000-default.conf # buildkit
# Tue, 24 Feb 2026 19:56:07 GMT
COPY files/vhost-https.conf /etc/apache2/sites-available/default-ssl.conf # buildkit
# Tue, 24 Feb 2026 19:56:07 GMT
COPY files/ports.conf /etc/apache2/ports.conf # buildkit
# Tue, 24 Feb 2026 19:56:07 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 24 Feb 2026 19:56:07 GMT
EXPOSE map[8443/tcp:{}]
# Tue, 24 Feb 2026 19:56:07 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Tue, 24 Feb 2026 19:56:07 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:f4e0b944ee1e7e50bdfbfa77bda370b6eccee7d698a7adca78c38f5ca0767ca5`  
		Last Modified: Tue, 24 Feb 2026 18:43:18 GMT  
		Size: 31.3 MB (31293918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c1cf78af71ee5fac784620feff9b89b3fc3d9634da6592d1194fc2b920ff2e5`  
		Last Modified: Tue, 24 Feb 2026 19:03:50 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e5db48ef5c27470fb3bdcb3b93e3dcb08709a0faac516f4e026ebdc0d14e48`  
		Last Modified: Tue, 24 Feb 2026 19:03:54 GMT  
		Size: 116.1 MB (116145246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6de807c0c3b4d8d9ac2f58103d526bebef9eb0bb86237877fbed903c435a9f50`  
		Last Modified: Tue, 24 Feb 2026 19:03:50 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff3d72268b0e780332b4188a6dd140127e0e5d9fc4dcf6c8c4d94ec0aba1e66`  
		Last Modified: Tue, 24 Feb 2026 19:03:50 GMT  
		Size: 4.5 MB (4458330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f69bb0c1985c6e547f41fca7ee1c2faaa696fb635fc31be5c380c5f25a8d2fb4`  
		Last Modified: Tue, 24 Feb 2026 19:03:51 GMT  
		Size: 431.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0881963f3aab55f73bb174e90d4aedbe5a98f164c4971bd0ef6644731389b5d`  
		Last Modified: Tue, 24 Feb 2026 19:03:51 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f55ff9bd033b11429a6f2b252b02de73a74b3cac2f5fbbb660b1f3f72928dfa`  
		Last Modified: Tue, 24 Feb 2026 19:03:52 GMT  
		Size: 14.5 MB (14498617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17e6d299a10031e8bd35d3c93b22057ff6143dc047cb234d30a3c4bfb974e66b`  
		Last Modified: Tue, 24 Feb 2026 19:03:52 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f1e73a77baad645c7bb2b80247587d7a8408c91c4810f53259012c3c425a2de`  
		Last Modified: Tue, 24 Feb 2026 19:03:53 GMT  
		Size: 15.3 MB (15342258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d7d7732ba3e0411d21e24380756e53b86cf400b6644a705d1648b8a89408dea`  
		Last Modified: Tue, 24 Feb 2026 19:03:53 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8862ca160c9cd503ddcf78d091b4835d2a688f21081269c69e42f71d90d0d242`  
		Last Modified: Tue, 24 Feb 2026 19:03:53 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef2d06baa450d1f842780f2a45a2ed80a7c62672072d24222c728b012e8a9484`  
		Last Modified: Tue, 24 Feb 2026 19:03:54 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:055de95abb3c0601c2bf980505218b69f460154457b3fb9c79c77eb77869fe5b`  
		Last Modified: Tue, 24 Feb 2026 19:56:12 GMT  
		Size: 111.8 KB (111828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14522046fb720749fec5d67fcf2a8a36156fac5b158e5c6a7b0a4ea14759368b`  
		Last Modified: Tue, 24 Feb 2026 19:56:12 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cef3816b388ca1d23a24999b364164ffa55d9a0032f9e5843321ea44528ea6db`  
		Last Modified: Tue, 24 Feb 2026 19:56:12 GMT  
		Size: 346.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a1081789096a12771393ed88d06da39d0e26855d47ad15e9706ae69fa3da355`  
		Last Modified: Tue, 24 Feb 2026 19:56:12 GMT  
		Size: 6.0 MB (6048926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a3022a6f26a940509f6de88b5158b2a9e35f171bc78fa5f675e98dcaeb4b79d`  
		Last Modified: Tue, 24 Feb 2026 19:56:13 GMT  
		Size: 2.1 KB (2093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e26997a706a163d17c2597780aa73c0283e8c5e4e898d855f8e8b1f656248a45`  
		Last Modified: Tue, 24 Feb 2026 19:56:13 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a51c790f70ffbae7e8333c83c531448e412411c2b12e13c86f39bf5e67b5fcc`  
		Last Modified: Tue, 24 Feb 2026 19:56:13 GMT  
		Size: 501.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e77d3f60ec759531919daefec905b9d58f8444572541f9e45420b15862c743e`  
		Last Modified: Tue, 24 Feb 2026 19:56:14 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7be6e55b38b5462a1cca424a4457c0e5259cdd1fee4abfc2861c48af471bc3d`  
		Last Modified: Tue, 24 Feb 2026 19:56:14 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:apache` - unknown; unknown

```console
$ docker pull yourls@sha256:24f01e3e75d5a848a65a568cf5930e797ba7a3e31db16fad570bd816f2bd52ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.5 KB (47531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27d736896f9bc607f3becc36d80e1d9070c667d6303ff42d0db69264e6dcab55`

```dockerfile
```

-	Layers:
	-	`sha256:dc46c0209fbea004341735076746b72a874e478c6768f3bf2758844069216453`  
		Last Modified: Tue, 24 Feb 2026 19:56:12 GMT  
		Size: 47.5 KB (47531 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:apache` - linux; ppc64le

```console
$ docker pull yourls@sha256:0449bf961ca8be05590fbd7e5e166fd7343ff57382f72662c52987b3bcc2a3ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.8 MB (183755502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebf9bc7827ad660ae2f9387495ca86e1b50be2e289a1f4b81efee2a0ee50dc86`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:46:48 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 03 Feb 2026 02:47:45 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 03 Feb 2026 02:47:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 02:47:45 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 03 Feb 2026 02:47:45 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 03 Feb 2026 02:47:45 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 03 Feb 2026 02:47:45 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 03 Feb 2026 02:48:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 03 Feb 2026 02:48:43 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 03 Feb 2026 02:48:44 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 03 Feb 2026 02:48:44 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 03 Feb 2026 02:48:44 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 03 Feb 2026 02:48:44 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 03 Feb 2026 02:48:44 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Tue, 03 Feb 2026 02:48:44 GMT
ENV PHP_VERSION=8.5.3
# Tue, 03 Feb 2026 02:48:44 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.3.tar.xz.asc
# Tue, 03 Feb 2026 02:48:44 GMT
ENV PHP_SHA256=ce65725b8af07356b69a6046d21487040b11f2acfde786de38b2bfb712c36eb9
# Fri, 13 Feb 2026 18:52:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 13 Feb 2026 18:52:26 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 13 Feb 2026 18:58:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 13 Feb 2026 18:58:25 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 13 Feb 2026 18:58:26 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 13 Feb 2026 18:58:26 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 13 Feb 2026 18:58:26 GMT
STOPSIGNAL SIGWINCH
# Fri, 13 Feb 2026 18:58:27 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 13 Feb 2026 18:58:27 GMT
WORKDIR /var/www/html
# Fri, 13 Feb 2026 18:58:27 GMT
EXPOSE map[80/tcp:{}]
# Fri, 13 Feb 2026 18:58:27 GMT
CMD ["apache2-foreground"]
# Fri, 13 Feb 2026 20:34:02 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)"     bcmath     pdo_mysql     mysqli # buildkit
# Fri, 13 Feb 2026 20:34:02 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Fri, 13 Feb 2026 20:34:03 GMT
RUN a2enmod rewrite expires # buildkit
# Fri, 13 Feb 2026 20:34:05 GMT
ARG YOURLS_VERSION=1.10.3
# Fri, 13 Feb 2026 20:34:05 GMT
ARG YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
# Fri, 13 Feb 2026 20:34:05 GMT
ENV YOURLS_VERSION=1.10.3
# Fri, 13 Feb 2026 20:34:05 GMT
ENV YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
# Fri, 13 Feb 2026 20:34:05 GMT
# ARGS: YOURLS_VERSION=1.10.3 YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Fri, 13 Feb 2026 20:34:05 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Fri, 13 Feb 2026 20:34:05 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Feb 2026 20:34:06 GMT
COPY files/vhost.conf /etc/apache2/sites-available/000-default.conf # buildkit
# Fri, 13 Feb 2026 20:34:06 GMT
COPY files/vhost-https.conf /etc/apache2/sites-available/default-ssl.conf # buildkit
# Fri, 13 Feb 2026 20:34:06 GMT
COPY files/ports.conf /etc/apache2/ports.conf # buildkit
# Fri, 13 Feb 2026 20:34:06 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 13 Feb 2026 20:34:06 GMT
EXPOSE map[8443/tcp:{}]
# Fri, 13 Feb 2026 20:34:06 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Fri, 13 Feb 2026 20:34:06 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:1aee42d34fb7e3a2db6f83f2a84e17846ac990ed8ecf693a309ae759efdbdaa3`  
		Last Modified: Tue, 03 Feb 2026 01:16:35 GMT  
		Size: 33.6 MB (33600184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a5aef540a1dbd10111c40eb7d9fc2480005c3fd8d164979371878603dac2854`  
		Last Modified: Tue, 03 Feb 2026 02:53:14 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:282dc5cdeff5e017f78b0496f224050268f625b87ef7cefd7cdd16e6abf1d723`  
		Last Modified: Tue, 03 Feb 2026 02:53:17 GMT  
		Size: 109.6 MB (109597358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09f41d4ecbf32a9e015fc638210e66283419cedac7dd29494bd26c767c870b92`  
		Last Modified: Tue, 03 Feb 2026 02:53:13 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef7b9ee345db4a78acffafdd3238a5dca1e196b0a4b0820239c3b77306dfc411`  
		Last Modified: Tue, 03 Feb 2026 02:54:27 GMT  
		Size: 4.9 MB (4881260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1214b31dd46127f293476e70fcf6aebc429b886d623edf3762ae804c6607a6c5`  
		Last Modified: Tue, 03 Feb 2026 02:54:27 GMT  
		Size: 435.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a1e19e97031950f9a8cb1af296b4ff35ee053b50f2f569235ee2442575edd8`  
		Last Modified: Tue, 03 Feb 2026 02:54:27 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbc574d3b8ba422c4d5f96b41738d0e06931790cfb9bd195dfa6db0663a47b88`  
		Last Modified: Fri, 13 Feb 2026 18:58:58 GMT  
		Size: 14.5 MB (14514461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:344fe9bbecbda240ba480c8a42053c671ddf1e0682432933aa1abfb620959ca0`  
		Last Modified: Fri, 13 Feb 2026 18:58:20 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e59d1601451b89978be52a445035cb0a54adf429c794cbf69004f364884fce47`  
		Last Modified: Fri, 13 Feb 2026 18:58:58 GMT  
		Size: 15.0 MB (14984656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa482acd178d2f9e5576faa5a27c544ea9ed0e8862c62dd869d41b359422b0d2`  
		Last Modified: Fri, 13 Feb 2026 18:58:57 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:686e9c0037ff1f57e1a847ab36648eb318b266b0f5177abf6cd25115e5beaa73`  
		Last Modified: Fri, 13 Feb 2026 18:58:57 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19a0e5208af9c82d162891798b50196b53dcb7570c3a81a8f56797a08430fda8`  
		Last Modified: Fri, 13 Feb 2026 18:58:58 GMT  
		Size: 895.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e00771525320bb238613b2c175543d993d9486bf7d6c64e9a6a60a12bcbc1cd4`  
		Last Modified: Fri, 13 Feb 2026 20:34:18 GMT  
		Size: 117.3 KB (117322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd9d622694b7b0178bc397fd4b77c3234015a095d31aa156b55d6727ed3f3eb`  
		Last Modified: Fri, 13 Feb 2026 20:34:18 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06ab24b7f470bef9dd33d1404438eddfb749a86fbacda61bc97462aa2ffe221f`  
		Last Modified: Fri, 13 Feb 2026 20:34:18 GMT  
		Size: 351.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:332455bdca4ba3b398b9a9f2a830186fcceef4a7c8882166b11a5566d6ff595a`  
		Last Modified: Fri, 13 Feb 2026 20:34:18 GMT  
		Size: 6.0 MB (6048925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f316f19fbe9bb33c7fbe1d5cf40a168cf4d7c1a689a7db2cfbf9291ead69744`  
		Last Modified: Fri, 13 Feb 2026 20:34:19 GMT  
		Size: 2.1 KB (2092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb5ad88823f6ac4db6c86c6d4293f40a2db6f5520cc9243968680d50dbbb9356`  
		Last Modified: Fri, 13 Feb 2026 20:34:19 GMT  
		Size: 1.7 KB (1695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61c9c04745b3f1f30c3e176c73f797abee4a2ad0efcdf916ea3e7153efdeddd3`  
		Last Modified: Fri, 13 Feb 2026 20:34:19 GMT  
		Size: 500.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dfc9f3e79393434594ef6e69b7aa3cc6fd9eb41a54fbe6836eb2a4752d916a2`  
		Last Modified: Fri, 13 Feb 2026 20:34:20 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afb054cf7d3c59d92d55553bcc94677d2b2160b2a3488fe18aa34f429114e6f3`  
		Last Modified: Fri, 13 Feb 2026 20:34:20 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:apache` - unknown; unknown

```console
$ docker pull yourls@sha256:25fca6b05aba99ec7c5b6e3e0f3bed96bf4a64664a8089952b783d642a448bab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 KB (47663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71ad87cb9956d3ea3eea44e65939fb3823e7ad7bfbd2bfd7171228540d730908`

```dockerfile
```

-	Layers:
	-	`sha256:ff1946fa847e298660f42fcc2ace6bc1b18b2749e0b618e27add9bac5a708f42`  
		Last Modified: Fri, 13 Feb 2026 20:34:17 GMT  
		Size: 47.7 KB (47663 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:apache` - linux; riscv64

```console
$ docker pull yourls@sha256:093fdf26ae1f7957d0856a4e3d785c042ea64dd735c14d50fcc19222ee0bd5ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.5 MB (213494828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c64837c95100cff96a56775dc952f3e5c63c6f07602b1a17a85149468388c5dc`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 17:08:39 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 03 Feb 2026 17:10:41 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 03 Feb 2026 17:10:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 17:10:41 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 03 Feb 2026 17:10:42 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 03 Feb 2026 17:10:42 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 03 Feb 2026 17:10:42 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 03 Feb 2026 18:15:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 03 Feb 2026 18:15:47 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 03 Feb 2026 18:15:48 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 03 Feb 2026 18:15:48 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 03 Feb 2026 18:15:48 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 03 Feb 2026 18:15:48 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 03 Feb 2026 18:15:48 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Tue, 03 Feb 2026 18:15:48 GMT
ENV PHP_VERSION=8.5.3
# Tue, 03 Feb 2026 18:15:48 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.3.tar.xz.asc
# Tue, 03 Feb 2026 18:15:48 GMT
ENV PHP_SHA256=ce65725b8af07356b69a6046d21487040b11f2acfde786de38b2bfb712c36eb9
# Fri, 13 Feb 2026 19:08:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 13 Feb 2026 19:08:01 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 13 Feb 2026 20:04:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 13 Feb 2026 20:04:47 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 13 Feb 2026 20:04:47 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 13 Feb 2026 20:04:47 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 13 Feb 2026 20:04:47 GMT
STOPSIGNAL SIGWINCH
# Fri, 13 Feb 2026 20:04:48 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 13 Feb 2026 20:04:48 GMT
WORKDIR /var/www/html
# Fri, 13 Feb 2026 20:04:48 GMT
EXPOSE map[80/tcp:{}]
# Fri, 13 Feb 2026 20:04:48 GMT
CMD ["apache2-foreground"]
# Sat, 14 Feb 2026 19:09:44 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)"     bcmath     pdo_mysql     mysqli # buildkit
# Sat, 14 Feb 2026 19:09:44 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Sat, 14 Feb 2026 19:09:45 GMT
RUN a2enmod rewrite expires # buildkit
# Sat, 14 Feb 2026 19:09:49 GMT
ARG YOURLS_VERSION=1.10.3
# Sat, 14 Feb 2026 19:09:49 GMT
ARG YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
# Sat, 14 Feb 2026 19:09:49 GMT
ENV YOURLS_VERSION=1.10.3
# Sat, 14 Feb 2026 19:09:49 GMT
ENV YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
# Sat, 14 Feb 2026 19:09:49 GMT
# ARGS: YOURLS_VERSION=1.10.3 YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Sat, 14 Feb 2026 19:09:49 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Sat, 14 Feb 2026 19:09:49 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 14 Feb 2026 19:09:49 GMT
COPY files/vhost.conf /etc/apache2/sites-available/000-default.conf # buildkit
# Sat, 14 Feb 2026 19:09:50 GMT
COPY files/vhost-https.conf /etc/apache2/sites-available/default-ssl.conf # buildkit
# Sat, 14 Feb 2026 19:09:50 GMT
COPY files/ports.conf /etc/apache2/ports.conf # buildkit
# Sat, 14 Feb 2026 19:09:50 GMT
EXPOSE map[8080/tcp:{}]
# Sat, 14 Feb 2026 19:09:50 GMT
EXPOSE map[8443/tcp:{}]
# Sat, 14 Feb 2026 19:09:50 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Sat, 14 Feb 2026 19:09:50 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:4526db52defd9278f79daec64ebfa633041460dbe0cfad19564ae34d84b13b4c`  
		Last Modified: Tue, 03 Feb 2026 07:14:46 GMT  
		Size: 28.3 MB (28276389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c6a0c7bf9985f7aa3278051e22de8b2e25e48b9247e1f8ee94b0580a41f8dbf`  
		Last Modified: Tue, 03 Feb 2026 18:13:33 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c308411999737082a164f0c80e801b9bba1f870be1efa26fb715f1dd002ad6b0`  
		Last Modified: Tue, 03 Feb 2026 18:14:01 GMT  
		Size: 146.6 MB (146578579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fa8ed6ff919b7995bbffcb5df8a9d82dfddafe0ad63dc244974287839a83ee2`  
		Last Modified: Tue, 03 Feb 2026 18:13:33 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2c39a123fee7384a8e42dd0131ab0dec5b9cbf76fa8ed14a529fbebc60ac424`  
		Last Modified: Tue, 03 Feb 2026 19:16:24 GMT  
		Size: 4.0 MB (4031154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4c78bb3209b3345dbe74ef17fe714509c869fb02bc4a3474afe127ff1263cb7`  
		Last Modified: Tue, 03 Feb 2026 19:16:22 GMT  
		Size: 435.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad8722119dcebc8afef8a1229503e5323ae32e648b97a65ea37d1bb92e48eee`  
		Last Modified: Tue, 03 Feb 2026 19:16:22 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7cc8252a1cf4c391cf93ab67c8e431bd9d79ff17a96bb6ced189d81d614d390`  
		Last Modified: Fri, 13 Feb 2026 20:08:02 GMT  
		Size: 14.5 MB (14514413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b66ada2524556038faf30c8a0471d30898e12ab3807bad5e4cd04156c6069f22`  
		Last Modified: Fri, 13 Feb 2026 20:07:58 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7df3b66ba9bcda7ede006592fcdcb3fd319cb34b6f5a35654e417c0806c29e51`  
		Last Modified: Fri, 13 Feb 2026 20:08:03 GMT  
		Size: 13.9 MB (13927433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd80899af7730f880612f365e645027a2615cace1f1ed4c194198d19eac5e2f6`  
		Last Modified: Fri, 13 Feb 2026 20:07:58 GMT  
		Size: 2.5 KB (2465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21962b00b28715762f9d0a6d7846ca3db2db11df512c9ace7857af39560c8911`  
		Last Modified: Fri, 13 Feb 2026 20:08:00 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560d346c227ecca3acf5499e9552bd8d2483197b687cd849380571937495ee57`  
		Last Modified: Fri, 13 Feb 2026 20:08:00 GMT  
		Size: 897.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c5406eb5df6f1556ddec8bcedcf6558657d3b99dfd3ff6b70d0ce600d3ee241`  
		Last Modified: Sat, 14 Feb 2026 19:10:39 GMT  
		Size: 106.6 KB (106580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af2ec04dea83794991b9c5bac291052c0d057395ad6caff072f20782cc8f7723`  
		Last Modified: Sat, 14 Feb 2026 19:10:39 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c67ce442cde272dcc616779c6bab5983536a54efc28673d317a35c90cdce169f`  
		Last Modified: Sat, 14 Feb 2026 19:10:39 GMT  
		Size: 351.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:963c216886305fb4d6342499662e91b7d37d249e979461af96a3504a741beaae`  
		Last Modified: Sat, 14 Feb 2026 19:10:40 GMT  
		Size: 6.0 MB (6048922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ad3d0d6fbfe3235ab8216ff54dbcf218d59af7830e1a9f42810e343e7c12c90`  
		Last Modified: Sat, 14 Feb 2026 19:10:41 GMT  
		Size: 2.1 KB (2096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecda93e7b914668967399a456e4406739301c1d54bd04643c54139bbfafbdea9`  
		Last Modified: Sat, 14 Feb 2026 19:10:41 GMT  
		Size: 1.7 KB (1695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b19db75eab5e45d6ff6dbf97ee02a44141d4108c42058957aaaa269b7ee27d1`  
		Last Modified: Sat, 14 Feb 2026 19:10:41 GMT  
		Size: 502.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62fff09a7e99bdd5e8fda213516c1ccc6d89f477e5869f55dcf3131cec6fa9a5`  
		Last Modified: Sat, 14 Feb 2026 19:10:42 GMT  
		Size: 548.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:162990e65e665444ec74cc9000d6e4333f365bebbbc499a651e07f016626b66c`  
		Last Modified: Sat, 14 Feb 2026 19:10:42 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:apache` - unknown; unknown

```console
$ docker pull yourls@sha256:6871ba669be560e37bc90aa9020039dd7b5e337509ab219c6d1437ae88432b50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 KB (47663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20a60aa4d56ddcae5ec96e35149a6bdd06a5704f3058bfd80ac4fb34c1d1d891`

```dockerfile
```

-	Layers:
	-	`sha256:35095d5bae1bdff2f18840d9b6c655fbe7b507a4c93140792b5659219aeada2d`  
		Last Modified: Sat, 14 Feb 2026 19:10:39 GMT  
		Size: 47.7 KB (47663 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:apache` - linux; s390x

```console
$ docker pull yourls@sha256:a1000e20c9e1ee0c38296501cb2ce53d17540772c00c6d009b97d682bdf02469
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.7 MB (161693665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:711ac01f01d42664618891ba25781f2eb4e196d544cf2d6fab9a9c944c14c266`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:06:30 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 24 Feb 2026 19:07:01 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 24 Feb 2026 19:07:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 19:07:01 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 24 Feb 2026 19:07:01 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 24 Feb 2026 19:07:01 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 24 Feb 2026 19:07:01 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 24 Feb 2026 19:07:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 24 Feb 2026 19:07:28 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 24 Feb 2026 19:07:30 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 24 Feb 2026 19:07:30 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 24 Feb 2026 19:07:30 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 24 Feb 2026 19:07:30 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 24 Feb 2026 19:07:30 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Tue, 24 Feb 2026 19:07:30 GMT
ENV PHP_VERSION=8.5.3
# Tue, 24 Feb 2026 19:07:30 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.3.tar.xz.asc
# Tue, 24 Feb 2026 19:07:30 GMT
ENV PHP_SHA256=ce65725b8af07356b69a6046d21487040b11f2acfde786de38b2bfb712c36eb9
# Tue, 24 Feb 2026 19:07:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 24 Feb 2026 19:07:54 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:13:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 24 Feb 2026 19:13:16 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:13:16 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 24 Feb 2026 19:13:16 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 24 Feb 2026 19:13:16 GMT
STOPSIGNAL SIGWINCH
# Tue, 24 Feb 2026 19:13:17 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:13:17 GMT
WORKDIR /var/www/html
# Tue, 24 Feb 2026 19:13:17 GMT
EXPOSE map[80/tcp:{}]
# Tue, 24 Feb 2026 19:13:17 GMT
CMD ["apache2-foreground"]
# Tue, 24 Feb 2026 23:50:59 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)"     bcmath     pdo_mysql     mysqli # buildkit
# Tue, 24 Feb 2026 23:50:59 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Tue, 24 Feb 2026 23:51:00 GMT
RUN a2enmod rewrite expires # buildkit
# Tue, 24 Feb 2026 23:51:02 GMT
ARG YOURLS_VERSION=1.10.3
# Tue, 24 Feb 2026 23:51:02 GMT
ARG YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
# Tue, 24 Feb 2026 23:51:02 GMT
ENV YOURLS_VERSION=1.10.3
# Tue, 24 Feb 2026 23:51:02 GMT
ENV YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
# Tue, 24 Feb 2026 23:51:02 GMT
# ARGS: YOURLS_VERSION=1.10.3 YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Tue, 24 Feb 2026 23:51:02 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Tue, 24 Feb 2026 23:51:02 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 23:51:03 GMT
COPY files/vhost.conf /etc/apache2/sites-available/000-default.conf # buildkit
# Tue, 24 Feb 2026 23:51:04 GMT
COPY files/vhost-https.conf /etc/apache2/sites-available/default-ssl.conf # buildkit
# Tue, 24 Feb 2026 23:51:05 GMT
COPY files/ports.conf /etc/apache2/ports.conf # buildkit
# Tue, 24 Feb 2026 23:51:05 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 24 Feb 2026 23:51:05 GMT
EXPOSE map[8443/tcp:{}]
# Tue, 24 Feb 2026 23:51:05 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Tue, 24 Feb 2026 23:51:05 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:b50f587e37cdad2c774c5137974987f2b5aca2ef491f293c135b60e1e43e0135`  
		Last Modified: Tue, 24 Feb 2026 18:43:50 GMT  
		Size: 29.8 MB (29838179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0fc84c4a640d0b8ba79b6cd68d2c4564c6077f19800ec5d8e027917022c6e9`  
		Last Modified: Tue, 24 Feb 2026 19:13:59 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7bc00985220e41136d718ea042c32549e1b97604874bde9947bbe41e1fc71b2`  
		Last Modified: Tue, 24 Feb 2026 19:14:02 GMT  
		Size: 92.6 MB (92571895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21873b6f711bdf207d7654c3ec75511328308e8b036073024b5287af128cd28e`  
		Last Modified: Tue, 24 Feb 2026 19:13:59 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd313c15857832abdcab0e6d4f3cd1e48ab7577d5cb417b5a8433b5f466c7b9f`  
		Last Modified: Tue, 24 Feb 2026 19:14:00 GMT  
		Size: 4.3 MB (4329173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3e59e20b28e86a33fbd99a153863d54bff4c01c3f1513683678440aa3be64f8`  
		Last Modified: Tue, 24 Feb 2026 19:14:00 GMT  
		Size: 432.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e4d013d041017a468d68a9f771421b030d25099afd435a9531239728156799`  
		Last Modified: Tue, 24 Feb 2026 19:14:00 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5a2a3316eb22efcb29fb334c3b798faad23407ca5b0780f76942d739f4152e6`  
		Last Modified: Tue, 24 Feb 2026 19:14:01 GMT  
		Size: 14.5 MB (14498209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76f4d3a821e89126ca8a3bdf0cd2e31828182a2ed474b8084950ca1fa46cd9ec`  
		Last Modified: Tue, 24 Feb 2026 19:14:01 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6708beca08aa067fea7b95de76882be6fa392900fbb9556937394c67905bcbb1`  
		Last Modified: Tue, 24 Feb 2026 19:14:02 GMT  
		Size: 14.3 MB (14284252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee8e4d4858b2600926751b107993e2f70f261a2c822adcfb457bf778ad7d094a`  
		Last Modified: Tue, 24 Feb 2026 19:14:02 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:537afe823cdf7f350c05ea9a5d22337b36237dafb25ba10cf597c903b784b1e4`  
		Last Modified: Tue, 24 Feb 2026 19:14:02 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44620d8593daa5b1a8ea3101cd836ff845c82f113e7e265a6253ea12f8142eea`  
		Last Modified: Tue, 24 Feb 2026 19:14:03 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36e9b109ac386ffcef5e8c1208fd86e230c366912f33c44b2caa51e8e34b6d3e`  
		Last Modified: Tue, 24 Feb 2026 23:51:14 GMT  
		Size: 111.7 KB (111693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3c98d815fb97828cd37bfc7df8e97561caab5bac75a02603581f02d32a51820`  
		Last Modified: Tue, 24 Feb 2026 23:51:14 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8cd19971333fdc5c654731bc439f0039ca38b073ed18a3b37504ac0bfd90477`  
		Last Modified: Tue, 24 Feb 2026 23:51:14 GMT  
		Size: 351.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df1cb05f66b923fdbdceb8c09f81f53beb66d49bd209059c087f196675417675`  
		Last Modified: Tue, 24 Feb 2026 23:51:14 GMT  
		Size: 6.0 MB (6048926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb6f640e9bdd32e79c97b8db37800522aa19a50a2ffd26cd7aec43a4a4c93a60`  
		Last Modified: Tue, 24 Feb 2026 23:51:15 GMT  
		Size: 2.1 KB (2098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:477f8e5413c95594443442652e3b3d172cd4c881385bff7110428ca5f8350369`  
		Last Modified: Tue, 24 Feb 2026 23:51:15 GMT  
		Size: 1.7 KB (1694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2c9ab0b700fabd86120e7d423a927e831dd99574fb6aeea6bd6031baac55bca`  
		Last Modified: Tue, 24 Feb 2026 23:51:15 GMT  
		Size: 502.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3de16c56f13aa4c10fe169a69dc481c8a0267c99e6b439092165a452b1ee7a8`  
		Last Modified: Tue, 24 Feb 2026 23:51:15 GMT  
		Size: 549.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30d6f0738082ed3efe258f6b3bd8f8693bd7a91a5f62cdbf9f97e97b20ba1627`  
		Last Modified: Tue, 24 Feb 2026 23:51:16 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:apache` - unknown; unknown

```console
$ docker pull yourls@sha256:f9b39ddc56ca7d7a664760ca5eea477138ac1dfd145be3caf3977bb65b92a53f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.6 KB (47579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af4104646e5a13ccad9dbe273de30e796ee049c564b24f0485dee663ba05f7e6`

```dockerfile
```

-	Layers:
	-	`sha256:7317935718795be359ffe1d5bc476443777d378f9190741dd791200c4dc069b3`  
		Last Modified: Tue, 24 Feb 2026 23:51:14 GMT  
		Size: 47.6 KB (47579 bytes)  
		MIME: application/vnd.in-toto+json
