## `postfixadmin:4-apache`

```console
$ docker pull postfixadmin@sha256:76ddc45da79e30ab42480390067f53478af712233fd016922b26f72503c49d52
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

### `postfixadmin:4-apache` - linux; amd64

```console
$ docker pull postfixadmin@sha256:ea74308d61f09390c520d7d1525d9c18870bccbcec42d7cc6badd69547034796
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.7 MB (204739141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb4886c3b884d5f1a0e2484ed77bd0e6370c9e094ab6ff7349448bb7c6607a1a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:26:53 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 24 Jun 2026 01:27:08 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 24 Jun 2026 01:27:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Wed, 24 Jun 2026 01:27:08 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 24 Jun 2026 01:27:08 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 24 Jun 2026 01:27:08 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 24 Jun 2026 01:27:08 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 24 Jun 2026 01:27:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 24 Jun 2026 01:27:13 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 24 Jun 2026 01:27:13 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 24 Jun 2026 01:27:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Jun 2026 01:27:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Jun 2026 01:27:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 24 Jun 2026 01:27:13 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 24 Jun 2026 01:27:13 GMT
ENV PHP_VERSION=8.3.31
# Wed, 24 Jun 2026 01:27:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.31.tar.xz.asc
# Wed, 24 Jun 2026 01:27:13 GMT
ENV PHP_SHA256=66410cee07f4b2baeb0843140bb2a2b52ef930b5cf9b3d6e6d158b33aae8fa37
# Wed, 24 Jun 2026 01:27:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 24 Jun 2026 01:27:20 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:29:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 24 Jun 2026 01:29:51 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:29:51 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 24 Jun 2026 01:29:51 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 24 Jun 2026 01:29:51 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 24 Jun 2026 01:29:51 GMT
STOPSIGNAL SIGWINCH
# Wed, 24 Jun 2026 01:29:51 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:29:51 GMT
WORKDIR /var/www/html
# Wed, 24 Jun 2026 01:29:51 GMT
EXPOSE map[80/tcp:{}]
# Wed, 24 Jun 2026 01:29:51 GMT
CMD ["apache2-foreground"]
# Tue, 30 Jun 2026 19:07:32 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Tue, 30 Jun 2026 19:07:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		gosu 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Jun 2026 19:07:50 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libpq-dev 		libsqlite3-dev 	; 	docker-php-ext-install -j "$(nproc)" 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -rt apt-mark manual; 			apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean # buildkit
# Tue, 30 Jun 2026 19:07:50 GMT
ARG POSTFIXADMIN_VERSION=4.0.4
# Tue, 30 Jun 2026 19:07:50 GMT
ARG POSTFIXADMIN_SHA512=cce293e92e03f06a20ddbe09a9faec251af3f166f38565429d791feaf832096344a62656bab2a60bbd360545c1a0bd3ed05e11f4a4e46f04858e84639c5391dd
# Tue, 30 Jun 2026 19:07:50 GMT
ENV POSTFIXADMIN_VERSION=4.0.4
# Tue, 30 Jun 2026 19:07:50 GMT
ENV POSTFIXADMIN_SHA512=cce293e92e03f06a20ddbe09a9faec251af3f166f38565429d791feaf832096344a62656bab2a60bbd360545c1a0bd3ed05e11f4a4e46f04858e84639c5391dd
# Tue, 30 Jun 2026 19:07:50 GMT
ENV APACHE_DOCUMENT_ROOT=/var/www/html/public
# Tue, 30 Jun 2026 19:07:50 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.4 POSTFIXADMIN_SHA512=cce293e92e03f06a20ddbe09a9faec251af3f166f38565429d791feaf832096344a62656bab2a60bbd360545c1a0bd3ed05e11f4a4e46f04858e84639c5391dd
RUN set -eu; sed -ri -e 's!/var/www/html!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/sites-available/*.conf; 	sed -ri -e 's!/var/www/!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/apache2.conf /etc/apache2/conf-available/*.conf # buildkit
# Tue, 30 Jun 2026 19:07:51 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.4 POSTFIXADMIN_SHA512=cce293e92e03f06a20ddbe09a9faec251af3f166f38565429d791feaf832096344a62656bab2a60bbd360545c1a0bd3ed05e11f4a4e46f04858e84639c5391dd
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/v${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin # buildkit
# Tue, 30 Jun 2026 19:07:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Jun 2026 19:07:51 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 30 Jun 2026 19:07:51 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 30 Jun 2026 19:07:59 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.4 POSTFIXADMIN_SHA512=cce293e92e03f06a20ddbe09a9faec251af3f166f38565429d791feaf832096344a62656bab2a60bbd360545c1a0bd3ed05e11f4a4e46f04858e84639c5391dd
RUN set -eux; 	composerDeps=" 		unzip 	"; 	apt-get update; 	apt-get install -y --no-install-recommends $composerDeps; 		export COMPOSER_HOME="$(mktemp -d)"; 	composer install --ignore-platform-req=ext-mysqli --no-dev --no-interaction --working-dir /usr/src/postfixadmin; 	rm -rf "$COMPOSER_HOME"; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $composerDeps; 	apt-get dist-clean # buildkit
# Tue, 30 Jun 2026 19:07:59 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Tue, 30 Jun 2026 19:07:59 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:e95a6c7ea7d49b37920899b023ecd0e32796c976c1748491f76cae53ba86d13a`  
		Last Modified: Wed, 24 Jun 2026 00:28:31 GMT  
		Size: 29.8 MB (29785419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c8d99b0993970483d4816f624eb877fb895013e2731d0b1ef4e7fdb887d6e87`  
		Last Modified: Wed, 24 Jun 2026 01:30:13 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35fb229d66d71c0ed5b5e1da93a19c6df01a1488d7c7caa0dc6b96a6533b2162`  
		Last Modified: Wed, 24 Jun 2026 01:30:17 GMT  
		Size: 117.8 MB (117840063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d5b8f076ceb8fc611252f20b7dd1ec0930d65191f0af4de4347719e4d11c89e`  
		Last Modified: Wed, 24 Jun 2026 01:30:14 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02f85b3f43f2046f4e6a57b90b5b2c91f68dcf187ae8a9b49fe4796e49141a1c`  
		Last Modified: Wed, 24 Jun 2026 01:30:14 GMT  
		Size: 4.2 MB (4227865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bff4cd0dbd7d5344b61b518c322ec701b04f9a66a9557a1860b931cbdd464efa`  
		Last Modified: Wed, 24 Jun 2026 01:30:15 GMT  
		Size: 431.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5592b32317e056f0371d6c73bdd7246b32ff10c7035d36c39d65f83a0d9b0198`  
		Last Modified: Wed, 24 Jun 2026 01:30:16 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97322e0a5ac23a4e402c39480ddca8156bebbefe4d8c1df6e73d3eb40d331d2e`  
		Last Modified: Wed, 24 Jun 2026 01:30:16 GMT  
		Size: 12.8 MB (12770110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de60d3ea043694be8d354d268f9781ff2b3645b5e8d959bc28410d2fbdf73275`  
		Last Modified: Wed, 24 Jun 2026 01:30:16 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7e34dbf4599de0542927071b981ce8f88e462c43f76d6f6ee0d624a4cd7f4b4`  
		Last Modified: Wed, 24 Jun 2026 01:30:17 GMT  
		Size: 11.7 MB (11715432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea6f168bbc472c2a95266e3d4e227ba10d4d0d345a1466533477c93c157e0b4e`  
		Last Modified: Wed, 24 Jun 2026 01:30:17 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66617053e057acc6616b396aa3b480af11046050539cbd768fc6d31bc73e6867`  
		Last Modified: Wed, 24 Jun 2026 01:30:18 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:276c1fc1b7e468e092de0107fa44b7af19d3672a7c26744a7a4ab11bdb6fe4cc`  
		Last Modified: Wed, 24 Jun 2026 01:30:19 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60ec3c0b368260f5ac8066312f8295b16b4f4c7e752a567f7a2fc1696b4df20`  
		Last Modified: Wed, 24 Jun 2026 01:30:19 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d73f401c449a66de3d541612a240c73bb1b3ff9c1f56dcab5b5e78065655fda`  
		Last Modified: Tue, 30 Jun 2026 19:08:05 GMT  
		Size: 1.4 MB (1352210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76c19d61e45e699fad71a3142bd74fb42bd4747eb7a1bbda2a89fcd6f6bdde62`  
		Last Modified: Tue, 30 Jun 2026 19:08:05 GMT  
		Size: 467.0 KB (467006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:895bd5332f0a790d881eeb54eb9b112ae6d3fae19175082f241af5501ac62eda`  
		Last Modified: Tue, 30 Jun 2026 19:08:05 GMT  
		Size: 7.5 KB (7479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54161e724343f5c5475a2037f85c5f418958c0ef23637bc5afe68671a880cdc3`  
		Last Modified: Tue, 30 Jun 2026 19:08:05 GMT  
		Size: 2.6 MB (2603510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91d2f444568f8cb6493840c6edb5be8f477a163ee5ce381a90aa08be5cb3ca01`  
		Last Modified: Tue, 30 Jun 2026 19:08:07 GMT  
		Size: 1.7 KB (1657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:973cad20767cf4642ede35f3bf1b332ddeb45127aa51de925e0bfec0626b6d70`  
		Last Modified: Tue, 30 Jun 2026 19:08:07 GMT  
		Size: 823.3 KB (823345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20db738266e907ebe92cd3ce11f80d0bf936d03f640effaec940d8ddfc48b6e7`  
		Last Modified: Tue, 30 Jun 2026 19:08:08 GMT  
		Size: 23.1 MB (23139323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:4-apache` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:fcaf12bac55550a0bcb2e46122fd1e81b0fbfcd901c555c8c8b0a84ccfb37820
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 KB (49975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15964137f8e04e43924d2ca9b561844d3fb1dfb3f6e5d9b36a5b38ca0b092cac`

```dockerfile
```

-	Layers:
	-	`sha256:0a1268deab24c6009c05df14fa4161b9f11b5710ace516dca6b2fe729721f69f`  
		Last Modified: Tue, 30 Jun 2026 19:08:05 GMT  
		Size: 50.0 KB (49975 bytes)  
		MIME: application/vnd.in-toto+json

### `postfixadmin:4-apache` - linux; arm variant v7

```console
$ docker pull postfixadmin@sha256:c7d44c4e42ee17774e1e12c46c5a1047725566216a1dfbaff0444f7819db2343
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.4 MB (167355576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f01b21bea37ce4af2f727337c6b6de836111ce1649bdede42e0e1f884da4712`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:34:52 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 24 Jun 2026 01:35:10 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 24 Jun 2026 01:35:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Wed, 24 Jun 2026 01:35:10 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 24 Jun 2026 01:35:10 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 24 Jun 2026 01:35:10 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 24 Jun 2026 01:35:10 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 24 Jun 2026 01:35:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 24 Jun 2026 01:35:17 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 24 Jun 2026 01:35:17 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 24 Jun 2026 01:35:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Jun 2026 01:35:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Jun 2026 01:35:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 24 Jun 2026 01:35:17 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 24 Jun 2026 01:35:17 GMT
ENV PHP_VERSION=8.3.31
# Wed, 24 Jun 2026 01:35:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.31.tar.xz.asc
# Wed, 24 Jun 2026 01:35:17 GMT
ENV PHP_SHA256=66410cee07f4b2baeb0843140bb2a2b52ef930b5cf9b3d6e6d158b33aae8fa37
# Wed, 24 Jun 2026 01:35:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 24 Jun 2026 01:35:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:38:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 24 Jun 2026 01:38:05 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:38:05 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 24 Jun 2026 01:38:05 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 24 Jun 2026 01:38:05 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 24 Jun 2026 01:38:05 GMT
STOPSIGNAL SIGWINCH
# Wed, 24 Jun 2026 01:38:05 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:38:05 GMT
WORKDIR /var/www/html
# Wed, 24 Jun 2026 01:38:05 GMT
EXPOSE map[80/tcp:{}]
# Wed, 24 Jun 2026 01:38:05 GMT
CMD ["apache2-foreground"]
# Tue, 30 Jun 2026 19:09:11 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Tue, 30 Jun 2026 19:09:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		gosu 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Jun 2026 19:09:37 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libpq-dev 		libsqlite3-dev 	; 	docker-php-ext-install -j "$(nproc)" 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -rt apt-mark manual; 			apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean # buildkit
# Tue, 30 Jun 2026 19:09:37 GMT
ARG POSTFIXADMIN_VERSION=4.0.4
# Tue, 30 Jun 2026 19:09:37 GMT
ARG POSTFIXADMIN_SHA512=cce293e92e03f06a20ddbe09a9faec251af3f166f38565429d791feaf832096344a62656bab2a60bbd360545c1a0bd3ed05e11f4a4e46f04858e84639c5391dd
# Tue, 30 Jun 2026 19:09:37 GMT
ENV POSTFIXADMIN_VERSION=4.0.4
# Tue, 30 Jun 2026 19:09:37 GMT
ENV POSTFIXADMIN_SHA512=cce293e92e03f06a20ddbe09a9faec251af3f166f38565429d791feaf832096344a62656bab2a60bbd360545c1a0bd3ed05e11f4a4e46f04858e84639c5391dd
# Tue, 30 Jun 2026 19:09:37 GMT
ENV APACHE_DOCUMENT_ROOT=/var/www/html/public
# Tue, 30 Jun 2026 19:09:38 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.4 POSTFIXADMIN_SHA512=cce293e92e03f06a20ddbe09a9faec251af3f166f38565429d791feaf832096344a62656bab2a60bbd360545c1a0bd3ed05e11f4a4e46f04858e84639c5391dd
RUN set -eu; sed -ri -e 's!/var/www/html!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/sites-available/*.conf; 	sed -ri -e 's!/var/www/!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/apache2.conf /etc/apache2/conf-available/*.conf # buildkit
# Tue, 30 Jun 2026 19:09:38 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.4 POSTFIXADMIN_SHA512=cce293e92e03f06a20ddbe09a9faec251af3f166f38565429d791feaf832096344a62656bab2a60bbd360545c1a0bd3ed05e11f4a4e46f04858e84639c5391dd
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/v${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin # buildkit
# Tue, 30 Jun 2026 19:09:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Jun 2026 19:09:38 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 30 Jun 2026 19:09:38 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 30 Jun 2026 19:09:48 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.4 POSTFIXADMIN_SHA512=cce293e92e03f06a20ddbe09a9faec251af3f166f38565429d791feaf832096344a62656bab2a60bbd360545c1a0bd3ed05e11f4a4e46f04858e84639c5391dd
RUN set -eux; 	composerDeps=" 		unzip 	"; 	apt-get update; 	apt-get install -y --no-install-recommends $composerDeps; 		export COMPOSER_HOME="$(mktemp -d)"; 	composer install --ignore-platform-req=ext-mysqli --no-dev --no-interaction --working-dir /usr/src/postfixadmin; 	rm -rf "$COMPOSER_HOME"; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $composerDeps; 	apt-get dist-clean # buildkit
# Tue, 30 Jun 2026 19:09:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Tue, 30 Jun 2026 19:09:48 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:81c84b0273952340067af970e1fe77a42ea83b4ed1a53319e258d5f1077848f0`  
		Last Modified: Wed, 24 Jun 2026 00:28:38 GMT  
		Size: 26.2 MB (26211051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de9d3d58fcd93bb623d3bf40d560105069105bcb162b2f7f196be2d15c132fcc`  
		Last Modified: Wed, 24 Jun 2026 01:38:22 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19b82b39819079517bda59ac63680c48a0d59ef834a127050a67a9c7b7ac33d5`  
		Last Modified: Wed, 24 Jun 2026 01:38:24 GMT  
		Size: 86.3 MB (86256290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:308c04a93f5abc695be7e27eb34f23047f502da85609ef8767509ed3d2969306`  
		Last Modified: Wed, 24 Jun 2026 01:38:22 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:357b636d3616e1cb7c646004a1c667d1205ebe0a4a085275fa4ca3927dab6f86`  
		Last Modified: Wed, 24 Jun 2026 01:38:22 GMT  
		Size: 3.8 MB (3756700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7d590cd60758b1cdb950e5caae80d26e20cd0f648aa0fe4255e122ec33b6795`  
		Last Modified: Wed, 24 Jun 2026 01:38:23 GMT  
		Size: 431.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b455b0d3ef80b2ca55712f1cc6deccb9163dbfab83e8c81dbb44796edbb95cd5`  
		Last Modified: Wed, 24 Jun 2026 01:38:23 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b362e678358c962daedf29781fdc7ea866f15adda94b119ff6357b23479ea4`  
		Last Modified: Wed, 24 Jun 2026 01:38:24 GMT  
		Size: 12.8 MB (12767749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92ecd6b4edf84b27e547aaa695521bcce6036eed4afd13482b9045bf2d067e65`  
		Last Modified: Wed, 24 Jun 2026 01:38:25 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49e0673eeb152c6c2e62191fd693589bed76f30266fae6f5617c6bddbd12a2c2`  
		Last Modified: Wed, 24 Jun 2026 01:38:25 GMT  
		Size: 10.1 MB (10074026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bc4ba190c02733bb92c0ad35adbc5d9179816df119818d812c1f5424ced4910`  
		Last Modified: Wed, 24 Jun 2026 01:38:25 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6a2a3f488bbb60ac218a6a9e1a1e79ddbf2411fef019e6c7c3c24591a2a122`  
		Last Modified: Wed, 24 Jun 2026 01:38:26 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4296ead16bcf34bf0ac18103739ef3792d1c2488c4e384525951e295a0f839`  
		Last Modified: Wed, 24 Jun 2026 01:38:26 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce436ad10dc7876e391b53a2ac9534c880747077fc1bff41ebe54e545b71af07`  
		Last Modified: Wed, 24 Jun 2026 01:38:26 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:727a7c3d7db116a9083c73db7814b14298833e288dfe966f888001a02e7a2d89`  
		Last Modified: Tue, 30 Jun 2026 19:09:55 GMT  
		Size: 1.3 MB (1289486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b660c36e89368f072cb4545d28bf5d1228649e5d1cf37fb1bb77de5035826710`  
		Last Modified: Tue, 30 Jun 2026 19:09:55 GMT  
		Size: 421.7 KB (421724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a32e3548133b65ce21bd0805013e920e0c049699c480bfa7a7257c7728954628`  
		Last Modified: Tue, 30 Jun 2026 19:09:55 GMT  
		Size: 7.5 KB (7478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12525d349e996a4536a59ccd115e6e84f814c81baf675cc4636ca31cf425fe7e`  
		Last Modified: Tue, 30 Jun 2026 19:09:55 GMT  
		Size: 2.6 MB (2603499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dab36dc7bdfc81dfb259055b46640cc280f2c9148ba316d4287f362b113c8db3`  
		Last Modified: Tue, 30 Jun 2026 19:09:56 GMT  
		Size: 1.7 KB (1652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59e417775ad35721c5d1310ba082ea7d9d58bcd944b6e20a8145e70e2e719527`  
		Last Modified: Tue, 30 Jun 2026 19:09:56 GMT  
		Size: 823.3 KB (823341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac9be44e7e5f7ce21535ddd242bbbe2e5c58c706fc50192df5c408a34c8b9806`  
		Last Modified: Tue, 30 Jun 2026 19:09:57 GMT  
		Size: 23.1 MB (23136851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:4-apache` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:a6fd4acddb6c27bec168992f4d58b29d8b9f2366a0c7ce8174ac2ed15a10a1e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 KB (50153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f12ec823357ae93c68ddf81dc20b8099342f55b562fe520f3d60613238131024`

```dockerfile
```

-	Layers:
	-	`sha256:f89f6b5c6c83c079d0c1925480867fa8d48488e11a4b4d722d82294d1dc35d9b`  
		Last Modified: Tue, 30 Jun 2026 19:09:54 GMT  
		Size: 50.2 KB (50153 bytes)  
		MIME: application/vnd.in-toto+json

### `postfixadmin:4-apache` - linux; arm64 variant v8

```console
$ docker pull postfixadmin@sha256:d7e0df8f1ef5a2c1eb18206f258363895705fb78ffe4fa209ed756ff14727348
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.4 MB (197440086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41f5e697be3fe179892bb94030cb713aeb28081758b70b6a828692b1522863e5`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:22:41 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 24 Jun 2026 01:22:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 24 Jun 2026 01:22:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Wed, 24 Jun 2026 01:22:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 24 Jun 2026 01:22:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 24 Jun 2026 01:22:58 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 24 Jun 2026 01:22:58 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 24 Jun 2026 01:23:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 24 Jun 2026 01:23:04 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 24 Jun 2026 01:23:05 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 24 Jun 2026 01:23:05 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Jun 2026 01:23:05 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Jun 2026 01:23:05 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 24 Jun 2026 01:23:05 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 24 Jun 2026 01:23:05 GMT
ENV PHP_VERSION=8.3.31
# Wed, 24 Jun 2026 01:23:05 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.31.tar.xz.asc
# Wed, 24 Jun 2026 01:23:05 GMT
ENV PHP_SHA256=66410cee07f4b2baeb0843140bb2a2b52ef930b5cf9b3d6e6d158b33aae8fa37
# Wed, 24 Jun 2026 01:27:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 24 Jun 2026 01:27:15 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:31:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 24 Jun 2026 01:31:09 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:31:09 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 24 Jun 2026 01:31:09 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 24 Jun 2026 01:31:09 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 24 Jun 2026 01:31:09 GMT
STOPSIGNAL SIGWINCH
# Wed, 24 Jun 2026 01:31:09 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:31:09 GMT
WORKDIR /var/www/html
# Wed, 24 Jun 2026 01:31:09 GMT
EXPOSE map[80/tcp:{}]
# Wed, 24 Jun 2026 01:31:09 GMT
CMD ["apache2-foreground"]
# Tue, 30 Jun 2026 19:07:42 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Tue, 30 Jun 2026 19:07:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		gosu 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Jun 2026 19:08:04 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libpq-dev 		libsqlite3-dev 	; 	docker-php-ext-install -j "$(nproc)" 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -rt apt-mark manual; 			apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean # buildkit
# Tue, 30 Jun 2026 19:08:04 GMT
ARG POSTFIXADMIN_VERSION=4.0.4
# Tue, 30 Jun 2026 19:08:04 GMT
ARG POSTFIXADMIN_SHA512=cce293e92e03f06a20ddbe09a9faec251af3f166f38565429d791feaf832096344a62656bab2a60bbd360545c1a0bd3ed05e11f4a4e46f04858e84639c5391dd
# Tue, 30 Jun 2026 19:08:04 GMT
ENV POSTFIXADMIN_VERSION=4.0.4
# Tue, 30 Jun 2026 19:08:04 GMT
ENV POSTFIXADMIN_SHA512=cce293e92e03f06a20ddbe09a9faec251af3f166f38565429d791feaf832096344a62656bab2a60bbd360545c1a0bd3ed05e11f4a4e46f04858e84639c5391dd
# Tue, 30 Jun 2026 19:08:04 GMT
ENV APACHE_DOCUMENT_ROOT=/var/www/html/public
# Tue, 30 Jun 2026 19:08:04 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.4 POSTFIXADMIN_SHA512=cce293e92e03f06a20ddbe09a9faec251af3f166f38565429d791feaf832096344a62656bab2a60bbd360545c1a0bd3ed05e11f4a4e46f04858e84639c5391dd
RUN set -eu; sed -ri -e 's!/var/www/html!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/sites-available/*.conf; 	sed -ri -e 's!/var/www/!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/apache2.conf /etc/apache2/conf-available/*.conf # buildkit
# Tue, 30 Jun 2026 19:08:04 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.4 POSTFIXADMIN_SHA512=cce293e92e03f06a20ddbe09a9faec251af3f166f38565429d791feaf832096344a62656bab2a60bbd360545c1a0bd3ed05e11f4a4e46f04858e84639c5391dd
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/v${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin # buildkit
# Tue, 30 Jun 2026 19:08:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Jun 2026 19:08:05 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 30 Jun 2026 19:08:05 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 30 Jun 2026 19:08:13 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.4 POSTFIXADMIN_SHA512=cce293e92e03f06a20ddbe09a9faec251af3f166f38565429d791feaf832096344a62656bab2a60bbd360545c1a0bd3ed05e11f4a4e46f04858e84639c5391dd
RUN set -eux; 	composerDeps=" 		unzip 	"; 	apt-get update; 	apt-get install -y --no-install-recommends $composerDeps; 		export COMPOSER_HOME="$(mktemp -d)"; 	composer install --ignore-platform-req=ext-mysqli --no-dev --no-interaction --working-dir /usr/src/postfixadmin; 	rm -rf "$COMPOSER_HOME"; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $composerDeps; 	apt-get dist-clean # buildkit
# Tue, 30 Jun 2026 19:08:13 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Tue, 30 Jun 2026 19:08:13 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:3be819c1c8cfde074541a1d875fbf2da3642b0ec6bb39aaa2ce7d56052b67dc1`  
		Last Modified: Wed, 24 Jun 2026 00:28:21 GMT  
		Size: 30.1 MB (30148551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d1374a0ef411e23f39e123da8d8b4439bfa330f7116dd896d85bdf25560095b`  
		Last Modified: Wed, 24 Jun 2026 01:26:56 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28ee031e0fccdc1b9ec467a6d402045bf1257008376fb9c95f1e4f46d1c11244`  
		Last Modified: Wed, 24 Jun 2026 01:26:59 GMT  
		Size: 110.2 MB (110169060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e85c2e4328f23ef330e5af53c366ea3c1ef744a67006663d77538a4f1c5cfd4b`  
		Last Modified: Wed, 24 Jun 2026 01:26:56 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e4e0d05850528570ff315c975a855e0f114092424753331408b0302bb1ba8f`  
		Last Modified: Wed, 24 Jun 2026 01:26:56 GMT  
		Size: 4.3 MB (4308356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39728b1574c3cc4fc28c7221d4d9efa2d2f33a74dafeb75a3b172f56fc55eed6`  
		Last Modified: Wed, 24 Jun 2026 01:26:57 GMT  
		Size: 426.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae371a8d303dbf3675fe9cd1953f38072b5bc2202cee63848f569847b4a9ed32`  
		Last Modified: Wed, 24 Jun 2026 01:26:58 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91df8badda595f6df054cbd5f996245db2286e475f1bfda5eac1d2fabdeb0ea3`  
		Last Modified: Wed, 24 Jun 2026 01:31:21 GMT  
		Size: 12.8 MB (12769745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef6b80bc0c9c2fe27c4089a2c60c80739f28a015817dc538fe5663ba6273da51`  
		Last Modified: Wed, 24 Jun 2026 01:31:20 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca5dc5d90935fd3955ad56945f847a9144c4b33f216f6a2bf6b54270c16273a`  
		Last Modified: Wed, 24 Jun 2026 01:31:21 GMT  
		Size: 11.7 MB (11734808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:570ef4bf2de11ce87e16389a4a16003275a410819a315c552a88dda0c3e7c7f2`  
		Last Modified: Wed, 24 Jun 2026 01:31:20 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81df943c2d3567af8fec236d8ccff92811b9a0a2d2939a15e6a1aa71cb228e66`  
		Last Modified: Wed, 24 Jun 2026 01:31:22 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5757cb928f795d8beab1316be03545ba0caf9cee0cf6b893edb973fa8c1a260`  
		Last Modified: Wed, 24 Jun 2026 01:31:22 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d675ea6715f2b5fcc3a65edd7f104b421d0ed1b48ed482eb6946573ca98ea1a9`  
		Last Modified: Wed, 24 Jun 2026 01:31:23 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa320d5e5e941b34e58aaa40a9397941ee3e077b2388f3bdfecd7d4084b84d1d`  
		Last Modified: Tue, 30 Jun 2026 19:08:20 GMT  
		Size: 1.3 MB (1266135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296582a00edd520d5e946d5138be84ea94b168ce60703760d1f1c920b142516b`  
		Last Modified: Tue, 30 Jun 2026 19:08:20 GMT  
		Size: 462.8 KB (462777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e86bdf3c925869fcd6ef4ad1b6e91ed4c0c4d3189987d9a5fcedb9e6a957092`  
		Last Modified: Tue, 30 Jun 2026 19:08:20 GMT  
		Size: 7.5 KB (7478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75dfc14bfbeed96d4b62ce162ca23f8eb96ce10961ce20061d711d471a6a2179`  
		Last Modified: Tue, 30 Jun 2026 19:08:20 GMT  
		Size: 2.6 MB (2603507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d46a0da9a2f81e4bbec6c727ac6473f85644b2b438826e9d1f6bfe7e21208a5`  
		Last Modified: Tue, 30 Jun 2026 19:08:21 GMT  
		Size: 1.7 KB (1656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1934de52bd5451aaafa8fc0b31bca2e60a0b21f9b9f416731f1a17d6052a1367`  
		Last Modified: Tue, 30 Jun 2026 19:08:22 GMT  
		Size: 823.3 KB (823347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8152aecce86237886ea9ae15300e34e1d8737f431aa4e42aebc97be43b1f3997`  
		Last Modified: Tue, 30 Jun 2026 19:08:22 GMT  
		Size: 23.1 MB (23138946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:4-apache` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:b0163db504f13f6ff8d5aa7f50add92575eeee543ee2e86fd0fc339902d1c41b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 KB (50213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6496d4d24279d5053fa2d76f40985d85efc50dbc00d5cf015882418a7e4a4a80`

```dockerfile
```

-	Layers:
	-	`sha256:d2f24b7b448ee48a93654364784280fad033bab250ade2c584b74dcb4f46369e`  
		Last Modified: Tue, 30 Jun 2026 19:08:19 GMT  
		Size: 50.2 KB (50213 bytes)  
		MIME: application/vnd.in-toto+json

### `postfixadmin:4-apache` - linux; 386

```console
$ docker pull postfixadmin@sha256:98701e76228170517721b8abd94a1137fce02cd55ccd5d44c6aa952b11656c26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.0 MB (204974493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4d98c750c3b03fb78dbfeb2779026b5c42ceffde6f9d11e7551d289f57512fd`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:25:05 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 24 Jun 2026 01:25:25 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 24 Jun 2026 01:25:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Wed, 24 Jun 2026 01:25:25 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 24 Jun 2026 01:25:25 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 24 Jun 2026 01:25:25 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 24 Jun 2026 01:25:25 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 24 Jun 2026 01:25:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 24 Jun 2026 01:25:33 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 24 Jun 2026 01:25:34 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 24 Jun 2026 01:25:34 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Jun 2026 01:25:34 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Jun 2026 01:25:34 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 24 Jun 2026 01:25:34 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 24 Jun 2026 01:25:34 GMT
ENV PHP_VERSION=8.3.31
# Wed, 24 Jun 2026 01:25:34 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.31.tar.xz.asc
# Wed, 24 Jun 2026 01:25:34 GMT
ENV PHP_SHA256=66410cee07f4b2baeb0843140bb2a2b52ef930b5cf9b3d6e6d158b33aae8fa37
# Wed, 24 Jun 2026 01:25:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 24 Jun 2026 01:25:43 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:28:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 24 Jun 2026 01:28:37 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:28:37 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 24 Jun 2026 01:28:37 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 24 Jun 2026 01:28:37 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 24 Jun 2026 01:28:37 GMT
STOPSIGNAL SIGWINCH
# Wed, 24 Jun 2026 01:28:37 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:28:37 GMT
WORKDIR /var/www/html
# Wed, 24 Jun 2026 01:28:37 GMT
EXPOSE map[80/tcp:{}]
# Wed, 24 Jun 2026 01:28:37 GMT
CMD ["apache2-foreground"]
# Tue, 30 Jun 2026 19:08:19 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Tue, 30 Jun 2026 19:08:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		gosu 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Jun 2026 19:08:42 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libpq-dev 		libsqlite3-dev 	; 	docker-php-ext-install -j "$(nproc)" 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -rt apt-mark manual; 			apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean # buildkit
# Tue, 30 Jun 2026 19:08:42 GMT
ARG POSTFIXADMIN_VERSION=4.0.4
# Tue, 30 Jun 2026 19:08:42 GMT
ARG POSTFIXADMIN_SHA512=cce293e92e03f06a20ddbe09a9faec251af3f166f38565429d791feaf832096344a62656bab2a60bbd360545c1a0bd3ed05e11f4a4e46f04858e84639c5391dd
# Tue, 30 Jun 2026 19:08:42 GMT
ENV POSTFIXADMIN_VERSION=4.0.4
# Tue, 30 Jun 2026 19:08:42 GMT
ENV POSTFIXADMIN_SHA512=cce293e92e03f06a20ddbe09a9faec251af3f166f38565429d791feaf832096344a62656bab2a60bbd360545c1a0bd3ed05e11f4a4e46f04858e84639c5391dd
# Tue, 30 Jun 2026 19:08:42 GMT
ENV APACHE_DOCUMENT_ROOT=/var/www/html/public
# Tue, 30 Jun 2026 19:08:42 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.4 POSTFIXADMIN_SHA512=cce293e92e03f06a20ddbe09a9faec251af3f166f38565429d791feaf832096344a62656bab2a60bbd360545c1a0bd3ed05e11f4a4e46f04858e84639c5391dd
RUN set -eu; sed -ri -e 's!/var/www/html!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/sites-available/*.conf; 	sed -ri -e 's!/var/www/!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/apache2.conf /etc/apache2/conf-available/*.conf # buildkit
# Tue, 30 Jun 2026 19:08:42 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.4 POSTFIXADMIN_SHA512=cce293e92e03f06a20ddbe09a9faec251af3f166f38565429d791feaf832096344a62656bab2a60bbd360545c1a0bd3ed05e11f4a4e46f04858e84639c5391dd
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/v${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin # buildkit
# Tue, 30 Jun 2026 19:08:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Jun 2026 19:08:42 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 30 Jun 2026 19:08:42 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 30 Jun 2026 19:08:51 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.4 POSTFIXADMIN_SHA512=cce293e92e03f06a20ddbe09a9faec251af3f166f38565429d791feaf832096344a62656bab2a60bbd360545c1a0bd3ed05e11f4a4e46f04858e84639c5391dd
RUN set -eux; 	composerDeps=" 		unzip 	"; 	apt-get update; 	apt-get install -y --no-install-recommends $composerDeps; 		export COMPOSER_HOME="$(mktemp -d)"; 	composer install --ignore-platform-req=ext-mysqli --no-dev --no-interaction --working-dir /usr/src/postfixadmin; 	rm -rf "$COMPOSER_HOME"; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $composerDeps; 	apt-get dist-clean # buildkit
# Tue, 30 Jun 2026 19:08:51 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Tue, 30 Jun 2026 19:08:51 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:984d3baa100eb8c4d7c83b7c23b4748e508aa6ed5903297f02be90a681f52d41`  
		Last Modified: Wed, 24 Jun 2026 00:28:38 GMT  
		Size: 31.3 MB (31301210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ef928af4a107d8dfa4981183977c4b41e803afeb1e1229e8af5999dddbdf7bd`  
		Last Modified: Wed, 24 Jun 2026 01:28:58 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4bf495b2e58667f07cb8809ac0edb8289cf9e7fcb355a17e0223f1597451ac2`  
		Last Modified: Wed, 24 Jun 2026 01:29:01 GMT  
		Size: 116.1 MB (116142394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0af40e0db6604edee4696ac451ed4f4c5844b6ac430a7d8af0e221c7448db15b`  
		Last Modified: Wed, 24 Jun 2026 01:28:58 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51630058c21a058f3945888fe6a86b6eb9d9d5833f6c5bb5e4fc7977f2a4e809`  
		Last Modified: Wed, 24 Jun 2026 01:28:59 GMT  
		Size: 4.5 MB (4459137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5309713240b69d88483e487e7da27f792f77729f7b03b3663a1f9ea3ac3c8247`  
		Last Modified: Wed, 24 Jun 2026 01:29:00 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:899f4a21bb6fb8d8f18cdc225380a7d6abcc47b8ecfd3cf1f9a8542c3ae5b7c7`  
		Last Modified: Wed, 24 Jun 2026 01:28:59 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eab1c41a2d13447b76beeac5d8d99dfcd7a77060483599b593096199a249f9e`  
		Last Modified: Wed, 24 Jun 2026 01:29:01 GMT  
		Size: 12.8 MB (12769151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:964f5f1e919d2517539fb0b1af7fced6fad51184cb3dce9805026b82db876fa4`  
		Last Modified: Wed, 24 Jun 2026 01:29:01 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe0d15e688d1b61d2141ae4bed18b13ae51d4fc1aa60f74cfa9df5b67e567700`  
		Last Modified: Wed, 24 Jun 2026 01:29:01 GMT  
		Size: 11.9 MB (11928972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2807577caceda16ef7dfef2f4f54d994a276de7b2e9f3b82ccd75d36c47692ee`  
		Last Modified: Wed, 24 Jun 2026 01:29:02 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44cf00dabe535c65ae4c7d0ada7809544db4f74c4c766a5af3843ab8a36437ea`  
		Last Modified: Wed, 24 Jun 2026 01:29:03 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c86c4934d8929f583791d02440c140db6cae447b568068feeffe934fc6027e75`  
		Last Modified: Wed, 24 Jun 2026 01:29:03 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb6ccbcd2fa4d5586d396b4d2c0d4f46b9aa6b6a39ed491ee8f7220c6e2fffd9`  
		Last Modified: Wed, 24 Jun 2026 01:29:04 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a89a8f2a917e0c007bf053bb16248fa46d0e423fe50076abf77578c05c7ae43`  
		Last Modified: Tue, 30 Jun 2026 19:08:58 GMT  
		Size: 1.3 MB (1311121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14e9659a9e6d0e179ca9cd8dfab88193fc2d4044ab3fb48bbd15a56522191870`  
		Last Modified: Tue, 30 Jun 2026 19:08:58 GMT  
		Size: 482.6 KB (482623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea0f72958755187eedf853accdd5231ecd34962e383170faf85ac26d9b76f419`  
		Last Modified: Tue, 30 Jun 2026 19:08:57 GMT  
		Size: 7.5 KB (7478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da6d1a1ab64f11c3a6522b9efb4e3fee9aa21abb2a967999e277ff4e7f47a61`  
		Last Modified: Tue, 30 Jun 2026 19:08:58 GMT  
		Size: 2.6 MB (2603505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e4657c0fc7c72a9845a029848fd8109d15112134fd7aa4a72aa046ddac8c02f`  
		Last Modified: Tue, 30 Jun 2026 19:08:59 GMT  
		Size: 1.7 KB (1656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dab7be48b703047487043b9c82fb34c35312271f8ee93cb0e99116b8fbf3fb0`  
		Last Modified: Tue, 30 Jun 2026 19:08:59 GMT  
		Size: 823.3 KB (823345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:209747bd921fdf2a41c5a414f25d4ae13740d7ed07a3fe2e40ea180d75e0b6a8`  
		Last Modified: Tue, 30 Jun 2026 19:09:00 GMT  
		Size: 23.1 MB (23138168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:4-apache` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:bc9230660bb45c464566d9b0b3e8a971f8d8bff7e743eba1bdb35abf5d40c6fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 KB (49907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4637fb04d644ff57c5f817715aca8abde1a26d4377f53cba9bfdded58175d463`

```dockerfile
```

-	Layers:
	-	`sha256:f86748033f636258d468adbb89ea3ce79ea0cadcafb2172462746018f22d3356`  
		Last Modified: Tue, 30 Jun 2026 19:08:57 GMT  
		Size: 49.9 KB (49907 bytes)  
		MIME: application/vnd.in-toto+json

### `postfixadmin:4-apache` - linux; ppc64le

```console
$ docker pull postfixadmin@sha256:17d6bdfcbe1712ce6e161d78c829ee326b90ade16b739efd62b4a623a06b85d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.3 MB (201333348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1613d284e88210fe3ba7a5b9dd1b057dc150f1c81cf419f4a18b0b3ef3e02f2c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:47:53 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 24 Jun 2026 01:48:31 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 24 Jun 2026 01:48:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Wed, 24 Jun 2026 01:48:31 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 24 Jun 2026 01:48:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 24 Jun 2026 01:48:32 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 24 Jun 2026 01:48:32 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 24 Jun 2026 01:50:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 24 Jun 2026 01:50:58 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 24 Jun 2026 01:50:59 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 24 Jun 2026 01:50:59 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Jun 2026 01:50:59 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Jun 2026 01:50:59 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 24 Jun 2026 01:50:59 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 24 Jun 2026 01:50:59 GMT
ENV PHP_VERSION=8.3.31
# Wed, 24 Jun 2026 01:50:59 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.31.tar.xz.asc
# Wed, 24 Jun 2026 01:50:59 GMT
ENV PHP_SHA256=66410cee07f4b2baeb0843140bb2a2b52ef930b5cf9b3d6e6d158b33aae8fa37
# Wed, 24 Jun 2026 02:29:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 24 Jun 2026 02:29:06 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 02:33:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 24 Jun 2026 02:33:01 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 02:33:01 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 24 Jun 2026 02:33:02 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 24 Jun 2026 02:33:02 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 24 Jun 2026 02:33:02 GMT
STOPSIGNAL SIGWINCH
# Wed, 24 Jun 2026 02:33:04 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 02:33:04 GMT
WORKDIR /var/www/html
# Wed, 24 Jun 2026 02:33:04 GMT
EXPOSE map[80/tcp:{}]
# Wed, 24 Jun 2026 02:33:04 GMT
CMD ["apache2-foreground"]
# Tue, 30 Jun 2026 19:06:54 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Tue, 30 Jun 2026 19:06:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		gosu 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Jun 2026 19:07:36 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libpq-dev 		libsqlite3-dev 	; 	docker-php-ext-install -j "$(nproc)" 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -rt apt-mark manual; 			apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean # buildkit
# Tue, 30 Jun 2026 19:07:36 GMT
ARG POSTFIXADMIN_VERSION=4.0.4
# Tue, 30 Jun 2026 19:07:36 GMT
ARG POSTFIXADMIN_SHA512=cce293e92e03f06a20ddbe09a9faec251af3f166f38565429d791feaf832096344a62656bab2a60bbd360545c1a0bd3ed05e11f4a4e46f04858e84639c5391dd
# Tue, 30 Jun 2026 19:07:36 GMT
ENV POSTFIXADMIN_VERSION=4.0.4
# Tue, 30 Jun 2026 19:07:36 GMT
ENV POSTFIXADMIN_SHA512=cce293e92e03f06a20ddbe09a9faec251af3f166f38565429d791feaf832096344a62656bab2a60bbd360545c1a0bd3ed05e11f4a4e46f04858e84639c5391dd
# Tue, 30 Jun 2026 19:07:36 GMT
ENV APACHE_DOCUMENT_ROOT=/var/www/html/public
# Tue, 30 Jun 2026 19:07:38 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.4 POSTFIXADMIN_SHA512=cce293e92e03f06a20ddbe09a9faec251af3f166f38565429d791feaf832096344a62656bab2a60bbd360545c1a0bd3ed05e11f4a4e46f04858e84639c5391dd
RUN set -eu; sed -ri -e 's!/var/www/html!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/sites-available/*.conf; 	sed -ri -e 's!/var/www/!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/apache2.conf /etc/apache2/conf-available/*.conf # buildkit
# Tue, 30 Jun 2026 19:07:49 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.4 POSTFIXADMIN_SHA512=cce293e92e03f06a20ddbe09a9faec251af3f166f38565429d791feaf832096344a62656bab2a60bbd360545c1a0bd3ed05e11f4a4e46f04858e84639c5391dd
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/v${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin # buildkit
# Tue, 30 Jun 2026 19:07:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Jun 2026 19:07:50 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 30 Jun 2026 19:07:50 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 30 Jun 2026 19:08:04 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.4 POSTFIXADMIN_SHA512=cce293e92e03f06a20ddbe09a9faec251af3f166f38565429d791feaf832096344a62656bab2a60bbd360545c1a0bd3ed05e11f4a4e46f04858e84639c5391dd
RUN set -eux; 	composerDeps=" 		unzip 	"; 	apt-get update; 	apt-get install -y --no-install-recommends $composerDeps; 		export COMPOSER_HOME="$(mktemp -d)"; 	composer install --ignore-platform-req=ext-mysqli --no-dev --no-interaction --working-dir /usr/src/postfixadmin; 	rm -rf "$COMPOSER_HOME"; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $composerDeps; 	apt-get dist-clean # buildkit
# Tue, 30 Jun 2026 19:08:04 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Tue, 30 Jun 2026 19:08:04 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:639e1c13483ea279c94219be2736856262d8dd2efeff3e6d309f11a66aba21fb`  
		Last Modified: Wed, 24 Jun 2026 00:30:29 GMT  
		Size: 33.6 MB (33606388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a64e77efe72bf9ab01112d6628b561df155e58c8abb9a5c50ca8c3c2d3054015`  
		Last Modified: Wed, 24 Jun 2026 01:53:55 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5a885bf66539705f27716480915d14f847c62afd59e7c77b0d7a2ec11fcf9f8`  
		Last Modified: Wed, 24 Jun 2026 01:53:59 GMT  
		Size: 109.6 MB (109598576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6270c259f3728f03e6c19bf8bc89dd6cfe4f6a02bdbe4c4a66ac81d4e83afc0f`  
		Last Modified: Wed, 24 Jun 2026 01:53:55 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cae69c11420255e2fb44bd4bb296ef90cc67414114637c79ac02fd2c37fbabf`  
		Last Modified: Wed, 24 Jun 2026 01:56:17 GMT  
		Size: 4.9 MB (4883625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85e59412a7fe8dbc45f29a87ef3523b22b2adb88633ffeaf709f79d061da843d`  
		Last Modified: Wed, 24 Jun 2026 01:56:17 GMT  
		Size: 436.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:836531defa102246f748656c2699b26aa90b6d91ae2eb76b5c0af7192847128c`  
		Last Modified: Wed, 24 Jun 2026 01:56:16 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:788c0dfdc7d988ee818ed1664dc9196837395b960e748a2e7e83ea5935c77bfd`  
		Last Modified: Wed, 24 Jun 2026 02:33:27 GMT  
		Size: 12.8 MB (12769181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af6ab6f632457cfbd24e6f80a5cdca364b5d907f54d52d8e63069bc6ef1057c0`  
		Last Modified: Wed, 24 Jun 2026 02:33:26 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8604b5169845cfd02ae72d9c89f14ea5702a0ca0d731ae9a603fcc8e42b5750b`  
		Last Modified: Wed, 24 Jun 2026 02:33:27 GMT  
		Size: 12.1 MB (12125096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4d024c5146fb40988386f91917c3b1cdfe073d8172940ed55a5279f066a20fe`  
		Last Modified: Wed, 24 Jun 2026 02:33:26 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb04e288077024cc1818a261e6e00f85dd981c14c980e6b4ec22d6c71211aa36`  
		Last Modified: Wed, 24 Jun 2026 02:33:27 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:901e590e4a19b203889dc2cab221bb80cbf5aa933ea1e97316be2ebae7d0123a`  
		Last Modified: Wed, 24 Jun 2026 02:33:27 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04681538d424258f9bed596e8d88f0a4cc5124832dd5bbd4fbc7ce0a970cb478`  
		Last Modified: Wed, 24 Jun 2026 02:33:28 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30ffde7fa5f9b2170f7f3e9aed4e9216e6b9dd518d359b50609f42fec17c6f3c`  
		Last Modified: Tue, 30 Jun 2026 19:08:17 GMT  
		Size: 1.3 MB (1268491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc0b1af4dfdf42f2b2c7584f3abd3f540238be3c9404ed7cd454e12726a1878c`  
		Last Modified: Tue, 30 Jun 2026 19:08:17 GMT  
		Size: 501.8 KB (501772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:589214fa4971dadfba1d95a3fd8d5f71cc6866f22de5336a458e247baed11537`  
		Last Modified: Tue, 30 Jun 2026 19:08:17 GMT  
		Size: 7.5 KB (7480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78e4b12ebb5b150f3b0f89ab92a80859ca829c40bbf8d66427401d86c086f82a`  
		Last Modified: Tue, 30 Jun 2026 19:08:17 GMT  
		Size: 2.6 MB (2603510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1f067f3033aa32c2e77f3c2323b66cfddddd5bbd2f15f2736ad366994c9104e`  
		Last Modified: Tue, 30 Jun 2026 19:08:18 GMT  
		Size: 1.7 KB (1658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ad16d6c021d23ab2643696b6d7467b83935e20520e3777a276907fd17206919`  
		Last Modified: Tue, 30 Jun 2026 19:08:18 GMT  
		Size: 823.3 KB (823344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:005aed404e47cd2135a179b33afeebee53c53eca42ff5b07a33239a94004e839`  
		Last Modified: Tue, 30 Jun 2026 19:08:19 GMT  
		Size: 23.1 MB (23138477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:4-apache` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:4573ce4bcd31c0890afc5b86052cc07ce673f6530804b4d6f8bd6c420c7525bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 KB (50061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95f421bac61ae552773d8a4665a2c546ab1f471ceafaa157acac27881394d91f`

```dockerfile
```

-	Layers:
	-	`sha256:19f5d2def2f3a76bc849df4167817221168054710aba6ac77993b6999189c6f9`  
		Last Modified: Tue, 30 Jun 2026 19:08:16 GMT  
		Size: 50.1 KB (50061 bytes)  
		MIME: application/vnd.in-toto+json

### `postfixadmin:4-apache` - linux; riscv64

```console
$ docker pull postfixadmin@sha256:27c1266009d0a89f68d378b1b1d39db3cb45c65dd7b22cfdb0720a0d5e096f6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.5 MB (231526729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b137c68a3e4a70114c8f29b15ca076afa08b75dc4986b1e0600c394b546d81e1`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 11:59:43 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 20 May 2026 12:01:47 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 20 May 2026 12:01:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 12:01:47 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 20 May 2026 12:01:47 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 20 May 2026 12:01:47 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 20 May 2026 12:01:47 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 20 May 2026 13:07:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 20 May 2026 13:07:17 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 20 May 2026 13:07:18 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 20 May 2026 13:07:18 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 20 May 2026 13:07:18 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 20 May 2026 13:07:18 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 20 May 2026 13:07:18 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 20 May 2026 13:07:18 GMT
ENV PHP_VERSION=8.3.31
# Wed, 20 May 2026 13:07:18 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.31.tar.xz.asc
# Wed, 20 May 2026 13:07:18 GMT
ENV PHP_SHA256=66410cee07f4b2baeb0843140bb2a2b52ef930b5cf9b3d6e6d158b33aae8fa37
# Wed, 20 May 2026 20:49:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 20 May 2026 20:49:04 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 20 May 2026 21:38:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 20 May 2026 21:38:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 20 May 2026 21:38:29 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 20 May 2026 21:38:30 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 20 May 2026 21:38:30 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 20 May 2026 21:38:30 GMT
STOPSIGNAL SIGWINCH
# Wed, 20 May 2026 21:38:30 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 20 May 2026 21:38:30 GMT
WORKDIR /var/www/html
# Wed, 20 May 2026 21:38:30 GMT
EXPOSE map[80/tcp:{}]
# Wed, 20 May 2026 21:38:30 GMT
CMD ["apache2-foreground"]
# Fri, 29 May 2026 01:09:57 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Fri, 29 May 2026 01:09:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		gosu 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 29 May 2026 01:14:06 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libpq-dev 		libsqlite3-dev 	; 	docker-php-ext-install -j "$(nproc)" 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -rt apt-mark manual; 			apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean # buildkit
# Fri, 29 May 2026 01:14:06 GMT
ARG POSTFIXADMIN_VERSION=4.0.1
# Fri, 29 May 2026 01:14:06 GMT
ARG POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
# Fri, 29 May 2026 01:14:06 GMT
ENV POSTFIXADMIN_VERSION=4.0.1
# Fri, 29 May 2026 01:14:06 GMT
ENV POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
# Fri, 29 May 2026 01:14:06 GMT
ENV APACHE_DOCUMENT_ROOT=/var/www/html/public
# Fri, 29 May 2026 01:14:06 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.1 POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
RUN set -eu; sed -ri -e 's!/var/www/html!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/sites-available/*.conf; 	sed -ri -e 's!/var/www/!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/apache2.conf /etc/apache2/conf-available/*.conf # buildkit
# Fri, 29 May 2026 01:14:09 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.1 POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/v${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin # buildkit
# Thu, 04 Jun 2026 20:34:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 20:34:22 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 20:34:22 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 04 Jun 2026 20:35:41 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.1 POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
RUN set -eux; 	composerDeps=" 		unzip 	"; 	apt-get update; 	apt-get install -y --no-install-recommends $composerDeps; 		export COMPOSER_HOME="$(mktemp -d)"; 	composer install --ignore-platform-req=ext-mysqli --no-dev --no-interaction --working-dir /usr/src/postfixadmin; 	rm -rf "$COMPOSER_HOME"; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $composerDeps; 	apt-get dist-clean # buildkit
# Thu, 04 Jun 2026 20:35:41 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Thu, 04 Jun 2026 20:35:41 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:58bbe80817efb8a686096088d2ce9bfdbe0120904c9ea14d905c0e6d847d3ffd`  
		Last Modified: Tue, 19 May 2026 23:51:26 GMT  
		Size: 28.3 MB (28277598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed3f1ce6bdb422619d5f28f3d354ac88efadf525446aa4cc0a2cf6d208358da0`  
		Last Modified: Wed, 20 May 2026 13:05:09 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2278d8aba6744e8388864d93d2ccd060b4b5b706da0855420292afc7562eef8`  
		Last Modified: Wed, 20 May 2026 13:05:36 GMT  
		Size: 146.6 MB (146584901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f680f6a3aa4a44306703b8a92e46d186729d6e1435771fbfda06e18de5ebcc5`  
		Last Modified: Wed, 20 May 2026 13:05:09 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:887cf26ec25a917a3969775023d91d64e52e0fc30b0f1e2c5a326ce664b36942`  
		Last Modified: Wed, 20 May 2026 14:08:12 GMT  
		Size: 4.0 MB (4031581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e116995318a8f16f6dd281e40820dba3f5cec3ccbf8b001b5f77cc47621731c`  
		Last Modified: Wed, 20 May 2026 14:08:10 GMT  
		Size: 436.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e72c0690c9ca74d867f3cd4b9dd3884b132b21d1a7e60c2dfcd33fecaa0fb76f`  
		Last Modified: Wed, 20 May 2026 14:08:10 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f141c427a46f1759713dd715f2b2791ede42c5999242efd0c63766804280c65`  
		Last Modified: Wed, 20 May 2026 21:41:36 GMT  
		Size: 12.8 MB (12784261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee06ce4dcedcd83bfb671ba90b0f3a5d9864ea66e2df3c3fc9863439f06e844b`  
		Last Modified: Wed, 20 May 2026 21:41:31 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34c074bd4815919a1ea293f5d0e9860a75d0d85a8517f686b8d664ab6b9884b4`  
		Last Modified: Wed, 20 May 2026 21:41:36 GMT  
		Size: 11.3 MB (11255979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3e03a1d9fb0c37e61eb1dbf72bc1a8cd205940124bf0f4d6a16857c6e59c7a4`  
		Last Modified: Wed, 20 May 2026 21:41:31 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f503077b0fb46c4efc42977e7d8e3dc3c5652f85e40d21d688e0bd5cc48806b`  
		Last Modified: Wed, 20 May 2026 21:41:34 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885921ea102fba979369e756898326a8244f68e27534c75bb87792e5d7cbbea8`  
		Last Modified: Wed, 20 May 2026 21:41:34 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa6b617233e6367ce4f70f391ff5cc68c4d273f816494a37326f5f6e80607a0f`  
		Last Modified: Wed, 20 May 2026 21:41:35 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9bf3b909767751dce0485dc66ea189ddf329f13096f995fea859472ee640aaa`  
		Last Modified: Fri, 29 May 2026 01:16:44 GMT  
		Size: 1.3 MB (1265668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ff01a38143a485d9a552b333b75e6c09ba7d68d88c5060773635ce7dc2264b`  
		Last Modified: Fri, 29 May 2026 01:16:44 GMT  
		Size: 456.1 KB (456090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7660bccae2e00f7bd4403114dc85245aad95c494fcfce6757ff3992625b13ea`  
		Last Modified: Fri, 29 May 2026 01:16:44 GMT  
		Size: 7.5 KB (7480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b019cd275d7f205e563e59d695c2a63afc524533d9222786f4ee2b0ff1c89c59`  
		Last Modified: Fri, 29 May 2026 01:16:45 GMT  
		Size: 2.6 MB (2602184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbaf21b7e9ddcf61185d8d8719bdf00d222b60f84732b59e9697fdf72c0c2fbd`  
		Last Modified: Thu, 04 Jun 2026 20:36:53 GMT  
		Size: 1.7 KB (1656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cede4bd0ae532b8cfce8639d3fcb15069baaef17d29291ad63b3a0e53431a6c`  
		Last Modified: Thu, 04 Jun 2026 20:36:53 GMT  
		Size: 823.3 KB (823345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:381b768b6bc3c4e727395fef901eea315c3df91e251d2ca6a1fbcf7dae2201ca`  
		Last Modified: Thu, 04 Jun 2026 20:36:57 GMT  
		Size: 23.4 MB (23430237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:4-apache` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:eca3a194b2fe170d130e57a4aeaf1158d2e7e8e5bb58bf3a5f29c5e02f37abe2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 KB (50061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9c7add5b6e2ac6a8d571b7a36713a8c1853d2d484ce3f82482bac2660368cdf`

```dockerfile
```

-	Layers:
	-	`sha256:875ab7d38e79503d3cb3f74840298e33831253120b7190df6bc538db5cbd3e28`  
		Last Modified: Fri, 05 Jun 2026 16:38:03 GMT  
		Size: 50.1 KB (50061 bytes)  
		MIME: application/vnd.in-toto+json

### `postfixadmin:4-apache` - linux; s390x

```console
$ docker pull postfixadmin@sha256:c91d9cd16f2ba80811cae375f15a1f31c54fcd1c932065e47bfb195cb8e2e428
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.5 MB (179458393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e6d9c512a7c8ed64ffafc4e492c0b877e1ec7e2874009823361e4ec3dfa16b1`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:19:37 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 24 Jun 2026 01:19:53 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 24 Jun 2026 01:19:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Wed, 24 Jun 2026 01:19:53 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 24 Jun 2026 01:19:53 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 24 Jun 2026 01:19:53 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 24 Jun 2026 01:19:53 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 24 Jun 2026 01:33:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 24 Jun 2026 01:33:52 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 24 Jun 2026 01:33:52 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 24 Jun 2026 01:33:52 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Jun 2026 01:33:52 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Jun 2026 01:33:52 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 24 Jun 2026 01:33:52 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 24 Jun 2026 01:33:52 GMT
ENV PHP_VERSION=8.3.31
# Wed, 24 Jun 2026 01:33:52 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.31.tar.xz.asc
# Wed, 24 Jun 2026 01:33:52 GMT
ENV PHP_SHA256=66410cee07f4b2baeb0843140bb2a2b52ef930b5cf9b3d6e6d158b33aae8fa37
# Wed, 24 Jun 2026 01:43:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 24 Jun 2026 01:43:24 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:47:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 24 Jun 2026 01:47:11 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:47:11 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 24 Jun 2026 01:47:11 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 24 Jun 2026 01:47:11 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 24 Jun 2026 01:47:11 GMT
STOPSIGNAL SIGWINCH
# Wed, 24 Jun 2026 01:47:12 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:47:12 GMT
WORKDIR /var/www/html
# Wed, 24 Jun 2026 01:47:12 GMT
EXPOSE map[80/tcp:{}]
# Wed, 24 Jun 2026 01:47:12 GMT
CMD ["apache2-foreground"]
# Tue, 30 Jun 2026 19:06:54 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Tue, 30 Jun 2026 19:06:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		gosu 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Jun 2026 19:07:13 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libpq-dev 		libsqlite3-dev 	; 	docker-php-ext-install -j "$(nproc)" 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -rt apt-mark manual; 			apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean # buildkit
# Tue, 30 Jun 2026 19:07:13 GMT
ARG POSTFIXADMIN_VERSION=4.0.4
# Tue, 30 Jun 2026 19:07:13 GMT
ARG POSTFIXADMIN_SHA512=cce293e92e03f06a20ddbe09a9faec251af3f166f38565429d791feaf832096344a62656bab2a60bbd360545c1a0bd3ed05e11f4a4e46f04858e84639c5391dd
# Tue, 30 Jun 2026 19:07:13 GMT
ENV POSTFIXADMIN_VERSION=4.0.4
# Tue, 30 Jun 2026 19:07:13 GMT
ENV POSTFIXADMIN_SHA512=cce293e92e03f06a20ddbe09a9faec251af3f166f38565429d791feaf832096344a62656bab2a60bbd360545c1a0bd3ed05e11f4a4e46f04858e84639c5391dd
# Tue, 30 Jun 2026 19:07:13 GMT
ENV APACHE_DOCUMENT_ROOT=/var/www/html/public
# Tue, 30 Jun 2026 19:07:13 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.4 POSTFIXADMIN_SHA512=cce293e92e03f06a20ddbe09a9faec251af3f166f38565429d791feaf832096344a62656bab2a60bbd360545c1a0bd3ed05e11f4a4e46f04858e84639c5391dd
RUN set -eu; sed -ri -e 's!/var/www/html!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/sites-available/*.conf; 	sed -ri -e 's!/var/www/!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/apache2.conf /etc/apache2/conf-available/*.conf # buildkit
# Tue, 30 Jun 2026 19:07:13 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.4 POSTFIXADMIN_SHA512=cce293e92e03f06a20ddbe09a9faec251af3f166f38565429d791feaf832096344a62656bab2a60bbd360545c1a0bd3ed05e11f4a4e46f04858e84639c5391dd
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/v${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin # buildkit
# Tue, 30 Jun 2026 19:07:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Jun 2026 19:07:14 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 30 Jun 2026 19:07:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 30 Jun 2026 19:07:22 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.4 POSTFIXADMIN_SHA512=cce293e92e03f06a20ddbe09a9faec251af3f166f38565429d791feaf832096344a62656bab2a60bbd360545c1a0bd3ed05e11f4a4e46f04858e84639c5391dd
RUN set -eux; 	composerDeps=" 		unzip 	"; 	apt-get update; 	apt-get install -y --no-install-recommends $composerDeps; 		export COMPOSER_HOME="$(mktemp -d)"; 	composer install --ignore-platform-req=ext-mysqli --no-dev --no-interaction --working-dir /usr/src/postfixadmin; 	rm -rf "$COMPOSER_HOME"; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $composerDeps; 	apt-get dist-clean # buildkit
# Tue, 30 Jun 2026 19:07:22 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Tue, 30 Jun 2026 19:07:22 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:b6a0af2ceb4b698210b8776157288a3fb06e46aaf75d641139449fcc50ce430d`  
		Last Modified: Wed, 24 Jun 2026 00:28:43 GMT  
		Size: 29.9 MB (29851381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00bb5043cbaffad0e2447070b4a5f2b29ea8f92190db347856d7a7b2afa8db0a`  
		Last Modified: Wed, 24 Jun 2026 01:23:50 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ba630d3700db23d64e3bf4975aae41a0cef309b5e0da02aa4e11522332f82a6`  
		Last Modified: Wed, 24 Jun 2026 01:23:52 GMT  
		Size: 92.6 MB (92572737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8d638a07841acb9fde6207fdb8aef39118b24dcc076004311a2f5332cfffa76`  
		Last Modified: Wed, 24 Jun 2026 01:23:51 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9934cf4fad3b9e7bdee6e9c72448c30a5832d72b4e60601c625ac641f62109d`  
		Last Modified: Wed, 24 Jun 2026 01:38:17 GMT  
		Size: 4.3 MB (4331455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e78a78df21c9e39fcde33b184440187a4b2dd6a7d7cae8c6837ccfbbceabb03`  
		Last Modified: Wed, 24 Jun 2026 01:38:17 GMT  
		Size: 437.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dafe91619df699122d9902dc580de5c79d359894a0bc8ddd2c722fadd53a1683`  
		Last Modified: Wed, 24 Jun 2026 01:38:17 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89592f836d40d4f256027f1a191116e22388b70b5ad58202fbf7ee5ec0181c3a`  
		Last Modified: Wed, 24 Jun 2026 01:47:30 GMT  
		Size: 12.8 MB (12768530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06d9652bf9fc8377adb4931f4c5a5fd8c9f236682f5d49b64a62754928ac5a64`  
		Last Modified: Wed, 24 Jun 2026 01:47:29 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b3121f2c934d575606a7ffb2402def865a177d773643b2d5487dad57bf4d4c5`  
		Last Modified: Wed, 24 Jun 2026 01:47:30 GMT  
		Size: 11.6 MB (11573254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2b1988ee4931e9a12a9e1c026aa02fd60d8084b92a41dfaeb2e460748f1f0fb`  
		Last Modified: Wed, 24 Jun 2026 01:47:29 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2ebd2bb8acc79169ed9a6e1f7ef330780b65ea9775e003e38511d5674b05d98`  
		Last Modified: Wed, 24 Jun 2026 01:47:30 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed1747056218bffad527151e6bcab21290feac23608d179ad2c4bf41d8a73c38`  
		Last Modified: Wed, 24 Jun 2026 01:47:30 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d3f06c0d8d6d77ed2648660e4d4bd411a781a863ff2d18d87cd5bcb55af41ce`  
		Last Modified: Wed, 24 Jun 2026 01:47:31 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:595e3cbded58ca3da0aab0cd91c2a80175982a8defe2005eb007954df4f907f0`  
		Last Modified: Tue, 30 Jun 2026 19:07:32 GMT  
		Size: 1.3 MB (1307474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f76f7de3497359e75163d070e8311c79366ae98c3d86a0a8f5556ecf4f7b90`  
		Last Modified: Tue, 30 Jun 2026 19:07:32 GMT  
		Size: 474.5 KB (474461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82bbac9ebc1a55a54dd97d864bdb71f52b42a695cd591ba94ce1b1f1be8ea3df`  
		Last Modified: Tue, 30 Jun 2026 19:07:32 GMT  
		Size: 7.5 KB (7480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:454b220cd99b8e56a9b85180dcef0d54bbd9622d8141c8153dd804cd764c9cf2`  
		Last Modified: Tue, 30 Jun 2026 19:07:32 GMT  
		Size: 2.6 MB (2603504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:802989aaea017eebeca1fea5c898f742b4be67ffa32fa6cc684e694304374472`  
		Last Modified: Tue, 30 Jun 2026 19:07:33 GMT  
		Size: 1.7 KB (1654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a41c60a2037b141e0996ba7a1382cb3502488582da4afb06ad3d7638701cc1ec`  
		Last Modified: Tue, 30 Jun 2026 19:07:33 GMT  
		Size: 823.3 KB (823343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deaeaf6b80d29a32aaec03678d92b65687fc675c395372810aa295ca53355fcd`  
		Last Modified: Tue, 30 Jun 2026 19:07:34 GMT  
		Size: 23.1 MB (23137382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:4-apache` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:b67730b2b82f40fcb6b4caafc9c7d9e485fe31479da0fae9cec53c57c977fe1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 KB (49967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c30c2ac29f4076e05fe20ba448811d8631c8079ecef5170030483a7a2b7ab9a2`

```dockerfile
```

-	Layers:
	-	`sha256:27d218b0caa0df9c6c4e6e86618a68c88f0b07e97be3461d1b7663994931affb`  
		Last Modified: Tue, 30 Jun 2026 19:07:32 GMT  
		Size: 50.0 KB (49967 bytes)  
		MIME: application/vnd.in-toto+json
