## `postfixadmin:latest`

```console
$ docker pull postfixadmin@sha256:cf56feb07a12f04e0c3ffcbb51a411ed505319d44082359f9d824268e5b40030
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

### `postfixadmin:latest` - linux; amd64

```console
$ docker pull postfixadmin@sha256:6f4cc50648e4b43dd33f75c436990e03647323e718c11032b407a8dbe689f799
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.0 MB (181046284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c7901d3ac8de0a1b7bdd0476f96b90ac884febb51388d47e34ae4714c4e08f6`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 11 Sep 2025 11:18:55 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1759104000'
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 11 Sep 2025 11:18:55 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 11 Sep 2025 11:18:55 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_VERSION=8.3.26
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.26.tar.xz.asc
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_SHA256=2f522eefa02c400c94610d07f25c4fd4c771f95e4a1f55102332ccb40663cbd2
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 11 Sep 2025 11:18:55 GMT
STOPSIGNAL SIGWINCH
# Thu, 11 Sep 2025 11:18:55 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
WORKDIR /var/www/html
# Thu, 11 Sep 2025 11:18:55 GMT
EXPOSE map[80/tcp:{}]
# Thu, 11 Sep 2025 11:18:55 GMT
CMD ["apache2-foreground"]
# Thu, 11 Sep 2025 11:18:55 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		gosu 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 	libc-client2007e-dev 	libkrb5-dev 	libpq-dev 	libsqlite3-dev 	; 		docker-php-ext-configure 		imap --with-imap-ssl --with-kerberos 	; 		docker-php-ext-install -j "$(nproc)" 		imap 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 		ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 			apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
ARG POSTFIXADMIN_VERSION=3.3.16
# Thu, 11 Sep 2025 11:18:55 GMT
ARG POSTFIXADMIN_SHA512=d1b8074c32f7912c187c2c37c5cca158432cb85fc415d9efe86cf11f70ab035117053cc579306e224cb180e70fa3c84a68335f18d62b43abf591e8105a00847d
# Thu, 11 Sep 2025 11:18:55 GMT
ENV POSTFIXADMIN_VERSION=3.3.16
# Thu, 11 Sep 2025 11:18:55 GMT
ENV POSTFIXADMIN_SHA512=d1b8074c32f7912c187c2c37c5cca158432cb85fc415d9efe86cf11f70ab035117053cc579306e224cb180e70fa3c84a68335f18d62b43abf591e8105a00847d
# Thu, 11 Sep 2025 11:18:55 GMT
ENV APACHE_DOCUMENT_ROOT=/var/www/html/public
# Thu, 11 Sep 2025 11:18:55 GMT
# ARGS: POSTFIXADMIN_VERSION=3.3.16 POSTFIXADMIN_SHA512=d1b8074c32f7912c187c2c37c5cca158432cb85fc415d9efe86cf11f70ab035117053cc579306e224cb180e70fa3c84a68335f18d62b43abf591e8105a00847d
RUN set -eu; sed -ri -e 's!/var/www/html!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/sites-available/*.conf; 	sed -ri -e 's!/var/www/!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/apache2.conf /etc/apache2/conf-available/*.conf # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
# ARGS: POSTFIXADMIN_VERSION=3.3.16 POSTFIXADMIN_SHA512=d1b8074c32f7912c187c2c37c5cca158432cb85fc415d9efe86cf11f70ab035117053cc579306e224cb180e70fa3c84a68335f18d62b43abf591e8105a00847d
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/postfixadmin-${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Thu, 11 Sep 2025 11:18:55 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:5c32499ab806884c5725c705c2bf528662d034ed99de13d3205309e0d9ef0375`  
		Last Modified: Mon, 29 Sep 2025 23:34:35 GMT  
		Size: 28.2 MB (28228336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5915ef80fee0d0d5db9590ef91156e390264f4455b19d808d105018914b81747`  
		Last Modified: Tue, 30 Sep 2025 00:00:08 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdd8c66d38462623f2f724948a16e15533521c59e9f5c6c34fa635bda54b37ab`  
		Last Modified: Tue, 30 Sep 2025 00:00:20 GMT  
		Size: 104.3 MB (104330298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e6947b8ca18edcce12dc828bc024036208e43eddbd669f6efd61d20780b1ded`  
		Last Modified: Tue, 30 Sep 2025 00:00:09 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:812403c03ecb63bbe7c9d4bd3cdc45fabf310499d1c191a28ec8c7595c57e3ab`  
		Last Modified: Tue, 30 Sep 2025 00:03:10 GMT  
		Size: 20.1 MB (20131826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e890343ac46f33328aa4efa9a4c57abb8bab8dda411717b4f2dbdbfa056bd9`  
		Last Modified: Tue, 30 Sep 2025 00:03:08 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e6c1f5c0560eeb3b6a52f3baf838d620471c8993c131ba68dffb5a54167595e`  
		Last Modified: Tue, 30 Sep 2025 00:03:08 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2c116c2a9d1d1906bc79d4e672c3eb88a15361c129f84f71334546407882ca9`  
		Last Modified: Tue, 30 Sep 2025 00:03:10 GMT  
		Size: 12.7 MB (12709609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdcee8f13d30bb00b2d29682b7f7cea74a7d7b5eae79af327931847d99d60829`  
		Last Modified: Tue, 30 Sep 2025 00:03:08 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cec48dfbf643c5c0782eb467ac244e0608341bc9457167435938c8ed2fb0b10b`  
		Last Modified: Tue, 30 Sep 2025 00:03:09 GMT  
		Size: 11.7 MB (11669265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:302df95cd27aa4d9b3e85ea51ae86468e163ca99371399664b438494c808a4fe`  
		Last Modified: Tue, 30 Sep 2025 00:03:08 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d10feb002e707c8b78d362bd5e4c328ba297dc2fa7e3ba2ef9859ca2862b87a`  
		Last Modified: Tue, 30 Sep 2025 00:03:08 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7721f4d73208e35daeaae358288dd9251a3ac3bb1af371aabc13ec3b4ab6d19`  
		Last Modified: Tue, 30 Sep 2025 00:03:08 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a98c7423946b2f3f0c5281e11cc60f5a3f779b94f7649c8443db4d8ab9e7518c`  
		Last Modified: Tue, 30 Sep 2025 00:03:08 GMT  
		Size: 888.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eddd38aa388ee76c32455f2e43b6634ae1ba755c64bda2aee8458ed39c4795b`  
		Last Modified: Tue, 30 Sep 2025 03:13:03 GMT  
		Size: 1.1 MB (1092778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bebb26ed812bd131f17062cc244764842e7dae81e3742f0715d56f2554ee4e3`  
		Last Modified: Tue, 30 Sep 2025 03:13:03 GMT  
		Size: 997.2 KB (997186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fad1a4e4166aa684f9aa130a53f43d665da33c21edefe1e5ce8e53143b72cef`  
		Last Modified: Tue, 30 Sep 2025 03:13:03 GMT  
		Size: 8.0 KB (8047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c713af6d2184c9d19d271c0e4b5570dfa2539555cb53bca62bfa2b45da8ee68`  
		Last Modified: Tue, 30 Sep 2025 03:13:04 GMT  
		Size: 1.9 MB (1871570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5a95f8da3a10201ac2d5592e3d91071c7fcabdb22d4ffbf781bd5a8da2b551d`  
		Last Modified: Tue, 30 Sep 2025 03:13:03 GMT  
		Size: 1.7 KB (1652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:latest` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:960781d70afd6e4c47a937327e5432476226f903379b33f84da888deb4c4bed5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 KB (36449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3ce1c7f63c579449446068df11e809bc85edaa9abf3be4cb510c68b04d4679c`

```dockerfile
```

-	Layers:
	-	`sha256:fac318a2e9aa29f1d71151c2a3a395651f2e60d5df227186864537961be26ff5`  
		Last Modified: Wed, 01 Oct 2025 14:14:18 GMT  
		Size: 36.4 KB (36449 bytes)  
		MIME: application/vnd.in-toto+json

### `postfixadmin:latest` - linux; arm variant v5

```console
$ docker pull postfixadmin@sha256:111caa34afc2ac43add7aad176809a3a9dc58ff18391d51e2520f55870ae4454
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.4 MB (154385664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:418ae1ad84eeca0d56b75da8aac55b02bb66642234e39208d9153196546e2b29`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 11 Sep 2025 11:18:55 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1760918400'
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 11 Sep 2025 11:18:55 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 11 Sep 2025 11:18:55 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_VERSION=8.3.26
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.26.tar.xz.asc
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_SHA256=2f522eefa02c400c94610d07f25c4fd4c771f95e4a1f55102332ccb40663cbd2
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 11 Sep 2025 11:18:55 GMT
STOPSIGNAL SIGWINCH
# Thu, 11 Sep 2025 11:18:55 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
WORKDIR /var/www/html
# Thu, 11 Sep 2025 11:18:55 GMT
EXPOSE map[80/tcp:{}]
# Thu, 11 Sep 2025 11:18:55 GMT
CMD ["apache2-foreground"]
# Thu, 11 Sep 2025 11:18:55 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		gosu 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 	libc-client2007e-dev 	libkrb5-dev 	libpq-dev 	libsqlite3-dev 	; 		docker-php-ext-configure 		imap --with-imap-ssl --with-kerberos 	; 		docker-php-ext-install -j "$(nproc)" 		imap 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 		ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 			apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
ARG POSTFIXADMIN_VERSION=3.3.16
# Thu, 11 Sep 2025 11:18:55 GMT
ARG POSTFIXADMIN_SHA512=d1b8074c32f7912c187c2c37c5cca158432cb85fc415d9efe86cf11f70ab035117053cc579306e224cb180e70fa3c84a68335f18d62b43abf591e8105a00847d
# Thu, 11 Sep 2025 11:18:55 GMT
ENV POSTFIXADMIN_VERSION=3.3.16
# Thu, 11 Sep 2025 11:18:55 GMT
ENV POSTFIXADMIN_SHA512=d1b8074c32f7912c187c2c37c5cca158432cb85fc415d9efe86cf11f70ab035117053cc579306e224cb180e70fa3c84a68335f18d62b43abf591e8105a00847d
# Thu, 11 Sep 2025 11:18:55 GMT
ENV APACHE_DOCUMENT_ROOT=/var/www/html/public
# Thu, 11 Sep 2025 11:18:55 GMT
# ARGS: POSTFIXADMIN_VERSION=3.3.16 POSTFIXADMIN_SHA512=d1b8074c32f7912c187c2c37c5cca158432cb85fc415d9efe86cf11f70ab035117053cc579306e224cb180e70fa3c84a68335f18d62b43abf591e8105a00847d
RUN set -eu; sed -ri -e 's!/var/www/html!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/sites-available/*.conf; 	sed -ri -e 's!/var/www/!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/apache2.conf /etc/apache2/conf-available/*.conf # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
# ARGS: POSTFIXADMIN_VERSION=3.3.16 POSTFIXADMIN_SHA512=d1b8074c32f7912c187c2c37c5cca158432cb85fc415d9efe86cf11f70ab035117053cc579306e224cb180e70fa3c84a68335f18d62b43abf591e8105a00847d
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/postfixadmin-${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Thu, 11 Sep 2025 11:18:55 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:f982c9691d15a93fba0c1226ca85169d870439f0b6119d1ec61ec73d2a7dc8c3`  
		Last Modified: Tue, 21 Oct 2025 00:19:59 GMT  
		Size: 25.8 MB (25757495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:875bf71cd370be96b629a37ec33d504d347096daaad8c9507851625c4e279768`  
		Last Modified: Tue, 21 Oct 2025 01:27:57 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0486f47daf4d640bfc7b799812a7e286af2c8b4192dc06285532a9495c332c8`  
		Last Modified: Tue, 21 Oct 2025 01:28:04 GMT  
		Size: 82.0 MB (81979353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70d5e72954b3eacb6fed09e756f558f55048b975d00d32d8d058870fcb58a4e3`  
		Last Modified: Tue, 21 Oct 2025 01:27:57 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7b360b0709739a4f3482a54c769a58cfc7efa242f110bd318884df15dd08ef2`  
		Last Modified: Tue, 21 Oct 2025 01:38:45 GMT  
		Size: 19.4 MB (19422579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf9520176f26e248e493da27e7954c82621edb8bff7f2819bbdaf9d645a063b0`  
		Last Modified: Tue, 21 Oct 2025 01:38:44 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d72988208ae38a432875986244268ef8995e641dd867951fed52cac12a5ef17`  
		Last Modified: Tue, 21 Oct 2025 01:38:44 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eb773c8550e3c887ae7197812770d32b347a0c89d8052b081c5849f65462e16`  
		Last Modified: Tue, 21 Oct 2025 01:48:40 GMT  
		Size: 12.7 MB (12707639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:644ddaf47e9f7f97218581f319e147347a2a03135b9946ddaca88958898f65f1`  
		Last Modified: Tue, 21 Oct 2025 01:48:39 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a4c75e95de75a72ecfd5b56a8e09b428749e46dd3795f4f83d1a4e4802bf8f3`  
		Last Modified: Tue, 21 Oct 2025 01:48:40 GMT  
		Size: 10.6 MB (10630929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8986fe02e4996971251eba766fae7f966fb0f3ebb071f51d71c2478ee13a5011`  
		Last Modified: Tue, 21 Oct 2025 01:48:39 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e14d82e2cceca1ae5a06eabc8b4739da1a1e1366b2399bfaf260858e4d9e774`  
		Last Modified: Tue, 21 Oct 2025 01:48:39 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8ecf516daf860f09f04e16993e53e7d40179636a2b7ce478fa1ed5416af9c74`  
		Last Modified: Tue, 21 Oct 2025 01:48:40 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e8aee11f026e840a7eef25a54767de7fec053bd20e2cd821071834d75774cad`  
		Last Modified: Tue, 21 Oct 2025 01:48:40 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56c0da631e0a36e56d1936e69d762186363c462bfa55de98d9e68cd81c8c448c`  
		Last Modified: Tue, 21 Oct 2025 03:53:55 GMT  
		Size: 1.1 MB (1065652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a27ec77cc00bc6e9279de49f81c65a6eb060876ae69acd0521b6d6200914e57a`  
		Last Modified: Tue, 21 Oct 2025 03:53:55 GMT  
		Size: 935.0 KB (935010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:185e05e105fd651f94c6f8f9969eb0a54823c59ad15b6a6fefe7b5d5234f7e5d`  
		Last Modified: Tue, 21 Oct 2025 03:53:55 GMT  
		Size: 8.0 KB (8048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c66f2531c1ffe0ebb6af3b1328d9b266b1b71753c64ef7ed914df7750ec2bc5`  
		Last Modified: Tue, 21 Oct 2025 03:53:55 GMT  
		Size: 1.9 MB (1871576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:389bee139882d1fe8d980866b2c61ee6f2f1ac6d954531a14ea8d5612ea749b9`  
		Last Modified: Tue, 21 Oct 2025 03:53:55 GMT  
		Size: 1.7 KB (1653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:latest` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:a86edb4140e31b6dd6651687d0b49421202921fec78e2cee463cd705f3da4702
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.6 KB (36594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a33d37822d689b2352746c0db3df0e53375f76abca5e7a6ef4de49c19189c15`

```dockerfile
```

-	Layers:
	-	`sha256:c40e3dde8c5fb71b49575464dec170978cad492e2f7a4d188152b6774a2d8716`  
		Last Modified: Tue, 21 Oct 2025 08:12:22 GMT  
		Size: 36.6 KB (36594 bytes)  
		MIME: application/vnd.in-toto+json

### `postfixadmin:latest` - linux; arm variant v7

```console
$ docker pull postfixadmin@sha256:3f032240e756d6e403295a0774d7c672b93c2ea77ab0a87d44ad2accbbb5673e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.5 MB (145538693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:221c839097e4ae8abc1ebf1ae7f5482def100c2b247bb28a0fb57f791d7a5000`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 11 Sep 2025 11:18:55 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1760918400'
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 11 Sep 2025 11:18:55 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 11 Sep 2025 11:18:55 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_VERSION=8.3.26
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.26.tar.xz.asc
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_SHA256=2f522eefa02c400c94610d07f25c4fd4c771f95e4a1f55102332ccb40663cbd2
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 11 Sep 2025 11:18:55 GMT
STOPSIGNAL SIGWINCH
# Thu, 11 Sep 2025 11:18:55 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
WORKDIR /var/www/html
# Thu, 11 Sep 2025 11:18:55 GMT
EXPOSE map[80/tcp:{}]
# Thu, 11 Sep 2025 11:18:55 GMT
CMD ["apache2-foreground"]
# Thu, 11 Sep 2025 11:18:55 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		gosu 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 	libc-client2007e-dev 	libkrb5-dev 	libpq-dev 	libsqlite3-dev 	; 		docker-php-ext-configure 		imap --with-imap-ssl --with-kerberos 	; 		docker-php-ext-install -j "$(nproc)" 		imap 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 		ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 			apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
ARG POSTFIXADMIN_VERSION=3.3.16
# Thu, 11 Sep 2025 11:18:55 GMT
ARG POSTFIXADMIN_SHA512=d1b8074c32f7912c187c2c37c5cca158432cb85fc415d9efe86cf11f70ab035117053cc579306e224cb180e70fa3c84a68335f18d62b43abf591e8105a00847d
# Thu, 11 Sep 2025 11:18:55 GMT
ENV POSTFIXADMIN_VERSION=3.3.16
# Thu, 11 Sep 2025 11:18:55 GMT
ENV POSTFIXADMIN_SHA512=d1b8074c32f7912c187c2c37c5cca158432cb85fc415d9efe86cf11f70ab035117053cc579306e224cb180e70fa3c84a68335f18d62b43abf591e8105a00847d
# Thu, 11 Sep 2025 11:18:55 GMT
ENV APACHE_DOCUMENT_ROOT=/var/www/html/public
# Thu, 11 Sep 2025 11:18:55 GMT
# ARGS: POSTFIXADMIN_VERSION=3.3.16 POSTFIXADMIN_SHA512=d1b8074c32f7912c187c2c37c5cca158432cb85fc415d9efe86cf11f70ab035117053cc579306e224cb180e70fa3c84a68335f18d62b43abf591e8105a00847d
RUN set -eu; sed -ri -e 's!/var/www/html!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/sites-available/*.conf; 	sed -ri -e 's!/var/www/!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/apache2.conf /etc/apache2/conf-available/*.conf # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
# ARGS: POSTFIXADMIN_VERSION=3.3.16 POSTFIXADMIN_SHA512=d1b8074c32f7912c187c2c37c5cca158432cb85fc415d9efe86cf11f70ab035117053cc579306e224cb180e70fa3c84a68335f18d62b43abf591e8105a00847d
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/postfixadmin-${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Thu, 11 Sep 2025 11:18:55 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:4f520125372ffa3e5f64f19eebfdfce1c8314446e9e3ab2629f5c13cacbd8345`  
		Last Modified: Tue, 21 Oct 2025 00:20:18 GMT  
		Size: 23.9 MB (23934023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15c6d68333875421eb3535fadc8c0e178e2da3d6248184d942f95f881a20e330`  
		Last Modified: Tue, 21 Oct 2025 01:35:42 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a0a64e327ecde037e7ec28073279eae8ad8870e8e4f9f92bc5dd09be7eed4e3`  
		Last Modified: Tue, 21 Oct 2025 01:35:49 GMT  
		Size: 76.1 MB (76147500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d0624afed2597f9aacabb02f828be322da86417a452d6e10f9ef4401d91522e`  
		Last Modified: Tue, 21 Oct 2025 01:35:42 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:421feed5ef0a9320224ac62dbc94666781566f18bde1b3eee5222c24874b2129`  
		Last Modified: Tue, 21 Oct 2025 01:35:44 GMT  
		Size: 18.9 MB (18860047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7492e926498170a363a88b453760f378be21bd56049ea00c29badb4970ced2dc`  
		Last Modified: Tue, 21 Oct 2025 01:35:42 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc6dc9e6baa4c01f5bf3b179d074d7c254fc314c5d552953646bfd0843257cd5`  
		Last Modified: Tue, 21 Oct 2025 01:35:42 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9181962540c195bb5e7f4ae26dc0cf6246e6a4bd3c46b5f216ce302219d29df`  
		Last Modified: Tue, 21 Oct 2025 01:51:19 GMT  
		Size: 12.7 MB (12707493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bed6336ccac05ec0e28836d8efc686ce27bc2b3ad590e53cdbd15351eae379a`  
		Last Modified: Tue, 21 Oct 2025 01:51:18 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af1bf39c88395808d5c5cf021a8f815bd3ee0bbeec3e96d025fb73d7bc56d048`  
		Last Modified: Tue, 21 Oct 2025 01:51:18 GMT  
		Size: 10.1 MB (10061419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fcaa118728b0638755d0aebe0a547c0d4d1e5146c98c503bc8a3fe4c6457bb9`  
		Last Modified: Tue, 21 Oct 2025 01:51:18 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8215a2fb9dd53770ab92ee4431e37169404ecfcf3f136f37132425b12ed71ad9`  
		Last Modified: Tue, 21 Oct 2025 01:51:19 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d29175c00bc973f1ee1ff0e5b8cbbb0b1d6834ed42e386558fb71eaba5a67b5`  
		Last Modified: Tue, 21 Oct 2025 01:51:19 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa87d2067c34cbf2234efbc06637faede618b5844cf3b134a01b171e84bfa15`  
		Last Modified: Tue, 21 Oct 2025 01:51:19 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f501f96ee0d6c6ee0f9b8df8ee75b359758e37b734bbc0d3a1a45010bdac9669`  
		Last Modified: Tue, 21 Oct 2025 04:08:47 GMT  
		Size: 1.1 MB (1058527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4854062b36ae8d310e978d04fb1393dc5f68a098d1448636d91c496a47693e4`  
		Last Modified: Tue, 21 Oct 2025 04:08:47 GMT  
		Size: 882.7 KB (882678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a27d00321968dbb0d1fcb51ad5144c7a922ea2b7451ac4b5734efe0c2a3e249`  
		Last Modified: Tue, 21 Oct 2025 04:08:47 GMT  
		Size: 8.0 KB (8047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c817fff08f289d8923378170cb1556b3096d4d1acda8e2227245f0f324425458`  
		Last Modified: Tue, 21 Oct 2025 04:08:50 GMT  
		Size: 1.9 MB (1871576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2146690cb397a91c236fa692d4ade427fe363a558530ddee039fdc1599e1e2e`  
		Last Modified: Tue, 21 Oct 2025 04:08:47 GMT  
		Size: 1.7 KB (1655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:latest` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:87ce643eff29266770546cc73257698ea3fecdd6979f5e2644ecfec7f2b44031
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.6 KB (36594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbdbb32ed467ca05c9a36cc094f11caacefc39b1824fa4d807130296032f22c1`

```dockerfile
```

-	Layers:
	-	`sha256:f8e0050901b5e66391785af571a3eeeb1f6e91be5989ff985a759f8897357277`  
		Last Modified: Tue, 21 Oct 2025 08:12:25 GMT  
		Size: 36.6 KB (36594 bytes)  
		MIME: application/vnd.in-toto+json

### `postfixadmin:latest` - linux; arm64 variant v8

```console
$ docker pull postfixadmin@sha256:e234c8368e906c9681ca40a8cecde960f8e884262aa97ad5c70a4eb941dfcaaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.7 MB (174716334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51d4e2b87b9b90110a95dac30f06f9e5d5162f39c985ad51513a133dbf050ff7`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 11 Sep 2025 11:18:55 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1759104000'
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 11 Sep 2025 11:18:55 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 11 Sep 2025 11:18:55 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_VERSION=8.3.26
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.26.tar.xz.asc
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_SHA256=2f522eefa02c400c94610d07f25c4fd4c771f95e4a1f55102332ccb40663cbd2
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 11 Sep 2025 11:18:55 GMT
STOPSIGNAL SIGWINCH
# Thu, 11 Sep 2025 11:18:55 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
WORKDIR /var/www/html
# Thu, 11 Sep 2025 11:18:55 GMT
EXPOSE map[80/tcp:{}]
# Thu, 11 Sep 2025 11:18:55 GMT
CMD ["apache2-foreground"]
# Thu, 11 Sep 2025 11:18:55 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		gosu 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 	libc-client2007e-dev 	libkrb5-dev 	libpq-dev 	libsqlite3-dev 	; 		docker-php-ext-configure 		imap --with-imap-ssl --with-kerberos 	; 		docker-php-ext-install -j "$(nproc)" 		imap 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 		ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 			apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
ARG POSTFIXADMIN_VERSION=3.3.16
# Thu, 11 Sep 2025 11:18:55 GMT
ARG POSTFIXADMIN_SHA512=d1b8074c32f7912c187c2c37c5cca158432cb85fc415d9efe86cf11f70ab035117053cc579306e224cb180e70fa3c84a68335f18d62b43abf591e8105a00847d
# Thu, 11 Sep 2025 11:18:55 GMT
ENV POSTFIXADMIN_VERSION=3.3.16
# Thu, 11 Sep 2025 11:18:55 GMT
ENV POSTFIXADMIN_SHA512=d1b8074c32f7912c187c2c37c5cca158432cb85fc415d9efe86cf11f70ab035117053cc579306e224cb180e70fa3c84a68335f18d62b43abf591e8105a00847d
# Thu, 11 Sep 2025 11:18:55 GMT
ENV APACHE_DOCUMENT_ROOT=/var/www/html/public
# Thu, 11 Sep 2025 11:18:55 GMT
# ARGS: POSTFIXADMIN_VERSION=3.3.16 POSTFIXADMIN_SHA512=d1b8074c32f7912c187c2c37c5cca158432cb85fc415d9efe86cf11f70ab035117053cc579306e224cb180e70fa3c84a68335f18d62b43abf591e8105a00847d
RUN set -eu; sed -ri -e 's!/var/www/html!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/sites-available/*.conf; 	sed -ri -e 's!/var/www/!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/apache2.conf /etc/apache2/conf-available/*.conf # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
# ARGS: POSTFIXADMIN_VERSION=3.3.16 POSTFIXADMIN_SHA512=d1b8074c32f7912c187c2c37c5cca158432cb85fc415d9efe86cf11f70ab035117053cc579306e224cb180e70fa3c84a68335f18d62b43abf591e8105a00847d
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/postfixadmin-${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Thu, 11 Sep 2025 11:18:55 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:f4e51325a7cb57cd9ae67bd9540483838b96bf7c9b0bf18205d9d30819e9ca38`  
		Last Modified: Mon, 29 Sep 2025 23:34:17 GMT  
		Size: 28.1 MB (28102145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:362cb5438649805147afb0804499dd5344c514d1a42ee81e2157648eb7410f9f`  
		Last Modified: Tue, 30 Sep 2025 00:01:02 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03df2072b3254f65082609b36336354f908fae3e0b8b4ed3a1d9022247f0fc86`  
		Last Modified: Tue, 30 Sep 2025 00:01:09 GMT  
		Size: 98.2 MB (98164904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b419d3a5b1d04d5e11a834638c65e4deb1fdbd3ed1ab3ddfa3dbfd9a81d1ac80`  
		Last Modified: Tue, 30 Sep 2025 00:01:02 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a55e9bc392eaf3c5b79adc9895fb4a481e3425bc8925fa6588be0eb01b88085`  
		Last Modified: Tue, 30 Sep 2025 00:01:07 GMT  
		Size: 20.2 MB (20159032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8021e76bf8cbf4b1487ca7586a10ed6303978035c1ca9ea09cf10689e534d012`  
		Last Modified: Tue, 30 Sep 2025 00:01:04 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d6cbcf50ec0046872a58e1962027a8c28a22d80cf330c6d6b4cac81e420e192`  
		Last Modified: Tue, 30 Sep 2025 00:01:05 GMT  
		Size: 481.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1a45110f9f4858848245e2b08e155aa8996187bde322121213e98db898fbe71`  
		Last Modified: Tue, 30 Sep 2025 00:05:07 GMT  
		Size: 12.7 MB (12709286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0892a8aed47fb225149579521d8a0da6c0d11daf9557fb0c4b5296f99201a6b`  
		Last Modified: Tue, 30 Sep 2025 00:05:06 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eebbb7955183e7b334c3c59e54f29018b51cd0c02dbe073ee887677f07624ade`  
		Last Modified: Tue, 30 Sep 2025 00:05:08 GMT  
		Size: 11.7 MB (11683533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5cdb77a01ac25cb13ab3463fe8dfde5687ae9e104843d61c85fde2102cfd2d2`  
		Last Modified: Tue, 30 Sep 2025 00:05:06 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f978b409d3d376675c585877fef914442b0fc0869e8b756c136e00a706cf0265`  
		Last Modified: Tue, 30 Sep 2025 00:05:06 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14317ca733b5c38f992116773e722731b7d7cda28cf2d72b142444c48dbd5791`  
		Last Modified: Tue, 30 Sep 2025 00:05:07 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a67dcd186184121c1272fa635ea407851b3a3dd2f414cb017936dd5bd2f69a30`  
		Last Modified: Tue, 30 Sep 2025 00:05:07 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a93ecb41664dc8c80c5a4c728198bf56f58d5b1ab468257155e9d470d3dcc03c`  
		Last Modified: Tue, 30 Sep 2025 00:58:31 GMT  
		Size: 1.0 MB (1022498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3703287fa879ce9ca62f3d33b92e570c656f2ee92938627be8406d8713f59c42`  
		Last Modified: Tue, 30 Sep 2025 00:58:31 GMT  
		Size: 987.9 KB (987943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38786b4aed9c78750ee90b4c68d7d79e2e459f526380c95a3c6ab1f6673affde`  
		Last Modified: Tue, 30 Sep 2025 00:58:31 GMT  
		Size: 8.0 KB (8047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d98c8f484065e5df71b7e8485d91712756deab80e1f040b5f4976bb28ccfdf6`  
		Last Modified: Tue, 30 Sep 2025 00:58:32 GMT  
		Size: 1.9 MB (1871574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94dd0c24b8112885e4b3518cf15414fe584add24d69c2dc7ae28c2578e5eda4a`  
		Last Modified: Tue, 30 Sep 2025 00:58:32 GMT  
		Size: 1.7 KB (1652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:latest` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:a4c5b9003159348a04914d64ad4fa7dbb612e092cd5b23a0f3120d9b1ec7eabb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.6 KB (36640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eb8acba7aa841f442c3cc7ccce8b6dd89d0ac16205011ed62ad09c56de75529`

```dockerfile
```

-	Layers:
	-	`sha256:ebc7fe8575efa0174563c222e5cb2c37db0f7aa4c919ade2b29565c7193cc895`  
		Last Modified: Wed, 01 Oct 2025 20:11:40 GMT  
		Size: 36.6 KB (36640 bytes)  
		MIME: application/vnd.in-toto+json

### `postfixadmin:latest` - linux; 386

```console
$ docker pull postfixadmin@sha256:f1ff2ab39f5661bd97d9bfad57c26e336e385792119204ad697c6fb192f0121c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.0 MB (179956858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e000708b1ba4de9e26155f5059c2df35e73389eeb0f76c09f24022cf1452f3d6`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 11 Sep 2025 11:18:55 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1759104000'
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 11 Sep 2025 11:18:55 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 11 Sep 2025 11:18:55 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_VERSION=8.3.26
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.26.tar.xz.asc
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_SHA256=2f522eefa02c400c94610d07f25c4fd4c771f95e4a1f55102332ccb40663cbd2
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 11 Sep 2025 11:18:55 GMT
STOPSIGNAL SIGWINCH
# Thu, 11 Sep 2025 11:18:55 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
WORKDIR /var/www/html
# Thu, 11 Sep 2025 11:18:55 GMT
EXPOSE map[80/tcp:{}]
# Thu, 11 Sep 2025 11:18:55 GMT
CMD ["apache2-foreground"]
# Thu, 11 Sep 2025 11:18:55 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		gosu 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 	libc-client2007e-dev 	libkrb5-dev 	libpq-dev 	libsqlite3-dev 	; 		docker-php-ext-configure 		imap --with-imap-ssl --with-kerberos 	; 		docker-php-ext-install -j "$(nproc)" 		imap 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 		ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 			apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
ARG POSTFIXADMIN_VERSION=3.3.16
# Thu, 11 Sep 2025 11:18:55 GMT
ARG POSTFIXADMIN_SHA512=d1b8074c32f7912c187c2c37c5cca158432cb85fc415d9efe86cf11f70ab035117053cc579306e224cb180e70fa3c84a68335f18d62b43abf591e8105a00847d
# Thu, 11 Sep 2025 11:18:55 GMT
ENV POSTFIXADMIN_VERSION=3.3.16
# Thu, 11 Sep 2025 11:18:55 GMT
ENV POSTFIXADMIN_SHA512=d1b8074c32f7912c187c2c37c5cca158432cb85fc415d9efe86cf11f70ab035117053cc579306e224cb180e70fa3c84a68335f18d62b43abf591e8105a00847d
# Thu, 11 Sep 2025 11:18:55 GMT
ENV APACHE_DOCUMENT_ROOT=/var/www/html/public
# Thu, 11 Sep 2025 11:18:55 GMT
# ARGS: POSTFIXADMIN_VERSION=3.3.16 POSTFIXADMIN_SHA512=d1b8074c32f7912c187c2c37c5cca158432cb85fc415d9efe86cf11f70ab035117053cc579306e224cb180e70fa3c84a68335f18d62b43abf591e8105a00847d
RUN set -eu; sed -ri -e 's!/var/www/html!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/sites-available/*.conf; 	sed -ri -e 's!/var/www/!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/apache2.conf /etc/apache2/conf-available/*.conf # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
# ARGS: POSTFIXADMIN_VERSION=3.3.16 POSTFIXADMIN_SHA512=d1b8074c32f7912c187c2c37c5cca158432cb85fc415d9efe86cf11f70ab035117053cc579306e224cb180e70fa3c84a68335f18d62b43abf591e8105a00847d
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/postfixadmin-${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Thu, 11 Sep 2025 11:18:55 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:5a19917fb037e6569ceef43a0b0faa5c3f8554f4d9b154320d254dea136b463a`  
		Last Modified: Mon, 29 Sep 2025 23:35:20 GMT  
		Size: 29.2 MB (29209630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0656bf04a20a86e28036473736ac09f859f0e4e02865f50c94fbf9a171aec25b`  
		Last Modified: Tue, 30 Sep 2025 00:00:14 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c7f9980b08865b4a6124d10726f4af312953f35cc3352b372660293d81ddd81`  
		Last Modified: Tue, 30 Sep 2025 00:00:21 GMT  
		Size: 101.5 MB (101517480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:811d5338f099e2984f8f9c5c4f456ea22cdce8fe6fcc55d450d50c10a6f3ce7e`  
		Last Modified: Tue, 30 Sep 2025 00:00:02 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87e0e56ebc0ca0f3beb569559607312bbc89944744c9b28b25d710d4e4c3f135`  
		Last Modified: Tue, 30 Sep 2025 00:00:16 GMT  
		Size: 20.7 MB (20658395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c602bd31b5ee6281563cf1c1f0b7281fbfdf82e7e3e0e2ccbbe3cb17460d7a27`  
		Last Modified: Tue, 30 Sep 2025 00:00:14 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c351bad5690404f896a76e664f6ca526c09b6ae4280a743e6983e1fa5555f4bd`  
		Last Modified: Tue, 30 Sep 2025 00:00:14 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1398e2731062ea7f1d5a751dc880a74942a6017a653f6a68e672081db8b4296`  
		Last Modified: Tue, 30 Sep 2025 00:03:30 GMT  
		Size: 12.7 MB (12708640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:996cec4117d6b8261b1a009594873e316de96176ea64ad9dd07d05849ba0746a`  
		Last Modified: Tue, 30 Sep 2025 00:03:27 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec5d66584933fab298790bfbb94fcdf8906d7086aaa203cbede7399d0019cbb8`  
		Last Modified: Tue, 30 Sep 2025 00:03:28 GMT  
		Size: 11.9 MB (11883003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16817abc1d0f4356997a2b5646c04902b59bf6ce0689616476b19f9b75a35022`  
		Last Modified: Tue, 30 Sep 2025 00:03:27 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fd02a4ee8afac1b76489deba7bc3feb151ded5bc298430445bf3365bec5aee9`  
		Last Modified: Tue, 30 Sep 2025 00:03:27 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa75a4be18e68a485f7574e422cdb51056615d938cc244c4706263b5083c2164`  
		Last Modified: Tue, 30 Sep 2025 00:03:28 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a81d51c2f434800d4495a750691c7b6fa0f34ee923bf361869e09d309bdbf837`  
		Last Modified: Tue, 30 Sep 2025 00:03:28 GMT  
		Size: 887.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa0eedcebd5ab4113ffc84bc484f9babd9db047aeb7180c13cdb31b715aec9f7`  
		Last Modified: Tue, 30 Sep 2025 00:49:04 GMT  
		Size: 1.1 MB (1077378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e325efa7a479b1be660ed1319365f14de6b0d22e7cbd4b82e7b47f78ad78267a`  
		Last Modified: Tue, 30 Sep 2025 00:49:04 GMT  
		Size: 1.0 MB (1015343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0c7e6999bbe808e0ea11a93351943d7781cc818601b85a21e3b494f6a8fc25e`  
		Last Modified: Tue, 30 Sep 2025 00:49:04 GMT  
		Size: 8.0 KB (8047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70010b9ca1a516d2ad053f147b592d2f80c3ba50b392aa3130cd89f095092bc`  
		Last Modified: Tue, 30 Sep 2025 00:49:04 GMT  
		Size: 1.9 MB (1871574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e006b29a1953e436df2f6a37cdef957c35744803a9ec58f607e94289ea9c2d7`  
		Last Modified: Tue, 30 Sep 2025 00:49:04 GMT  
		Size: 1.7 KB (1651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:latest` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:53e18f082693ff1fe514bc57eb3838b757395c0847e152e9ce7b25866860f157
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 KB (36395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e63c228e4a3cc1980fce7b68d822ba42480149819d0363388ca53e992745acf5`

```dockerfile
```

-	Layers:
	-	`sha256:2174bf0b54b4e4520ecdcc76ffe9e12c60ef25c0473bf1e2ef906344be0425cc`  
		Last Modified: Wed, 01 Oct 2025 23:10:31 GMT  
		Size: 36.4 KB (36395 bytes)  
		MIME: application/vnd.in-toto+json

### `postfixadmin:latest` - linux; mips64le

```console
$ docker pull postfixadmin@sha256:b5f9872f557eb374832f6d9f823eb9e685edf6292d7b9bfb1b4e65325d398d5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156529543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40d66fec9daa450d36abc1626e4446dab76366952914ef955c6b172ce82e50d2`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 11 Sep 2025 11:18:55 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1759104000'
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 11 Sep 2025 11:18:55 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 11 Sep 2025 11:18:55 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_VERSION=8.3.26
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.26.tar.xz.asc
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_SHA256=2f522eefa02c400c94610d07f25c4fd4c771f95e4a1f55102332ccb40663cbd2
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 11 Sep 2025 11:18:55 GMT
STOPSIGNAL SIGWINCH
# Thu, 11 Sep 2025 11:18:55 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
WORKDIR /var/www/html
# Thu, 11 Sep 2025 11:18:55 GMT
EXPOSE map[80/tcp:{}]
# Thu, 11 Sep 2025 11:18:55 GMT
CMD ["apache2-foreground"]
# Thu, 11 Sep 2025 11:18:55 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		gosu 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 	libc-client2007e-dev 	libkrb5-dev 	libpq-dev 	libsqlite3-dev 	; 		docker-php-ext-configure 		imap --with-imap-ssl --with-kerberos 	; 		docker-php-ext-install -j "$(nproc)" 		imap 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 		ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 			apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
ARG POSTFIXADMIN_VERSION=3.3.16
# Thu, 11 Sep 2025 11:18:55 GMT
ARG POSTFIXADMIN_SHA512=d1b8074c32f7912c187c2c37c5cca158432cb85fc415d9efe86cf11f70ab035117053cc579306e224cb180e70fa3c84a68335f18d62b43abf591e8105a00847d
# Thu, 11 Sep 2025 11:18:55 GMT
ENV POSTFIXADMIN_VERSION=3.3.16
# Thu, 11 Sep 2025 11:18:55 GMT
ENV POSTFIXADMIN_SHA512=d1b8074c32f7912c187c2c37c5cca158432cb85fc415d9efe86cf11f70ab035117053cc579306e224cb180e70fa3c84a68335f18d62b43abf591e8105a00847d
# Thu, 11 Sep 2025 11:18:55 GMT
ENV APACHE_DOCUMENT_ROOT=/var/www/html/public
# Thu, 11 Sep 2025 11:18:55 GMT
# ARGS: POSTFIXADMIN_VERSION=3.3.16 POSTFIXADMIN_SHA512=d1b8074c32f7912c187c2c37c5cca158432cb85fc415d9efe86cf11f70ab035117053cc579306e224cb180e70fa3c84a68335f18d62b43abf591e8105a00847d
RUN set -eu; sed -ri -e 's!/var/www/html!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/sites-available/*.conf; 	sed -ri -e 's!/var/www/!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/apache2.conf /etc/apache2/conf-available/*.conf # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
# ARGS: POSTFIXADMIN_VERSION=3.3.16 POSTFIXADMIN_SHA512=d1b8074c32f7912c187c2c37c5cca158432cb85fc415d9efe86cf11f70ab035117053cc579306e224cb180e70fa3c84a68335f18d62b43abf591e8105a00847d
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/postfixadmin-${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Thu, 11 Sep 2025 11:18:55 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:73d0a1261a90ced7c792643cb457a2c9f7bbeca1bcb84939b4029c5a1f01f26c`  
		Last Modified: Mon, 29 Sep 2025 23:34:06 GMT  
		Size: 28.5 MB (28513676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03232016453cd060197e2a81f928170eb114761525dd3c00d9c3384ae2ea93a1`  
		Last Modified: Tue, 30 Sep 2025 01:01:06 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:328cd0006dcf6f780bfb278c18a1cd05d5749f4ae1dc56b6871eda9ce8337a0f`  
		Last Modified: Tue, 30 Sep 2025 01:01:10 GMT  
		Size: 80.7 MB (80669954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b051af170b89147ad2709eb996909dd4f1c5c675586ecff406438604a808c3f`  
		Last Modified: Tue, 30 Sep 2025 01:01:06 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b8f48641d932ec49521be7cec7e78ea4a22aa760bb742df9a0cfcbe1e919c93`  
		Last Modified: Tue, 30 Sep 2025 01:21:37 GMT  
		Size: 20.1 MB (20077207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96157c2a8dfe5add66d6c626e94a5d9862da2ba276c6a5513379adfad12bf4b2`  
		Last Modified: Tue, 30 Sep 2025 01:21:35 GMT  
		Size: 440.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:676f70b4aebf8e81a34ec1464fcdb561265c9b108099c6f18d0a226a6295a3fe`  
		Last Modified: Tue, 30 Sep 2025 01:21:35 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c87d8b146cc3fa14be5c84ca4060afca0e6d8143fcf49fc4d3158827eb03b2`  
		Last Modified: Tue, 30 Sep 2025 03:47:23 GMT  
		Size: 12.7 MB (12707226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbe73a536ea645bff53e9dd2bd62a67ef0ae2aa1755e2d91d75ab685555b2915`  
		Last Modified: Tue, 30 Sep 2025 03:47:22 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b74011f18afe485e2ea85a3abeae6ee2170357b432810770d4f27be8e9487d3`  
		Last Modified: Tue, 30 Sep 2025 03:47:23 GMT  
		Size: 10.7 MB (10741455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87d7012984302569b88986e30f646377ced0bceb4cd7238f9f8dc1f40e17f4e2`  
		Last Modified: Tue, 30 Sep 2025 03:47:22 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99e2be4b299b38bfb2963879ed2dc65c2bcf986436b873a8e66a4a3a69c74654`  
		Last Modified: Tue, 30 Sep 2025 03:47:22 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d780ac50f5ab4fca389938027b4c1c1428c0ccb4ed111988dfb12877a11c5e7`  
		Last Modified: Tue, 30 Sep 2025 03:47:22 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:172c549cd41a41766f4600056b437edc5dccbaf41dac29f4fdc6805c48f493a6`  
		Last Modified: Tue, 30 Sep 2025 03:47:22 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85a8c2575406f73dadb531efca290b757a5ca295ecbc14a50bedcd2d58be916f`  
		Last Modified: Tue, 30 Sep 2025 20:20:27 GMT  
		Size: 973.9 KB (973922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93c7e01642ea5eba23b9cac59e86ac2eb9dd6abb19912fd1df52529c93ca725f`  
		Last Modified: Tue, 30 Sep 2025 20:20:27 GMT  
		Size: 959.1 KB (959084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e73070747ef678e733eef150863807cc18afd055068b71cbbebba77d4757000c`  
		Last Modified: Tue, 30 Sep 2025 20:20:27 GMT  
		Size: 8.0 KB (8048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7654f6ed1174e425865ee1df8f086f71a4b2a5d65d8bb2586bd5ec86c9bf0d87`  
		Last Modified: Tue, 30 Sep 2025 20:20:28 GMT  
		Size: 1.9 MB (1871575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a9af8d6eaeae89377ae071403f88876354bc46f0940a8807cc89551e6703d3f`  
		Last Modified: Tue, 30 Sep 2025 20:20:28 GMT  
		Size: 1.7 KB (1653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:latest` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:d1dbbb9e4a854c57a1c1fab7c61b4f857749ecb7c05dbd313785361e40638f7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.5 KB (36549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50b3d7b57bdbbc2ef135cc3b1978e7b6667657e4145b784b86aa520416e55770`

```dockerfile
```

-	Layers:
	-	`sha256:3cb0e7b5294cf5aa8c7c274ca8aaff10f90aaa1e61f4f478934fd8929509db93`  
		Last Modified: Wed, 01 Oct 2025 20:11:45 GMT  
		Size: 36.5 KB (36549 bytes)  
		MIME: application/vnd.in-toto+json

### `postfixadmin:latest` - linux; ppc64le

```console
$ docker pull postfixadmin@sha256:0fe4f1844ccecbc39d3f2e2f448f38ee30ad9f15b7732e5eeda90f745c37e44b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.5 MB (185532168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb6ec59369d2b493dff45c2d7fb5d6402967337ce9f5e2bac68c1d3ca09ae490`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 11 Sep 2025 11:18:55 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1759104000'
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 11 Sep 2025 11:18:55 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 11 Sep 2025 11:18:55 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_VERSION=8.3.26
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.26.tar.xz.asc
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_SHA256=2f522eefa02c400c94610d07f25c4fd4c771f95e4a1f55102332ccb40663cbd2
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 11 Sep 2025 11:18:55 GMT
STOPSIGNAL SIGWINCH
# Thu, 11 Sep 2025 11:18:55 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
WORKDIR /var/www/html
# Thu, 11 Sep 2025 11:18:55 GMT
EXPOSE map[80/tcp:{}]
# Thu, 11 Sep 2025 11:18:55 GMT
CMD ["apache2-foreground"]
# Thu, 11 Sep 2025 11:18:55 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		gosu 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 	libc-client2007e-dev 	libkrb5-dev 	libpq-dev 	libsqlite3-dev 	; 		docker-php-ext-configure 		imap --with-imap-ssl --with-kerberos 	; 		docker-php-ext-install -j "$(nproc)" 		imap 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 		ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 			apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
ARG POSTFIXADMIN_VERSION=3.3.16
# Thu, 11 Sep 2025 11:18:55 GMT
ARG POSTFIXADMIN_SHA512=d1b8074c32f7912c187c2c37c5cca158432cb85fc415d9efe86cf11f70ab035117053cc579306e224cb180e70fa3c84a68335f18d62b43abf591e8105a00847d
# Thu, 11 Sep 2025 11:18:55 GMT
ENV POSTFIXADMIN_VERSION=3.3.16
# Thu, 11 Sep 2025 11:18:55 GMT
ENV POSTFIXADMIN_SHA512=d1b8074c32f7912c187c2c37c5cca158432cb85fc415d9efe86cf11f70ab035117053cc579306e224cb180e70fa3c84a68335f18d62b43abf591e8105a00847d
# Thu, 11 Sep 2025 11:18:55 GMT
ENV APACHE_DOCUMENT_ROOT=/var/www/html/public
# Thu, 11 Sep 2025 11:18:55 GMT
# ARGS: POSTFIXADMIN_VERSION=3.3.16 POSTFIXADMIN_SHA512=d1b8074c32f7912c187c2c37c5cca158432cb85fc415d9efe86cf11f70ab035117053cc579306e224cb180e70fa3c84a68335f18d62b43abf591e8105a00847d
RUN set -eu; sed -ri -e 's!/var/www/html!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/sites-available/*.conf; 	sed -ri -e 's!/var/www/!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/apache2.conf /etc/apache2/conf-available/*.conf # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
# ARGS: POSTFIXADMIN_VERSION=3.3.16 POSTFIXADMIN_SHA512=d1b8074c32f7912c187c2c37c5cca158432cb85fc415d9efe86cf11f70ab035117053cc579306e224cb180e70fa3c84a68335f18d62b43abf591e8105a00847d
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/postfixadmin-${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Thu, 11 Sep 2025 11:18:55 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:2dae4fd387571f8090d4bc2fed08c7939fa2ac7aed0e2814aea4306333899e47`  
		Last Modified: Mon, 29 Sep 2025 23:34:09 GMT  
		Size: 32.1 MB (32068697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9224126999b17ea18ad3192bf1f731d4bb9aa32a52f09c442a3de3ba3b786f3`  
		Last Modified: Tue, 30 Sep 2025 00:21:12 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2e6783fc03077e22b7c9e12c11882548b0054a2663a8ef49358f7327baf349e`  
		Last Modified: Tue, 30 Sep 2025 00:21:18 GMT  
		Size: 103.3 MB (103328743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d33ae54ede2b3ffe909b51995334afb653bfac09e40805963f18c29327385318`  
		Last Modified: Tue, 30 Sep 2025 00:21:11 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55e826edd8f76372320eb04b480569c9550cc354df72e5453efc1e24f8ca6435`  
		Last Modified: Tue, 30 Sep 2025 00:26:39 GMT  
		Size: 21.3 MB (21317847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73eacfec890bc561637d332e33d282a65c2cee7448068ffa32b8bd41b9d125d2`  
		Last Modified: Tue, 30 Sep 2025 00:26:28 GMT  
		Size: 436.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45a5094e1ce142c1a5814e699f6a3866a8717dbe8a8afb25a8345bb4dabf2de6`  
		Last Modified: Tue, 30 Sep 2025 00:26:28 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab4cd037a7381bf2aed527327ea502a1bbfd6e187fa6d1d3970426aedd765fe8`  
		Last Modified: Tue, 30 Sep 2025 01:03:41 GMT  
		Size: 12.7 MB (12708943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8002f7e0257683261c8bbdfaa70173b7e7d5a5f2881e8e3e9b4dd39acd64cb04`  
		Last Modified: Tue, 30 Sep 2025 01:03:36 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e187af3ab77ba8b655c46e9225723a4270938644552feb31d31d2604064c848`  
		Last Modified: Tue, 30 Sep 2025 01:03:41 GMT  
		Size: 12.1 MB (12082803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15b88892b85a7a3e4fa10e8d5bfe489738a8fac4bfb2ddc4ab40944574410c79`  
		Last Modified: Tue, 30 Sep 2025 01:03:36 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a84c43a857ca25ba9db42ddeef99a39bb8de5ac3e22f631c6c66b21e99e94354`  
		Last Modified: Tue, 30 Sep 2025 01:03:36 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:800913fcb5e5889aede3b8df07a4487f18ad2d3b82938ca8c9fff8ca9aecfb27`  
		Last Modified: Tue, 30 Sep 2025 01:03:36 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1552f9489dd07c44a1dcfb75885e1484b495de0b409e54b89d116464548e0c1d`  
		Last Modified: Tue, 30 Sep 2025 01:03:36 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3adf05e137972803b883f266ddfed589a506f89c42ca50563ec14fc5716dddc6`  
		Last Modified: Tue, 30 Sep 2025 08:49:25 GMT  
		Size: 1.0 MB (1009549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cc7f44e0acc92eaef7ee51a42c43174e4752f3a7a685c185ede85d5809224fa`  
		Last Modified: Tue, 30 Sep 2025 08:49:25 GMT  
		Size: 1.1 MB (1128572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b13f801a3a64bab378c42ce3955967a74db6e4799b4227a7a64190caea1cef0`  
		Last Modified: Tue, 30 Sep 2025 08:49:25 GMT  
		Size: 8.0 KB (8048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d21ce65873b673120bd214338cbb4732e0caec0b3be69da1e04f3f872f55d42`  
		Last Modified: Tue, 30 Sep 2025 08:49:25 GMT  
		Size: 1.9 MB (1871574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c37ed4e2da375a9fb5ffc385682b5d4a787c58df3991179c959512362b3b525d`  
		Last Modified: Tue, 30 Sep 2025 08:49:25 GMT  
		Size: 1.7 KB (1653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:latest` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:32b3b5461188575b1c4a869d1e181ede3507410a3c191c5a3d0c156e60aaf4de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.5 KB (36527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:508ad7c76f83ec0fc5a17952dfc3abe4bdf62cb1e56b04cae5e7eb1af7446e6b`

```dockerfile
```

-	Layers:
	-	`sha256:cbda8210f56fcbee53491a9106f7e41732542f2ee6340f5ebcd2134d40870193`  
		Last Modified: Wed, 01 Oct 2025 20:27:35 GMT  
		Size: 36.5 KB (36527 bytes)  
		MIME: application/vnd.in-toto+json

### `postfixadmin:latest` - linux; s390x

```console
$ docker pull postfixadmin@sha256:0ede3c5e865776182866702b5ac944488080ecabead7c5d81fb7289e29ab1a69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.1 MB (155140140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daeda12e9427222fe8e3ff5a868519c76abbc8f23eff4c3ed6b014125826d17f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 11 Sep 2025 11:18:55 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1759104000'
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 11 Sep 2025 11:18:55 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 11 Sep 2025 11:18:55 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_VERSION=8.3.26
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.26.tar.xz.asc
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_SHA256=2f522eefa02c400c94610d07f25c4fd4c771f95e4a1f55102332ccb40663cbd2
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 11 Sep 2025 11:18:55 GMT
STOPSIGNAL SIGWINCH
# Thu, 11 Sep 2025 11:18:55 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
WORKDIR /var/www/html
# Thu, 11 Sep 2025 11:18:55 GMT
EXPOSE map[80/tcp:{}]
# Thu, 11 Sep 2025 11:18:55 GMT
CMD ["apache2-foreground"]
# Thu, 11 Sep 2025 11:18:55 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		gosu 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 	libc-client2007e-dev 	libkrb5-dev 	libpq-dev 	libsqlite3-dev 	; 		docker-php-ext-configure 		imap --with-imap-ssl --with-kerberos 	; 		docker-php-ext-install -j "$(nproc)" 		imap 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 		ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 			apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
ARG POSTFIXADMIN_VERSION=3.3.16
# Thu, 11 Sep 2025 11:18:55 GMT
ARG POSTFIXADMIN_SHA512=d1b8074c32f7912c187c2c37c5cca158432cb85fc415d9efe86cf11f70ab035117053cc579306e224cb180e70fa3c84a68335f18d62b43abf591e8105a00847d
# Thu, 11 Sep 2025 11:18:55 GMT
ENV POSTFIXADMIN_VERSION=3.3.16
# Thu, 11 Sep 2025 11:18:55 GMT
ENV POSTFIXADMIN_SHA512=d1b8074c32f7912c187c2c37c5cca158432cb85fc415d9efe86cf11f70ab035117053cc579306e224cb180e70fa3c84a68335f18d62b43abf591e8105a00847d
# Thu, 11 Sep 2025 11:18:55 GMT
ENV APACHE_DOCUMENT_ROOT=/var/www/html/public
# Thu, 11 Sep 2025 11:18:55 GMT
# ARGS: POSTFIXADMIN_VERSION=3.3.16 POSTFIXADMIN_SHA512=d1b8074c32f7912c187c2c37c5cca158432cb85fc415d9efe86cf11f70ab035117053cc579306e224cb180e70fa3c84a68335f18d62b43abf591e8105a00847d
RUN set -eu; sed -ri -e 's!/var/www/html!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/sites-available/*.conf; 	sed -ri -e 's!/var/www/!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/apache2.conf /etc/apache2/conf-available/*.conf # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
# ARGS: POSTFIXADMIN_VERSION=3.3.16 POSTFIXADMIN_SHA512=d1b8074c32f7912c187c2c37c5cca158432cb85fc415d9efe86cf11f70ab035117053cc579306e224cb180e70fa3c84a68335f18d62b43abf591e8105a00847d
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/postfixadmin-${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Thu, 11 Sep 2025 11:18:55 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:ee23af7e2c95e7ad71a0f6edf7e138d45ffffb442811e2b9572806a68ee1338e`  
		Last Modified: Mon, 29 Sep 2025 23:34:05 GMT  
		Size: 26.9 MB (26884320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:980d82124f58a645a9da3f15f3da28d4ca1455d28e5d91846444d1052535447d`  
		Last Modified: Tue, 30 Sep 2025 00:04:01 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b01b9ac7d1cffa33f9a421d32a8141448890b76a8a421333ce992c42c236f2`  
		Last Modified: Tue, 30 Sep 2025 00:04:05 GMT  
		Size: 80.8 MB (80826420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e37f8a2c56e71c89a84dc64f20767ac8e393ae6bf31491b671931026500a94fa`  
		Last Modified: Tue, 30 Sep 2025 00:04:01 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c3685d083390bd60c92d11c2e2ab236933b2524cd63c252f67bc317596f4e4b`  
		Last Modified: Tue, 30 Sep 2025 00:08:30 GMT  
		Size: 19.9 MB (19910066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6a5638c8e94672d92902c3cf9c6c0393af360f85f2aeacb8367aafe726448bc`  
		Last Modified: Tue, 30 Sep 2025 00:08:28 GMT  
		Size: 434.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bf8ee6849a38404ca53b58991fcde9db799e42b9656d3c6688293143ac44192`  
		Last Modified: Tue, 30 Sep 2025 00:08:28 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eb5def321b5231dd9f25fe8d8120ee1b06d1d3a03c5e9dd17a9925accde25c0`  
		Last Modified: Tue, 30 Sep 2025 00:46:15 GMT  
		Size: 12.7 MB (12707919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e7050aba78af363c13634344206fd9083835249cd55e4b10e324c649d70cf60`  
		Last Modified: Tue, 30 Sep 2025 00:46:10 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e856a966adf8e64c0a22929b519415a527f6aba948aa18814c07e25d723bcc8f`  
		Last Modified: Tue, 30 Sep 2025 00:46:10 GMT  
		Size: 10.9 MB (10880363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca2b13fd7e6a073924a5c4cf35cba2c068257ee095c6f136448d360aeaf3a3de`  
		Last Modified: Tue, 30 Sep 2025 00:46:09 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2741cf7dc704c52ff970a3c94d0c098a595f8bb12ec377b93563a048bce79003`  
		Last Modified: Tue, 30 Sep 2025 00:46:10 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:286cf8864e14cda4f51fabc46dc8ac088f75bcaff1a1421972cb02a35eab404d`  
		Last Modified: Tue, 30 Sep 2025 00:46:10 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810e762ab2942c0ddbc0fe061a4fc8f5e9ff402e6e2e25df9a9af16ff16fd5ec`  
		Last Modified: Tue, 30 Sep 2025 00:46:10 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f33d05954d998db86973fa685c2b9ae5b05e69c04e196bdac2ab0074445696ac`  
		Last Modified: Tue, 30 Sep 2025 08:04:27 GMT  
		Size: 1.1 MB (1057849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae1dc999bca380f16f092bf90665f3d8f0b24cde3aa212d5ad1e34496f32f1d2`  
		Last Modified: Tue, 30 Sep 2025 08:04:27 GMT  
		Size: 986.2 KB (986206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c6407fd35e35ccbb49b67bf6888f76372975cc06b0e08bdbd3486284ab35754`  
		Last Modified: Tue, 30 Sep 2025 08:04:27 GMT  
		Size: 8.0 KB (8048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc86c85c613ed830f9b16254ee64f2c0a569a83622f4aa1c174767bb45164473`  
		Last Modified: Tue, 30 Sep 2025 08:04:27 GMT  
		Size: 1.9 MB (1871576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d2b3264d282e277f91c00d0dec123ea4e204dfd0cc4ea01bb5e6507ee18dc0`  
		Last Modified: Tue, 30 Sep 2025 08:04:27 GMT  
		Size: 1.6 KB (1649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:latest` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:8a7d476e446219cb5fb49c7c3c66264aa3a434de19fd0344186b595ebff68608
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 KB (36443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:865c0407677e38f0b4b22a7a2187dbf2b5238610efb446e91ade5dc1111a45be`

```dockerfile
```

-	Layers:
	-	`sha256:692065d0993363a432ca73c0083a2f0874fb2baeaf9b15629c929a1dc2e1d992`  
		Last Modified: Wed, 01 Oct 2025 20:11:50 GMT  
		Size: 36.4 KB (36443 bytes)  
		MIME: application/vnd.in-toto+json
