## `yourls:apache`

```console
$ docker pull yourls@sha256:462e1da8bce6c3c6b403720672c6ebe39e673159e123656c763f7aba8c15433a
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
$ docker pull yourls@sha256:bbc60936c783a1e86c1501ebef039803a79a613e9237225d8cf75c3266af4078
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.5 MB (187534894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0edac9cb38c5b1894716d2e4b442c0f12a8b33804372f20f0cbaf5c014e8b444`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:23:15 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Mon, 16 Mar 2026 22:23:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Mon, 16 Mar 2026 22:23:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Mon, 16 Mar 2026 22:23:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 16 Mar 2026 22:23:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 16 Mar 2026 22:23:32 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Mon, 16 Mar 2026 22:23:32 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Mon, 16 Mar 2026 22:23:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Mon, 16 Mar 2026 22:23:38 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Mon, 16 Mar 2026 22:23:39 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Mon, 16 Mar 2026 22:23:39 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 16 Mar 2026 22:23:39 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 16 Mar 2026 22:23:39 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 16 Mar 2026 22:23:39 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Mon, 16 Mar 2026 22:23:39 GMT
ENV PHP_VERSION=8.5.4
# Mon, 16 Mar 2026 22:23:39 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.4.tar.xz.asc
# Mon, 16 Mar 2026 22:23:39 GMT
ENV PHP_SHA256=c1569f1f543f6b025c583cdc0e730e5c5833c603618613f1aa8e75d1524b8c91
# Mon, 16 Mar 2026 22:23:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 16 Mar 2026 22:23:48 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:26:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 16 Mar 2026 22:26:46 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:26:46 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 16 Mar 2026 22:26:46 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 16 Mar 2026 22:26:46 GMT
STOPSIGNAL SIGWINCH
# Mon, 16 Mar 2026 22:26:46 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:26:46 GMT
WORKDIR /var/www/html
# Mon, 16 Mar 2026 22:26:46 GMT
EXPOSE map[80/tcp:{}]
# Mon, 16 Mar 2026 22:26:46 GMT
CMD ["apache2-foreground"]
# Mon, 16 Mar 2026 23:24:15 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)"     bcmath     pdo_mysql     mysqli # buildkit
# Mon, 16 Mar 2026 23:24:15 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Mon, 16 Mar 2026 23:24:15 GMT
RUN a2enmod rewrite expires # buildkit
# Mon, 16 Mar 2026 23:24:17 GMT
ARG YOURLS_VERSION=1.10.3
# Mon, 16 Mar 2026 23:24:17 GMT
ARG YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
# Mon, 16 Mar 2026 23:24:17 GMT
ENV YOURLS_VERSION=1.10.3
# Mon, 16 Mar 2026 23:24:17 GMT
ENV YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
# Mon, 16 Mar 2026 23:24:17 GMT
# ARGS: YOURLS_VERSION=1.10.3 YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Mon, 16 Mar 2026 23:24:17 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Mon, 16 Mar 2026 23:24:17 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 23:24:17 GMT
COPY files/vhost.conf /etc/apache2/sites-available/000-default.conf # buildkit
# Mon, 16 Mar 2026 23:24:17 GMT
COPY files/vhost-https.conf /etc/apache2/sites-available/default-ssl.conf # buildkit
# Mon, 16 Mar 2026 23:24:17 GMT
COPY files/ports.conf /etc/apache2/ports.conf # buildkit
# Mon, 16 Mar 2026 23:24:17 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 16 Mar 2026 23:24:17 GMT
EXPOSE map[8443/tcp:{}]
# Mon, 16 Mar 2026 23:24:17 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Mon, 16 Mar 2026 23:24:17 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:ec781dee3f4719c2ca0dd9e73cb1d4ed834ed1a406495eb6e44b6dfaad5d1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:19 GMT  
		Size: 29.8 MB (29775500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b8bbe5e71e1a3e47e441ca86adf899da136b197e50a0ed84a21b9cb6688ffd7`  
		Last Modified: Mon, 16 Mar 2026 22:27:08 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81fb1bfad0b3a31590d5e1f45efc41bdadb887e6b950bc8743531dba459df569`  
		Last Modified: Mon, 16 Mar 2026 22:27:11 GMT  
		Size: 117.8 MB (117843539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7660bba312d9922fc7efa8734e55f4aeb08ce4f9401bc66fdec80f684db94dc5`  
		Last Modified: Mon, 16 Mar 2026 22:27:08 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a329f51c60be5f3dc24ca9b10fba835d198aeab05667ced5ad3fc20b8bc74dda`  
		Last Modified: Mon, 16 Mar 2026 22:27:08 GMT  
		Size: 4.2 MB (4226955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42878a26b2a89a024880bf35fc5e9736a9572087b69083df11a2c1a8bde50948`  
		Last Modified: Mon, 16 Mar 2026 22:27:09 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69be67c990f8a682441ed28cf893ea55f8c9707013773761cec82c5009744623`  
		Last Modified: Mon, 16 Mar 2026 22:27:09 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d89608c973dad6285c0ec6870a183508897b41bbfbb8b7d65e5b18fe12202b4`  
		Last Modified: Mon, 16 Mar 2026 22:27:10 GMT  
		Size: 14.5 MB (14515548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5551960b4d45745155016cd1be35c21e0ad6bf333bf93e3189ed821f335e08ee`  
		Last Modified: Mon, 16 Mar 2026 22:27:10 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70e08d698001c1ab8dd08be7da7520c3540f3d67747afd3dff12e46bb094401`  
		Last Modified: Mon, 16 Mar 2026 22:27:11 GMT  
		Size: 15.0 MB (15004738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42f8155a24a407d5c5de1b4abee81807d0d7c0d2446616e343126da0a0057335`  
		Last Modified: Mon, 16 Mar 2026 22:27:11 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36d2823c6399e5d8f1e2565fc188c3a45bfb178214dc39d1ba5f22e25b86d664`  
		Last Modified: Mon, 16 Mar 2026 22:27:11 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c6db6cf7eb2bad663880b02b2a765255d1e2b600d1a51d936679e356ee9ebeb`  
		Last Modified: Mon, 16 Mar 2026 22:27:12 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49daf0cfdf25b4af1381d39d3ffb7213bd427ef4f8e74e35cb2364e9d7056b22`  
		Last Modified: Mon, 16 Mar 2026 23:24:23 GMT  
		Size: 108.4 KB (108375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f09da618d32556bb615aa7e2c4e42adb6f30ed14abd21746b408c3a98befc7e5`  
		Last Modified: Mon, 16 Mar 2026 23:24:23 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20931d96f471ca14d334ac8551f9875c86ce68cb350e90cb082e34f5a3782a71`  
		Last Modified: Mon, 16 Mar 2026 23:24:23 GMT  
		Size: 342.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af3cb7fc4cb647255ebec595bcee62e34935a7339e84961c6658e6c0fb3f2bb2`  
		Last Modified: Mon, 16 Mar 2026 23:24:23 GMT  
		Size: 6.0 MB (6048925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c7b0893c619c03c9b2089f02ec3bdc787af9bef570d3f510128c8252bd09d4f`  
		Last Modified: Mon, 16 Mar 2026 23:24:24 GMT  
		Size: 2.1 KB (2094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:168833613d4bc8984d60895a11024588a64ec3031fc17993cf403ffbb9530529`  
		Last Modified: Mon, 16 Mar 2026 23:24:24 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a71fe5a563c5e7020e1412d98a136114436e35bb4f36c67249311f393707b88`  
		Last Modified: Mon, 16 Mar 2026 23:24:25 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14f5e57285b10e084a12843c8a09e0cd767661ab45a7c946aeb54b4444c95de2`  
		Last Modified: Mon, 16 Mar 2026 23:24:24 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13561b98ca665fa9bed10c277839232e0d641b80864df6dedc8b1fcaf7f05846`  
		Last Modified: Mon, 16 Mar 2026 23:24:26 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:apache` - unknown; unknown

```console
$ docker pull yourls@sha256:91c9bf937661b6d8a4369fe3c19d08cde0b3e0deceef2492099788cfc1ae9c51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.6 KB (47588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fd72c81f82e4b225afcf627e147c2744163adb2b790eeb0409e579d5423fdbf`

```dockerfile
```

-	Layers:
	-	`sha256:53697946cf1ad86abc9b43d42a71b22284b7b11648167a2d5e86ab9404d7ae3b`  
		Last Modified: Mon, 16 Mar 2026 23:24:23 GMT  
		Size: 47.6 KB (47588 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:apache` - linux; arm variant v5

```console
$ docker pull yourls@sha256:700579cb02554dd97c9361922c7461f2a829aeb29603d7c0b326c27dcce12c1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.7 MB (160704357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0671359a14583b7467d3d66aa396d83b04988972e8112138cf57677120776081`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1771804800'
# Thu, 12 Mar 2026 23:36:35 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 12 Mar 2026 23:36:57 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 12 Mar 2026 23:36:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 12 Mar 2026 23:36:57 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Mar 2026 23:36:57 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Mar 2026 23:36:57 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 12 Mar 2026 23:36:57 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 12 Mar 2026 23:37:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 12 Mar 2026 23:37:08 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 12 Mar 2026 23:37:08 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 12 Mar 2026 23:37:08 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Mar 2026 23:37:08 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Mar 2026 23:37:08 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Mar 2026 23:37:08 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Thu, 12 Mar 2026 23:37:08 GMT
ENV PHP_VERSION=8.5.4
# Thu, 12 Mar 2026 23:37:08 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.4.tar.xz.asc
# Thu, 12 Mar 2026 23:37:08 GMT
ENV PHP_SHA256=c1569f1f543f6b025c583cdc0e730e5c5833c603618613f1aa8e75d1524b8c91
# Thu, 12 Mar 2026 23:37:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 12 Mar 2026 23:37:21 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Mar 2026 23:40:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Mar 2026 23:40:41 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Mar 2026 23:40:41 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Mar 2026 23:40:41 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Mar 2026 23:40:41 GMT
STOPSIGNAL SIGWINCH
# Thu, 12 Mar 2026 23:40:41 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 12 Mar 2026 23:40:41 GMT
WORKDIR /var/www/html
# Thu, 12 Mar 2026 23:40:41 GMT
EXPOSE map[80/tcp:{}]
# Thu, 12 Mar 2026 23:40:41 GMT
CMD ["apache2-foreground"]
# Fri, 13 Mar 2026 00:22:46 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)"     bcmath     pdo_mysql     mysqli # buildkit
# Fri, 13 Mar 2026 00:22:46 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Fri, 13 Mar 2026 00:22:46 GMT
RUN a2enmod rewrite expires # buildkit
# Fri, 13 Mar 2026 00:22:46 GMT
ARG YOURLS_VERSION=1.10.3
# Fri, 13 Mar 2026 00:22:46 GMT
ARG YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
# Fri, 13 Mar 2026 00:22:46 GMT
ENV YOURLS_VERSION=1.10.3
# Fri, 13 Mar 2026 00:22:46 GMT
ENV YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
# Fri, 13 Mar 2026 00:22:46 GMT
# ARGS: YOURLS_VERSION=1.10.3 YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Fri, 13 Mar 2026 00:22:46 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Fri, 13 Mar 2026 00:22:46 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Mar 2026 00:22:46 GMT
COPY files/vhost.conf /etc/apache2/sites-available/000-default.conf # buildkit
# Fri, 13 Mar 2026 00:22:47 GMT
COPY files/vhost-https.conf /etc/apache2/sites-available/default-ssl.conf # buildkit
# Fri, 13 Mar 2026 00:22:47 GMT
COPY files/ports.conf /etc/apache2/ports.conf # buildkit
# Fri, 13 Mar 2026 00:22:47 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 13 Mar 2026 00:22:47 GMT
EXPOSE map[8443/tcp:{}]
# Fri, 13 Mar 2026 00:22:47 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Fri, 13 Mar 2026 00:22:47 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:280a075cc1d2a97445b9f4430aa9774bfc38fc4217b7fc9d6a7b04e7e431cb65`  
		Last Modified: Tue, 24 Feb 2026 18:42:44 GMT  
		Size: 27.9 MB (27947608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf1ce746b282244f866d043f42c294a4ffd808e5fd82a3521d1cf992fb232c0b`  
		Last Modified: Thu, 12 Mar 2026 23:40:59 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:509cce7b8b6ec3edd04d3157ce238d47112c2e35d0c0bbebbb1f57156e0f3080`  
		Last Modified: Thu, 12 Mar 2026 23:41:02 GMT  
		Size: 94.9 MB (94884024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14feb531cc23aa13075d8237b081c0fb64560aa2988e499680a7dc96221912ee`  
		Last Modified: Thu, 12 Mar 2026 23:40:59 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b0098f59786652a69e774b6fe060e4cf53d1f03c5542ca0f62bbd5b8d4a1774`  
		Last Modified: Thu, 12 Mar 2026 23:41:00 GMT  
		Size: 4.1 MB (4088844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0b5d92db985e500aa35c0fc8c5bac8b20f75e0e55ca79d35400818b0395fb81`  
		Last Modified: Thu, 12 Mar 2026 23:41:00 GMT  
		Size: 433.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf25536a3cf92e232738df7f3769850d18f56ac2c149dd7adc9049754ee72590`  
		Last Modified: Thu, 12 Mar 2026 23:41:01 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c125cf341aa387b4d749c911c9f126455ae4e370a0b11217365378c871e183f`  
		Last Modified: Thu, 12 Mar 2026 23:41:01 GMT  
		Size: 14.5 MB (14512933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28e2c75d7a790959c47c1f64a3963566b658c1fa5f70ceb6989b5dffe3e3bfc8`  
		Last Modified: Thu, 12 Mar 2026 23:41:02 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:206a8880b35fd16a3d0b55ec92bfb73d23cf18349f5dc823ea4b2d79b1b1c33b`  
		Last Modified: Thu, 12 Mar 2026 23:41:02 GMT  
		Size: 13.1 MB (13113714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4763f831acb9dbcc02a0428dbb6bb6d091f91b1b31d1281fe5413fd7a7d7c371`  
		Last Modified: Thu, 12 Mar 2026 23:41:03 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e01b913d90fea8f82f856b4f3705c6202d63188cf3f169c9daf4c4e6adc40872`  
		Last Modified: Thu, 12 Mar 2026 23:41:03 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea27a51e5f36989c2743dcd8069a60816fd5a16d756ee6ff2d6dab462df2dc2e`  
		Last Modified: Thu, 12 Mar 2026 23:41:03 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7abd66e2f846590799214df21e37b56e0539b6f9f3ac858ad3ec51ef7caad63`  
		Last Modified: Fri, 13 Mar 2026 00:22:52 GMT  
		Size: 97.0 KB (96972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46bc60705a6049ee7f2510e37a47ac55583ff952565b061e82522500c8479626`  
		Last Modified: Fri, 13 Mar 2026 00:22:52 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbdd067957630882b1a2036664014bc6a75c14abce54d03ce643c192fdc6d5fb`  
		Last Modified: Fri, 13 Mar 2026 00:22:52 GMT  
		Size: 345.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fe9d2c522734fb522103365bd40460b2d73cb9b7f4830a858bcb80cc41ec82b`  
		Last Modified: Fri, 13 Mar 2026 00:22:52 GMT  
		Size: 6.0 MB (6048933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:721e20c1bb2d9a24181b0872eeba7e17692bdd0783b4e28e290411d8867b8624`  
		Last Modified: Fri, 13 Mar 2026 00:22:53 GMT  
		Size: 2.1 KB (2095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:751966454a5a0f5c11486a1dcb7618653b24841571f47e69f98a8d22d9444e87`  
		Last Modified: Fri, 13 Mar 2026 00:22:53 GMT  
		Size: 1.7 KB (1695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e79aefd21e5ac9bfc100981d0568c0dea84f91a9847726d9887bc40a6a7ae85`  
		Last Modified: Fri, 13 Mar 2026 00:22:53 GMT  
		Size: 500.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8742dacbab9f286d4dbcc1924f90be940197008cf826669b90c42daa5c27c44`  
		Last Modified: Fri, 13 Mar 2026 00:22:53 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b39b27634d5419313e1e3ea73ed8df00b3abf4004aefa8c199cb9b21a6a4cbb`  
		Last Modified: Fri, 13 Mar 2026 00:22:54 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:apache` - unknown; unknown

```console
$ docker pull yourls@sha256:40c46a6453f312d3f8e4c0cf4943cd0153a2d2bc1785d4ecb79472b09e2e70a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 KB (47720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98295f3241523cb6bf6acb228faf0fea93c07ffbd1768c7f8748085fe7782f79`

```dockerfile
```

-	Layers:
	-	`sha256:abb42d66f2ce0bfe5ae1a7ed9c1d90821c577dfbc024e5090557c143775aad90`  
		Last Modified: Fri, 13 Mar 2026 00:22:51 GMT  
		Size: 47.7 KB (47720 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:apache` - linux; arm variant v7

```console
$ docker pull yourls@sha256:26a6df26f48afce777bd03d9c3310b26f749ecad018b36c07048b7da57eb472f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.4 MB (149380569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a7d636432bb8b36e1a5f01c93fa26fe3bc0e41b0112b5aee3f495482af42c9b`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1771804800'
# Thu, 12 Mar 2026 23:31:56 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 12 Mar 2026 23:32:18 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 12 Mar 2026 23:32:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 12 Mar 2026 23:32:18 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Mar 2026 23:32:18 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Mar 2026 23:32:18 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 12 Mar 2026 23:32:18 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 12 Mar 2026 23:32:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 12 Mar 2026 23:32:26 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 12 Mar 2026 23:32:26 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 12 Mar 2026 23:32:26 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Mar 2026 23:32:26 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Mar 2026 23:32:26 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Mar 2026 23:32:26 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Thu, 12 Mar 2026 23:32:26 GMT
ENV PHP_VERSION=8.5.4
# Thu, 12 Mar 2026 23:32:26 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.4.tar.xz.asc
# Thu, 12 Mar 2026 23:32:26 GMT
ENV PHP_SHA256=c1569f1f543f6b025c583cdc0e730e5c5833c603618613f1aa8e75d1524b8c91
# Thu, 12 Mar 2026 23:32:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 12 Mar 2026 23:32:37 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Mar 2026 23:35:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Mar 2026 23:35:36 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Mar 2026 23:35:37 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Mar 2026 23:35:37 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Mar 2026 23:35:37 GMT
STOPSIGNAL SIGWINCH
# Thu, 12 Mar 2026 23:35:37 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 12 Mar 2026 23:35:37 GMT
WORKDIR /var/www/html
# Thu, 12 Mar 2026 23:35:37 GMT
EXPOSE map[80/tcp:{}]
# Thu, 12 Mar 2026 23:35:37 GMT
CMD ["apache2-foreground"]
# Fri, 13 Mar 2026 00:20:49 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)"     bcmath     pdo_mysql     mysqli # buildkit
# Fri, 13 Mar 2026 00:20:49 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Fri, 13 Mar 2026 00:20:49 GMT
RUN a2enmod rewrite expires # buildkit
# Fri, 13 Mar 2026 00:20:50 GMT
ARG YOURLS_VERSION=1.10.3
# Fri, 13 Mar 2026 00:20:50 GMT
ARG YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
# Fri, 13 Mar 2026 00:20:50 GMT
ENV YOURLS_VERSION=1.10.3
# Fri, 13 Mar 2026 00:20:50 GMT
ENV YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
# Fri, 13 Mar 2026 00:20:50 GMT
# ARGS: YOURLS_VERSION=1.10.3 YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Fri, 13 Mar 2026 00:20:51 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Fri, 13 Mar 2026 00:20:51 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Mar 2026 00:20:51 GMT
COPY files/vhost.conf /etc/apache2/sites-available/000-default.conf # buildkit
# Fri, 13 Mar 2026 00:20:51 GMT
COPY files/vhost-https.conf /etc/apache2/sites-available/default-ssl.conf # buildkit
# Fri, 13 Mar 2026 00:20:51 GMT
COPY files/ports.conf /etc/apache2/ports.conf # buildkit
# Fri, 13 Mar 2026 00:20:51 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 13 Mar 2026 00:20:51 GMT
EXPOSE map[8443/tcp:{}]
# Fri, 13 Mar 2026 00:20:51 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Fri, 13 Mar 2026 00:20:51 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:be1f02cfc6708a9e39fcae481bc45544f342901641dd63341104a8ef3fa3cde9`  
		Last Modified: Tue, 24 Feb 2026 18:42:48 GMT  
		Size: 26.2 MB (26213745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52fea0d10a2d2957702c40e8bde5d545b7546c0c3ea45a596c3dbcfba79d774c`  
		Last Modified: Thu, 12 Mar 2026 23:35:19 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a939ecd0ace5c935beaed1b7b765be4d6a3a94aadb90f1d056c54def514c2782`  
		Last Modified: Thu, 12 Mar 2026 23:35:56 GMT  
		Size: 86.2 MB (86246914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdb4ac586be1e1a611606f83ed6a09a336f292279fd277a91695227794e4d6aa`  
		Last Modified: Thu, 12 Mar 2026 23:35:53 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c847be847416477ef1b55bfc8d8a250511c69f6212448c1004ae28c2e10e8dfd`  
		Last Modified: Thu, 12 Mar 2026 23:35:54 GMT  
		Size: 3.8 MB (3757584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b90e730cce7097a62e0210881b822bd85de7cd97f24d29d0f369d7e23e2cf1f5`  
		Last Modified: Thu, 12 Mar 2026 23:35:54 GMT  
		Size: 432.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a51864d721cb04d333e6bd09c3147ad1a60c5c04d72891ffe63afa911fbaac0`  
		Last Modified: Thu, 12 Mar 2026 23:35:55 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72876372a55b4a1d46235da9bb8b6da955c79243f3d21ddda6519d90bc720dc1`  
		Last Modified: Thu, 12 Mar 2026 23:35:56 GMT  
		Size: 14.5 MB (14513033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ef535308c07dce9decd9b02f54264c8db170f7143772dfbcb4dc05836967288`  
		Last Modified: Thu, 12 Mar 2026 23:35:56 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9161851ad3dcdc225b8abe4b3dd466d9839fbdc9c59a54760cb31ee0a706a52`  
		Last Modified: Thu, 12 Mar 2026 23:35:57 GMT  
		Size: 12.5 MB (12498156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5782d0817496766ef4b82b38d1728477c3125ca58a0aae1d38728f19abb001ae`  
		Last Modified: Thu, 12 Mar 2026 23:35:57 GMT  
		Size: 2.5 KB (2464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4f1c17916fd4b7b62ce79f5ae6929f4a519435ec378d2c063ba9ca326a00aa0`  
		Last Modified: Thu, 12 Mar 2026 23:35:58 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff4f0b0707f004f60b05be71fc7881fbb5492f4ad47f4e413d3087cecf90ff7a`  
		Last Modified: Thu, 12 Mar 2026 23:35:58 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2d2334c4364e9657ca2e953dbdd4a569a9cd634463ee0c6749684e36fb39908`  
		Last Modified: Fri, 13 Mar 2026 00:20:56 GMT  
		Size: 90.9 KB (90876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe56985a01934954cac8d22b30f54b293b7b190a29ca614c783a73256e186da7`  
		Last Modified: Fri, 13 Mar 2026 00:20:56 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a71b197e684a34e3e143f8758799625dd7df23f9ab2bda263bc440e5911b6326`  
		Last Modified: Fri, 13 Mar 2026 00:20:56 GMT  
		Size: 345.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6812a077bea8b80d9c6765acc186f141111baf66723b64a20e0149a860f2ef5`  
		Last Modified: Fri, 13 Mar 2026 00:20:56 GMT  
		Size: 6.0 MB (6048925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c5849859ccc369bdfca5ed509ffdcf551cabe6f5a62c54155ed688bc9bb0e6a`  
		Last Modified: Fri, 13 Mar 2026 00:20:57 GMT  
		Size: 2.1 KB (2097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7e60a1719b91f5d62774521b592ce3777115fb1e1f974cd636725d8f4de834f`  
		Last Modified: Fri, 13 Mar 2026 00:20:57 GMT  
		Size: 1.7 KB (1694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b4f767e179f6c13860594ee8b5d9acfbc6b63f9f4f4e0484ae28f4d1ee06b38`  
		Last Modified: Fri, 13 Mar 2026 00:20:57 GMT  
		Size: 502.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a72700ed3e652fd711981d1f59d25c0dd9acb15106e14948feaccfada4c1433d`  
		Last Modified: Fri, 13 Mar 2026 00:20:58 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9631df008695caca4ae5c10168b15cba26ac0c287cb9f9cce3de9a439977441`  
		Last Modified: Fri, 13 Mar 2026 00:20:58 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:apache` - unknown; unknown

```console
$ docker pull yourls@sha256:5e30e37c6c0b629cff92e2de647aca2e9e6ff5b3bcadd067b9722024f720b89e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 KB (47720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90e002d9bf913cd06f27c0e39bcb58a53f92f5ec5e1267b852789dfbfaae127d`

```dockerfile
```

-	Layers:
	-	`sha256:b3abc787e124ea04aa48963b5ac64e16f4c5e49bb8a648b5f604baa6162ffdc1`  
		Last Modified: Fri, 13 Mar 2026 00:20:56 GMT  
		Size: 47.7 KB (47720 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:apache` - linux; arm64 variant v8

```console
$ docker pull yourls@sha256:b3d4d9784ae2c96d7b35571370d77f2d85f1c9dd28070ce20cdf9ed0ec89facb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.9 MB (179854302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8937785fc6014aec64957ab822062feac7fb561a5bc2b426cc62bd4ab4903f0`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:23:02 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Mon, 16 Mar 2026 22:23:20 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Mon, 16 Mar 2026 22:23:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Mon, 16 Mar 2026 22:23:20 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 16 Mar 2026 22:23:20 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 16 Mar 2026 22:23:20 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Mon, 16 Mar 2026 22:23:20 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Mon, 16 Mar 2026 22:23:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Mon, 16 Mar 2026 22:23:27 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Mon, 16 Mar 2026 22:23:27 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Mon, 16 Mar 2026 22:23:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 16 Mar 2026 22:23:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 16 Mar 2026 22:23:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 16 Mar 2026 22:23:27 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Mon, 16 Mar 2026 22:23:27 GMT
ENV PHP_VERSION=8.5.4
# Mon, 16 Mar 2026 22:23:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.4.tar.xz.asc
# Mon, 16 Mar 2026 22:23:27 GMT
ENV PHP_SHA256=c1569f1f543f6b025c583cdc0e730e5c5833c603618613f1aa8e75d1524b8c91
# Mon, 16 Mar 2026 22:23:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 16 Mar 2026 22:23:37 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:26:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 16 Mar 2026 22:26:59 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:26:59 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 16 Mar 2026 22:26:59 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 16 Mar 2026 22:26:59 GMT
STOPSIGNAL SIGWINCH
# Mon, 16 Mar 2026 22:26:59 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:27:00 GMT
WORKDIR /var/www/html
# Mon, 16 Mar 2026 22:27:00 GMT
EXPOSE map[80/tcp:{}]
# Mon, 16 Mar 2026 22:27:00 GMT
CMD ["apache2-foreground"]
# Mon, 16 Mar 2026 23:29:35 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)"     bcmath     pdo_mysql     mysqli # buildkit
# Mon, 16 Mar 2026 23:29:35 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Mon, 16 Mar 2026 23:29:35 GMT
RUN a2enmod rewrite expires # buildkit
# Mon, 16 Mar 2026 23:29:36 GMT
ARG YOURLS_VERSION=1.10.3
# Mon, 16 Mar 2026 23:29:36 GMT
ARG YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
# Mon, 16 Mar 2026 23:29:36 GMT
ENV YOURLS_VERSION=1.10.3
# Mon, 16 Mar 2026 23:29:36 GMT
ENV YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
# Mon, 16 Mar 2026 23:29:36 GMT
# ARGS: YOURLS_VERSION=1.10.3 YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Mon, 16 Mar 2026 23:29:37 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Mon, 16 Mar 2026 23:29:37 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 23:29:37 GMT
COPY files/vhost.conf /etc/apache2/sites-available/000-default.conf # buildkit
# Mon, 16 Mar 2026 23:29:37 GMT
COPY files/vhost-https.conf /etc/apache2/sites-available/default-ssl.conf # buildkit
# Mon, 16 Mar 2026 23:29:37 GMT
COPY files/ports.conf /etc/apache2/ports.conf # buildkit
# Mon, 16 Mar 2026 23:29:37 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 16 Mar 2026 23:29:37 GMT
EXPOSE map[8443/tcp:{}]
# Mon, 16 Mar 2026 23:29:37 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Mon, 16 Mar 2026 23:29:37 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:f4badedbec24858ef2dc51256f6418328e305e9c3c5a5e093581f83425618bd5`  
		Last Modified: Mon, 16 Mar 2026 21:53:04 GMT  
		Size: 30.1 MB (30138416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8af7753225c0a79ef3c56194676dac85a2ade8fb9c256415f21600acb03a9731`  
		Last Modified: Mon, 16 Mar 2026 22:26:39 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1b0ffd274772cdefc5ba095eece54497b0562452e0ea1caf5998bb486d5b630`  
		Last Modified: Mon, 16 Mar 2026 22:27:23 GMT  
		Size: 110.2 MB (110164972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d18be28244641f4edd769e324a504255161c59fef2d5759b4daad764090536f1`  
		Last Modified: Mon, 16 Mar 2026 22:27:20 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84b68504ace9fdb7e306032e2adf1d297b591f087627c533b121b03e5ace5e1b`  
		Last Modified: Mon, 16 Mar 2026 22:27:21 GMT  
		Size: 4.3 MB (4305468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4164c41cf3f401bd706f091c14f5deb30cfd58d065cdd074b0b704b22afaf14f`  
		Last Modified: Mon, 16 Mar 2026 22:27:21 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fb1ddd3dd35c3ad1fff159bf905b70255b82a38083e7689184f019e1bb23015`  
		Last Modified: Mon, 16 Mar 2026 22:27:22 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7259b3ac10dc6bf797623dfc9651249448afea40cfbaefa14d951eedc066534e`  
		Last Modified: Mon, 16 Mar 2026 22:27:23 GMT  
		Size: 14.5 MB (14515101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db7006e7bd8693560577918f9f1af978ad1e91886d5574a2e27625f9e489d333`  
		Last Modified: Mon, 16 Mar 2026 22:27:23 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2871862d507ab1b9a11fa169ef5245b41d242148afcbb3faec2b389957e27cf`  
		Last Modified: Mon, 16 Mar 2026 22:27:23 GMT  
		Size: 14.6 MB (14564378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c4d74cc84fd57003c0cddf18fac0ae0886e3dc0579ba79f08092c458f87566f`  
		Last Modified: Mon, 16 Mar 2026 22:27:24 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e372984d86f657bf1dd419b79dadba9f5faf439b81cdcdda3e2d5520b66b4ef5`  
		Last Modified: Mon, 16 Mar 2026 22:27:24 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6446934860a2665f78ee36327b931b5537ec51372f4ef9c79584d396ce0d1c5d`  
		Last Modified: Mon, 16 Mar 2026 22:27:25 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42dd9959603012d3f4894f7bca1f831169ff4599b71cabf35303ef7171652feb`  
		Last Modified: Mon, 16 Mar 2026 23:29:42 GMT  
		Size: 105.8 KB (105752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bfcb501765ee5c3a086c6d4862df19b790997ba9344b43a1d6626c7cab829f6`  
		Last Modified: Mon, 16 Mar 2026 23:29:42 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86865ebcbf51ee721903ecd3a0ae4d30f2512af2e4bc0bb905f47be011584b98`  
		Last Modified: Mon, 16 Mar 2026 23:29:42 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e1fa3bef5691a2d61a4e5a7a2f0f8e3e1066326126f53621f86c5bb8be1b826`  
		Last Modified: Mon, 16 Mar 2026 23:29:42 GMT  
		Size: 6.0 MB (6048923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c67d036f5ae319296e15617d37bb939040358cd6e7ee94f64fd6d022f37fe6d2`  
		Last Modified: Mon, 16 Mar 2026 23:29:43 GMT  
		Size: 2.1 KB (2096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87d841b5d6b33b557063fffcc8042e9bde415998d0829922e860b0b17ef64bdd`  
		Last Modified: Mon, 16 Mar 2026 23:29:43 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0863bc53890582f4ddbb998c9ac5b3fde89d77bdf97b2f24d98616b25c2d9c7e`  
		Last Modified: Mon, 16 Mar 2026 23:29:43 GMT  
		Size: 500.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc86acf8b3541495ee024b242eaa23cd401e76a25e3f2a628d92fa98393c3f7c`  
		Last Modified: Mon, 16 Mar 2026 23:29:43 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87296eed967749cd18420aabff853d23c6a517034ec3740fa45db590a25ec4e5`  
		Last Modified: Mon, 16 Mar 2026 23:29:44 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:apache` - unknown; unknown

```console
$ docker pull yourls@sha256:8ccb1d2d2b8e870131d8e6ea0d936d1a7586d89e51f20d32ae46e450dea49f4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 KB (47786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d198384e933d26bfa2a7b3ad35ce20e6120c70d82af6245f3cd97f4087c278da`

```dockerfile
```

-	Layers:
	-	`sha256:1f4d4607297b1638c4f5aefa488b0de46ad1eac15909fda2950173ca3e87c20a`  
		Last Modified: Mon, 16 Mar 2026 23:29:42 GMT  
		Size: 47.8 KB (47786 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:apache` - linux; 386

```console
$ docker pull yourls@sha256:4e7153b29c9bcc64ea077ad3f2035c09101d611049bda5a6470ba7386f023e93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.9 MB (187934365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0caaca397fd957420e82d8ecda127fad814336c596ab39da203c26d8bd840836`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:19:03 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Mon, 16 Mar 2026 22:19:23 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Mon, 16 Mar 2026 22:19:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Mon, 16 Mar 2026 22:19:23 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 16 Mar 2026 22:19:23 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 16 Mar 2026 22:19:23 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Mon, 16 Mar 2026 22:19:23 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Mon, 16 Mar 2026 22:19:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Mon, 16 Mar 2026 22:19:31 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Mon, 16 Mar 2026 22:19:31 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Mon, 16 Mar 2026 22:19:31 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 16 Mar 2026 22:19:31 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 16 Mar 2026 22:19:31 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 16 Mar 2026 22:19:31 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Mon, 16 Mar 2026 22:19:31 GMT
ENV PHP_VERSION=8.5.4
# Mon, 16 Mar 2026 22:19:31 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.4.tar.xz.asc
# Mon, 16 Mar 2026 22:19:31 GMT
ENV PHP_SHA256=c1569f1f543f6b025c583cdc0e730e5c5833c603618613f1aa8e75d1524b8c91
# Mon, 16 Mar 2026 22:19:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 16 Mar 2026 22:19:42 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:23:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 16 Mar 2026 22:23:00 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:23:00 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 16 Mar 2026 22:23:00 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 16 Mar 2026 22:23:00 GMT
STOPSIGNAL SIGWINCH
# Mon, 16 Mar 2026 22:23:00 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:23:00 GMT
WORKDIR /var/www/html
# Mon, 16 Mar 2026 22:23:00 GMT
EXPOSE map[80/tcp:{}]
# Mon, 16 Mar 2026 22:23:00 GMT
CMD ["apache2-foreground"]
# Mon, 16 Mar 2026 23:41:11 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)"     bcmath     pdo_mysql     mysqli # buildkit
# Mon, 16 Mar 2026 23:41:11 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Mon, 16 Mar 2026 23:41:11 GMT
RUN a2enmod rewrite expires # buildkit
# Mon, 16 Mar 2026 23:41:12 GMT
ARG YOURLS_VERSION=1.10.3
# Mon, 16 Mar 2026 23:41:12 GMT
ARG YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
# Mon, 16 Mar 2026 23:41:12 GMT
ENV YOURLS_VERSION=1.10.3
# Mon, 16 Mar 2026 23:41:12 GMT
ENV YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
# Mon, 16 Mar 2026 23:41:12 GMT
# ARGS: YOURLS_VERSION=1.10.3 YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Mon, 16 Mar 2026 23:41:12 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Mon, 16 Mar 2026 23:41:12 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 23:41:13 GMT
COPY files/vhost.conf /etc/apache2/sites-available/000-default.conf # buildkit
# Mon, 16 Mar 2026 23:41:13 GMT
COPY files/vhost-https.conf /etc/apache2/sites-available/default-ssl.conf # buildkit
# Mon, 16 Mar 2026 23:41:13 GMT
COPY files/ports.conf /etc/apache2/ports.conf # buildkit
# Mon, 16 Mar 2026 23:41:13 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 16 Mar 2026 23:41:13 GMT
EXPOSE map[8443/tcp:{}]
# Mon, 16 Mar 2026 23:41:13 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Mon, 16 Mar 2026 23:41:13 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:2c0c3f3238f3d4cecd93e4dee6eda788943ef955de61c3ad4ff659da1f43ba60`  
		Last Modified: Mon, 16 Mar 2026 21:53:39 GMT  
		Size: 31.3 MB (31291132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6430aa54236efc8566784d692daca77ac8d017a92bc6b1357ed51459cc9ad0a6`  
		Last Modified: Mon, 16 Mar 2026 22:23:20 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e3d9d0b585f178e57b411bab3823359830c6aac1ddcce9d296c31f65569aba9`  
		Last Modified: Mon, 16 Mar 2026 22:23:23 GMT  
		Size: 116.1 MB (116144472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7d52c7717486cef6f41a448a04ac0781f3ec983202bb1c87549a04810369fa7`  
		Last Modified: Mon, 16 Mar 2026 22:23:20 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aae4a5d22a825625df7a52712e780882edb7e9473a9c6ab4f035365bb1cc0d2f`  
		Last Modified: Mon, 16 Mar 2026 22:23:21 GMT  
		Size: 4.5 MB (4458327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5c5173129d77c61fa605c145b4e28ad12fdfd40686464598069def9d330f436`  
		Last Modified: Mon, 16 Mar 2026 22:23:21 GMT  
		Size: 432.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b642f9658a387d63b833794c1dd8c29e7174a3c605e6afcbe07dee277b4e75a7`  
		Last Modified: Mon, 16 Mar 2026 22:23:21 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ecf2f0edcb2adb42682eda9eaf4d33bf6888df530f50c2996ba56f46ad51c09`  
		Last Modified: Mon, 16 Mar 2026 22:23:22 GMT  
		Size: 14.5 MB (14514325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66fbfa9dd2a0d36f7810cea16c728b4e0d59c73a312d7a88444e6c95a1f169f3`  
		Last Modified: Mon, 16 Mar 2026 22:23:23 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78174901719932f8760c360d9861f00130aaa84daa2e2f43053e385641f63723`  
		Last Modified: Mon, 16 Mar 2026 22:23:23 GMT  
		Size: 15.4 MB (15354048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e787ce2c53c6c18438080746c3213cfc9ef971bb9acd520778635dc6367f6140`  
		Last Modified: Mon, 16 Mar 2026 22:23:24 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d05dcef2c42bd705a1e74b7c3e268a049a0e4e63d691499fe22b75ccc95d6a39`  
		Last Modified: Mon, 16 Mar 2026 22:23:24 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ed413837bc6d83b13d95d29098e04236ebbbacd32fccd10987464f07249673`  
		Last Modified: Mon, 16 Mar 2026 22:23:24 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4700cc1308a1280861edc82148f8a8103c169093bc22bfee6bad3db56fb9155`  
		Last Modified: Mon, 16 Mar 2026 23:41:18 GMT  
		Size: 111.8 KB (111831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc527c877a1f96c99dd596fd8983c91d6aa915520fa3ef7f508c94e10bb6a052`  
		Last Modified: Mon, 16 Mar 2026 23:41:18 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fafed984c5236bbce308a9c3fddfe8ddcde4eff75bb3f3a12bce0afd3bd34efb`  
		Last Modified: Mon, 16 Mar 2026 23:41:18 GMT  
		Size: 344.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b3ccc5093c4a3c559becdbd70f28cf6f567eb1cb17548508c4815900aa98603`  
		Last Modified: Mon, 16 Mar 2026 23:41:18 GMT  
		Size: 6.0 MB (6048923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4594d13112c12c7f7d910903449701d80d7a4643112699aad4e487cb7b29952e`  
		Last Modified: Mon, 16 Mar 2026 23:41:19 GMT  
		Size: 2.1 KB (2094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fd3bc433b5d8944a9f5ba7df2d61881d6e87979a910f2e8e4308ba6d6e63f6c`  
		Last Modified: Mon, 16 Mar 2026 23:41:19 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de2b6d4661610a351d77959db7167a2095b62333af553259edec9119e89e6ccc`  
		Last Modified: Mon, 16 Mar 2026 23:41:19 GMT  
		Size: 501.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad0cd03c2b848a0a2f9429c15e08191ebd7b1e2b3f38678e649c93f277fe48fe`  
		Last Modified: Mon, 16 Mar 2026 23:41:19 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ab0dbf5816c7bc4416457393099f5068858a0634f3d2412a9cfcb52e6df91b7`  
		Last Modified: Mon, 16 Mar 2026 23:41:20 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:apache` - unknown; unknown

```console
$ docker pull yourls@sha256:4054dbc110ac08330c81f5b9b69c0e00c0e9bf5886b48d3a884ab5f05903610e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.5 KB (47531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18867d006bbee70a9760ff2b71a7d2a3f635cc22bbcf5769ae47aea8a6f58a3d`

```dockerfile
```

-	Layers:
	-	`sha256:fb988af82b913d45e06e4caf447196be8571a5bcc70f7a5b329c7612d43b3d31`  
		Last Modified: Mon, 16 Mar 2026 23:41:18 GMT  
		Size: 47.5 KB (47531 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:apache` - linux; ppc64le

```console
$ docker pull yourls@sha256:c8df44bdbb7a1e5242595c69921588812330cd670ccb0ed3226a0c6a621442f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.8 MB (183758393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:851697907943f702fe076c0da11d8a0f5b1d537988b4f5c7e27560a68849ef5a`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Thu, 12 Mar 2026 23:28:30 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 12 Mar 2026 23:29:05 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 12 Mar 2026 23:29:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 12 Mar 2026 23:29:05 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Mar 2026 23:29:06 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Mar 2026 23:29:06 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 12 Mar 2026 23:29:06 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 12 Mar 2026 23:29:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 12 Mar 2026 23:29:24 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 12 Mar 2026 23:29:24 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 12 Mar 2026 23:29:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Mar 2026 23:29:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Mar 2026 23:29:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Mar 2026 23:29:24 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Thu, 12 Mar 2026 23:29:24 GMT
ENV PHP_VERSION=8.5.4
# Thu, 12 Mar 2026 23:29:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.4.tar.xz.asc
# Thu, 12 Mar 2026 23:29:24 GMT
ENV PHP_SHA256=c1569f1f543f6b025c583cdc0e730e5c5833c603618613f1aa8e75d1524b8c91
# Thu, 12 Mar 2026 23:29:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 12 Mar 2026 23:29:43 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Mar 2026 23:34:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Mar 2026 23:34:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Mar 2026 23:34:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Mar 2026 23:34:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Mar 2026 23:34:40 GMT
STOPSIGNAL SIGWINCH
# Thu, 12 Mar 2026 23:34:41 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 12 Mar 2026 23:34:41 GMT
WORKDIR /var/www/html
# Thu, 12 Mar 2026 23:34:41 GMT
EXPOSE map[80/tcp:{}]
# Thu, 12 Mar 2026 23:34:41 GMT
CMD ["apache2-foreground"]
# Fri, 13 Mar 2026 01:16:53 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)"     bcmath     pdo_mysql     mysqli # buildkit
# Fri, 13 Mar 2026 01:16:54 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Fri, 13 Mar 2026 01:16:55 GMT
RUN a2enmod rewrite expires # buildkit
# Fri, 13 Mar 2026 01:16:58 GMT
ARG YOURLS_VERSION=1.10.3
# Fri, 13 Mar 2026 01:16:58 GMT
ARG YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
# Fri, 13 Mar 2026 01:16:58 GMT
ENV YOURLS_VERSION=1.10.3
# Fri, 13 Mar 2026 01:16:58 GMT
ENV YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
# Fri, 13 Mar 2026 01:16:58 GMT
# ARGS: YOURLS_VERSION=1.10.3 YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Fri, 13 Mar 2026 01:16:59 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Fri, 13 Mar 2026 01:16:59 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Mar 2026 01:17:00 GMT
COPY files/vhost.conf /etc/apache2/sites-available/000-default.conf # buildkit
# Fri, 13 Mar 2026 01:17:00 GMT
COPY files/vhost-https.conf /etc/apache2/sites-available/default-ssl.conf # buildkit
# Fri, 13 Mar 2026 01:17:02 GMT
COPY files/ports.conf /etc/apache2/ports.conf # buildkit
# Fri, 13 Mar 2026 01:17:02 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 13 Mar 2026 01:17:02 GMT
EXPOSE map[8443/tcp:{}]
# Fri, 13 Mar 2026 01:17:02 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Fri, 13 Mar 2026 01:17:02 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:91416f8238d93c33a42d4030b8a24944e7f5b4b808e36e206f1bf078f8543c0d`  
		Last Modified: Tue, 24 Feb 2026 18:45:10 GMT  
		Size: 33.6 MB (33600216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3775d5ddfc085666c347a617d5e829f26310c4192ca085c2d6858133f39bb6c`  
		Last Modified: Thu, 12 Mar 2026 23:34:49 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ec48d97db5ea952f4576b2f9d01739464e680954cd8131033b1130e99184b70`  
		Last Modified: Thu, 12 Mar 2026 23:34:53 GMT  
		Size: 109.6 MB (109598721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22b0b943276144e2999641cbe60a6b81da9ba29447be9c399b166708aed41be`  
		Last Modified: Thu, 12 Mar 2026 23:34:49 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3f84c131d02b3be73176ef8b7c57e2a39b63dcc1bb5ceea93dac058e985306e`  
		Last Modified: Thu, 12 Mar 2026 23:35:05 GMT  
		Size: 4.9 MB (4880872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae2728e307aae21e44ce3f6ba94a4c04ed30c34f504f8061a61c64a57cb08ad`  
		Last Modified: Thu, 12 Mar 2026 23:35:05 GMT  
		Size: 433.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fd5424425190807f10168029676dc3af5f99f0d4e09b8b0e41e35032cd1b24a`  
		Last Modified: Thu, 12 Mar 2026 23:35:05 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d0bf979a21a0f166c5bd032ae7cbc392696f7b81d0f3590f396b8b9ea236790`  
		Last Modified: Thu, 12 Mar 2026 23:35:05 GMT  
		Size: 14.5 MB (14514462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d30d24870f03d934706ef07673bc91ea0fc3d449939fc7b952daa340451eed`  
		Last Modified: Thu, 12 Mar 2026 23:35:06 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b30fe930cb8ea1209750d52fdd20c412ace8b3f01c6d0f6d00eb037c82d8cea`  
		Last Modified: Thu, 12 Mar 2026 23:35:06 GMT  
		Size: 15.0 MB (14986549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:322d63d40dac56f60f5738c4e05c65e251e0851dcbd3e4b881dedb4dc372c057`  
		Last Modified: Thu, 12 Mar 2026 23:35:06 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97a20c94346fc0ca745272562d693370f76c3ca667990fb3efb209e1b6968ad3`  
		Last Modified: Thu, 12 Mar 2026 23:35:07 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a3afcd7ff47d3d38e8e68f773486c93bbad9e43d081a276ed51441ddd56791b`  
		Last Modified: Thu, 12 Mar 2026 23:35:07 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dedaa98df5bbab7027dfd22f0c3da7bd42467736662fc74787ae0332cb8e5710`  
		Last Modified: Fri, 13 Mar 2026 01:17:15 GMT  
		Size: 117.3 KB (117324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64b8fd22b889681fd18b57c00ecedf85b437703d696dcb3f2af7944c01d441aa`  
		Last Modified: Fri, 13 Mar 2026 01:17:15 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc0baf9b0f8d00beebcf1a85071a3081d54d9d224be467ed348cdc5ca122c485`  
		Last Modified: Fri, 13 Mar 2026 01:17:15 GMT  
		Size: 343.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93b1886cead4a60e148c19e0beabaa7ccb6cd6332acc49b5a508c47f5ef34352`  
		Last Modified: Fri, 13 Mar 2026 01:17:15 GMT  
		Size: 6.0 MB (6048922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9c8c4a807ee9c213157290a5718f62c5acdb3793cb966fae879e7d2c0e7d2a2`  
		Last Modified: Fri, 13 Mar 2026 01:17:16 GMT  
		Size: 2.1 KB (2096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea98174c2e10dc8b8612b49b09b508c558916d3bfed8eb16c9305ac8e9f2dd60`  
		Last Modified: Fri, 13 Mar 2026 01:17:16 GMT  
		Size: 1.7 KB (1695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3b988eb8d1f435eedbaf12fe640573df120d4f502f7f1d33357d6eb1f932295`  
		Last Modified: Fri, 13 Mar 2026 01:17:16 GMT  
		Size: 501.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ebe6b5f7a52e0b42a684a2777491ceddcde45f4635d2e4fc35164b00f2af15d`  
		Last Modified: Fri, 13 Mar 2026 01:17:16 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21c0443c60f3eddeaa14525bc3bdbe183050dbd6dca9bb51567d4c0c2d8b8bb9`  
		Last Modified: Fri, 13 Mar 2026 01:17:17 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:apache` - unknown; unknown

```console
$ docker pull yourls@sha256:2607691346b490981ddb4aaabf28eeb1a539903f29932d804a18f3386021c99e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 KB (47663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e52780cd2224d17a1f96aa301217a6cffb3826b7ab20e83c13c5d27e8d92c164`

```dockerfile
```

-	Layers:
	-	`sha256:8c0ce6cc99b35b3967fdc14dbf684d5b17428b67b3a764e6eaf3487330bce647`  
		Last Modified: Fri, 13 Mar 2026 01:17:14 GMT  
		Size: 47.7 KB (47663 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:apache` - linux; riscv64

```console
$ docker pull yourls@sha256:02027adab6d0f6bdd6655ba607878a329d9bf65e9d6d7dc176753903ea5d80cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.5 MB (213525350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f6785b7dde5b8f9b02694c6b7b1a61c5edcb657393f55c9d64b9bc6e8683309`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1771804800'
# Wed, 25 Feb 2026 08:37:15 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 25 Feb 2026 08:39:17 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 25 Feb 2026 08:39:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Wed, 25 Feb 2026 08:39:17 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 25 Feb 2026 08:39:18 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 25 Feb 2026 08:39:18 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 25 Feb 2026 08:39:18 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 25 Feb 2026 09:45:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 25 Feb 2026 09:45:07 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 25 Feb 2026 09:45:07 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 25 Feb 2026 09:45:07 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 25 Feb 2026 09:45:07 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 25 Feb 2026 09:45:07 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 25 Feb 2026 09:45:07 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Wed, 25 Feb 2026 09:45:07 GMT
ENV PHP_VERSION=8.5.4
# Wed, 25 Feb 2026 09:45:07 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.4.tar.xz.asc
# Wed, 25 Feb 2026 09:45:07 GMT
ENV PHP_SHA256=c1569f1f543f6b025c583cdc0e730e5c5833c603618613f1aa8e75d1524b8c91
# Fri, 13 Mar 2026 00:56:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 13 Mar 2026 00:56:29 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 13 Mar 2026 01:53:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 13 Mar 2026 01:53:36 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 13 Mar 2026 01:53:37 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 13 Mar 2026 01:53:37 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 13 Mar 2026 01:53:37 GMT
STOPSIGNAL SIGWINCH
# Fri, 13 Mar 2026 01:53:37 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 13 Mar 2026 01:53:37 GMT
WORKDIR /var/www/html
# Fri, 13 Mar 2026 01:53:37 GMT
EXPOSE map[80/tcp:{}]
# Fri, 13 Mar 2026 01:53:37 GMT
CMD ["apache2-foreground"]
# Sat, 14 Mar 2026 03:01:07 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)"     bcmath     pdo_mysql     mysqli # buildkit
# Sat, 14 Mar 2026 03:01:08 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Sat, 14 Mar 2026 03:01:08 GMT
RUN a2enmod rewrite expires # buildkit
# Sat, 14 Mar 2026 03:01:12 GMT
ARG YOURLS_VERSION=1.10.3
# Sat, 14 Mar 2026 03:01:12 GMT
ARG YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
# Sat, 14 Mar 2026 03:01:12 GMT
ENV YOURLS_VERSION=1.10.3
# Sat, 14 Mar 2026 03:01:12 GMT
ENV YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
# Sat, 14 Mar 2026 03:01:12 GMT
# ARGS: YOURLS_VERSION=1.10.3 YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Sat, 14 Mar 2026 03:01:12 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Sat, 14 Mar 2026 03:01:12 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 14 Mar 2026 03:01:12 GMT
COPY files/vhost.conf /etc/apache2/sites-available/000-default.conf # buildkit
# Sat, 14 Mar 2026 03:01:12 GMT
COPY files/vhost-https.conf /etc/apache2/sites-available/default-ssl.conf # buildkit
# Sat, 14 Mar 2026 03:01:13 GMT
COPY files/ports.conf /etc/apache2/ports.conf # buildkit
# Sat, 14 Mar 2026 03:01:13 GMT
EXPOSE map[8080/tcp:{}]
# Sat, 14 Mar 2026 03:01:13 GMT
EXPOSE map[8443/tcp:{}]
# Sat, 14 Mar 2026 03:01:13 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Sat, 14 Mar 2026 03:01:13 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:7d614b9ad5a6f3dd0478c6903a6d2ffddc9bc5b17650714d4c1f761161fde58d`  
		Last Modified: Tue, 24 Feb 2026 18:59:14 GMT  
		Size: 28.3 MB (28276417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ae6df9269bfd4174a44849bb7987f7a59ec3c5430213257f79ad656b80f4e2d`  
		Last Modified: Wed, 25 Feb 2026 09:42:47 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e38127a1d5098bc45d1ab51573d3cb4b81e383d9777a8e0449378000b440c3dc`  
		Last Modified: Wed, 25 Feb 2026 09:43:30 GMT  
		Size: 146.6 MB (146584285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a1ad2ba1292d9c3abe04163ae27f6acc0fa6ab45f94cf6f5f5eebe7c6a93122`  
		Last Modified: Wed, 25 Feb 2026 09:42:47 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f3a876c8422313d0a43027590b8fc459e4a29661c5847fd658bce53a13bb4e0`  
		Last Modified: Wed, 25 Feb 2026 10:46:34 GMT  
		Size: 4.0 MB (4037258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd8e4b4bf531444641519173c266dfe93629a2bdb44e06f0c5459425152cb23d`  
		Last Modified: Wed, 25 Feb 2026 10:46:32 GMT  
		Size: 439.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39d2885598cb9a87bb0bc5f0fc373406eb91bf8da837243354f7f0d3155de09b`  
		Last Modified: Wed, 25 Feb 2026 10:46:33 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7904821464438b71cf51800c38df1c8ba773a532a2f96d26ae4944904380d2a3`  
		Last Modified: Fri, 13 Mar 2026 01:56:52 GMT  
		Size: 14.5 MB (14530030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4f1d94f7d858906f24438a209fb7cf6858c73490e2e953b0e802e6470fb73e1`  
		Last Modified: Fri, 13 Mar 2026 01:56:47 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c94d14a869022b068ccd4550eccd6af02a06d134ecc96d561bb4d6959d75bb88`  
		Last Modified: Fri, 13 Mar 2026 01:56:52 GMT  
		Size: 13.9 MB (13930487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7abf6c7c26df6d5556737d76bd1abd3903afe30205c6e13eb1439b86dd2f3a3e`  
		Last Modified: Fri, 13 Mar 2026 01:56:47 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4410f7ac7a74242e2375eaf16f9bc7b6e50ca929332f1c3e22c8a1a721d4a474`  
		Last Modified: Fri, 13 Mar 2026 01:56:50 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7a3fbecca0f75c8f6687971721519c364d1be340e5b3498be338025991404a0`  
		Last Modified: Fri, 13 Mar 2026 01:56:50 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f5e3ffca8336ca267c2edcc8ccf7dca6856822ed8aeaa171f355b5e7bb4e57f`  
		Last Modified: Sat, 14 Mar 2026 03:02:04 GMT  
		Size: 106.6 KB (106582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e631dc50a20f9a982185d41c8e90ab383b7cd225ab3378899203d81293d7445`  
		Last Modified: Sat, 14 Mar 2026 03:02:04 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99b64c0cff30726af5218527fcd93325f5d385bd0010b1258c2a5bc71410930e`  
		Last Modified: Sat, 14 Mar 2026 03:02:04 GMT  
		Size: 355.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8c41ef4a91b9ebf5f82cb74a7194ed80a84d9df0be6397268a81674ec0b17cb`  
		Last Modified: Sat, 14 Mar 2026 03:02:05 GMT  
		Size: 6.0 MB (6048926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba233138b77c6e273dad7ff3a16cd5ac728e793496a16458c6587ed4ecf4ca54`  
		Last Modified: Sat, 14 Mar 2026 03:02:05 GMT  
		Size: 2.1 KB (2094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52455a12124fd0de4cc7a111c2cc9fd53bd78e43f799cb8318ef92d7d3d81a0e`  
		Last Modified: Sat, 14 Mar 2026 03:02:06 GMT  
		Size: 1.7 KB (1697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d0eb5039ee1bc7a985b416c1f68878021c0752e874baf63886f85a80085ad06`  
		Last Modified: Sat, 14 Mar 2026 03:02:06 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d507af663f4dd21a3058a2fff7ab962a274f19fa29cf8f26365c3773050e6515`  
		Last Modified: Sat, 14 Mar 2026 03:02:06 GMT  
		Size: 550.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e6cea755c22366057901a2bddb808d6b3d3ed3bda64647fdf673a501793ccb0`  
		Last Modified: Sat, 14 Mar 2026 03:02:06 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:apache` - unknown; unknown

```console
$ docker pull yourls@sha256:b17b9e5e4f69a6a82ef435be50a46b2cfeea9405bbaa185cf6fcd17c32e553e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 KB (47663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f33a3554cb36b6dcc4f121a42c20cfa12694bc4f1fb1560cec6e443a93213fb`

```dockerfile
```

-	Layers:
	-	`sha256:bd04f9ba38a7934ac07bcb826bccb262b92a5803367bf017abc3dc18060c2e75`  
		Last Modified: Sat, 14 Mar 2026 03:02:04 GMT  
		Size: 47.7 KB (47663 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:apache` - linux; s390x

```console
$ docker pull yourls@sha256:b7e7195dc7d6662c536b5761a5b260db215fa8635df0072370691c1881e7ac96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.7 MB (161708742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c690e1d8293e2b7e7ec7de2701b058d9bdc1b724062cae0c104c3b67fd260cd7`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1771804800'
# Thu, 12 Mar 2026 23:25:31 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 12 Mar 2026 23:25:54 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 12 Mar 2026 23:25:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 12 Mar 2026 23:25:54 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Mar 2026 23:25:54 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Mar 2026 23:25:54 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 12 Mar 2026 23:25:54 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 12 Mar 2026 23:26:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 12 Mar 2026 23:26:01 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 12 Mar 2026 23:26:01 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 12 Mar 2026 23:26:01 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Mar 2026 23:26:01 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Mar 2026 23:26:01 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Mar 2026 23:26:01 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Thu, 12 Mar 2026 23:26:01 GMT
ENV PHP_VERSION=8.5.4
# Thu, 12 Mar 2026 23:26:01 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.4.tar.xz.asc
# Thu, 12 Mar 2026 23:26:01 GMT
ENV PHP_SHA256=c1569f1f543f6b025c583cdc0e730e5c5833c603618613f1aa8e75d1524b8c91
# Thu, 12 Mar 2026 23:26:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 12 Mar 2026 23:26:10 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Mar 2026 23:30:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Mar 2026 23:30:41 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Mar 2026 23:30:41 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Mar 2026 23:30:41 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Mar 2026 23:30:41 GMT
STOPSIGNAL SIGWINCH
# Thu, 12 Mar 2026 23:30:41 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 12 Mar 2026 23:30:41 GMT
WORKDIR /var/www/html
# Thu, 12 Mar 2026 23:30:41 GMT
EXPOSE map[80/tcp:{}]
# Thu, 12 Mar 2026 23:30:41 GMT
CMD ["apache2-foreground"]
# Fri, 13 Mar 2026 00:27:02 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)"     bcmath     pdo_mysql     mysqli # buildkit
# Fri, 13 Mar 2026 00:27:02 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Fri, 13 Mar 2026 00:27:02 GMT
RUN a2enmod rewrite expires # buildkit
# Fri, 13 Mar 2026 00:27:03 GMT
ARG YOURLS_VERSION=1.10.3
# Fri, 13 Mar 2026 00:27:03 GMT
ARG YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
# Fri, 13 Mar 2026 00:27:03 GMT
ENV YOURLS_VERSION=1.10.3
# Fri, 13 Mar 2026 00:27:03 GMT
ENV YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
# Fri, 13 Mar 2026 00:27:03 GMT
# ARGS: YOURLS_VERSION=1.10.3 YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Fri, 13 Mar 2026 00:27:03 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Fri, 13 Mar 2026 00:27:04 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Mar 2026 00:27:04 GMT
COPY files/vhost.conf /etc/apache2/sites-available/000-default.conf # buildkit
# Fri, 13 Mar 2026 00:27:04 GMT
COPY files/vhost-https.conf /etc/apache2/sites-available/default-ssl.conf # buildkit
# Fri, 13 Mar 2026 00:27:04 GMT
COPY files/ports.conf /etc/apache2/ports.conf # buildkit
# Fri, 13 Mar 2026 00:27:04 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 13 Mar 2026 00:27:04 GMT
EXPOSE map[8443/tcp:{}]
# Fri, 13 Mar 2026 00:27:04 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Fri, 13 Mar 2026 00:27:04 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:b50f587e37cdad2c774c5137974987f2b5aca2ef491f293c135b60e1e43e0135`  
		Last Modified: Tue, 24 Feb 2026 18:43:50 GMT  
		Size: 29.8 MB (29838179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0d1a248f9303e1fa5e2a7c523e205819414479821c10d403fae432f570aa37e`  
		Last Modified: Thu, 12 Mar 2026 23:31:00 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da2905080f9d09ea0b07e19780754f8f1935322caf9425d045ae6bebab0b292d`  
		Last Modified: Thu, 12 Mar 2026 23:31:02 GMT  
		Size: 92.6 MB (92572117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc0754b1bc5a336f979da71da16e221438ff759f3570041153e4228ddfc581a`  
		Last Modified: Thu, 12 Mar 2026 23:31:00 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:129c72d387e91f2da9e9398e94a0a90c84e51a2c7954326d5c5d3fd23bc013dc`  
		Last Modified: Thu, 12 Mar 2026 23:31:00 GMT  
		Size: 4.3 MB (4328920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cefa5010e262b69661bde2f3657ca838f2587c64b5f040fef0ced640b9b6e92b`  
		Last Modified: Thu, 12 Mar 2026 23:31:01 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:852ee76f00b06c57fc67e35cfe14cf5e53764382190763ffbf9b773bfb00b46f`  
		Last Modified: Thu, 12 Mar 2026 23:31:01 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dea0c73208aab0a867d829d91293264678eee39fcfe6968032e352fa5b4ffc5a`  
		Last Modified: Thu, 12 Mar 2026 23:31:01 GMT  
		Size: 14.5 MB (14513721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af4712f7c9b4c1d521280005159203d5d8cbfc1ce13b044e2a0cbf325c677ecc`  
		Last Modified: Thu, 12 Mar 2026 23:31:02 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2c1b185c1e73b99f502a272cd7f2c237cf31b979eb322cfa9e8c2e7e3225f76`  
		Last Modified: Thu, 12 Mar 2026 23:31:02 GMT  
		Size: 14.3 MB (14283854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79db4d5482062af36da882191cb421e5abe0e173cba415089b157ab700e578a8`  
		Last Modified: Thu, 12 Mar 2026 23:31:03 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:076ea80421c9ec923ad4f27b521b9ad615a6364767d92ee14f304b35a949288f`  
		Last Modified: Thu, 12 Mar 2026 23:31:03 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:532ba436e996f6c221573bec467adc54b8b6a5b1b3d0e324cb76a30742cfc5ab`  
		Last Modified: Thu, 12 Mar 2026 23:31:04 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd910f6ae6b2aaca9da25dc0bfa89e5ecdedc5311a841f826f1f20a1d15f4ce1`  
		Last Modified: Fri, 13 Mar 2026 00:27:12 GMT  
		Size: 111.7 KB (111697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:254510b167bcee2527a4ae667a201587bd744cdefde93cab84fc7b11526e6880`  
		Last Modified: Fri, 13 Mar 2026 00:27:12 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:462d78d80542b31f41915c56d947563cca22961ac21bf424e94119323edda0ad`  
		Last Modified: Fri, 13 Mar 2026 00:27:12 GMT  
		Size: 346.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43a1f2bebb13d01b8e5faf74aa623bb83efdd4e810350adad3313cb05da61888`  
		Last Modified: Fri, 13 Mar 2026 00:27:12 GMT  
		Size: 6.0 MB (6048925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e6c477698ecf1221d75642a52773ac679d608a360f4b8078dcab89dfe18213`  
		Last Modified: Fri, 13 Mar 2026 00:27:13 GMT  
		Size: 2.1 KB (2096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a59ab46b880472264443e8f5c1a8c8ddf0f389ac4217d271cbaaff009f9859a1`  
		Last Modified: Fri, 13 Mar 2026 00:27:13 GMT  
		Size: 1.7 KB (1694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a0cb97cf959342c4a04ec7ba01c9c1e793aa1a014cb9d96c01fed11e2ab3e39`  
		Last Modified: Fri, 13 Mar 2026 00:27:13 GMT  
		Size: 502.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6231faa3b8e03b19d95efdf89db38db1e2f8ad8de92f3161f7b50339aaf2fba9`  
		Last Modified: Fri, 13 Mar 2026 00:27:14 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b011b003a4a33c6e7fc234f79e4779aee07d6076db64f00414d6ee5bace44a69`  
		Last Modified: Fri, 13 Mar 2026 00:27:14 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:apache` - unknown; unknown

```console
$ docker pull yourls@sha256:82382e88f9686b033fd192d00a77c88c58e182ca4b3deb023a3f8cc6c9f589a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.6 KB (47579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fecdea968861788f6bc3986f17a848d4065ed1827037af3973234acbe1dc727`

```dockerfile
```

-	Layers:
	-	`sha256:769114265ecc1b1b52608063ea7049129a59a60473d4be1ff66174821eb05a99`  
		Last Modified: Fri, 13 Mar 2026 00:27:12 GMT  
		Size: 47.6 KB (47579 bytes)  
		MIME: application/vnd.in-toto+json
