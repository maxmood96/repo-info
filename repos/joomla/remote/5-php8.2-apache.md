## `joomla:5-php8.2-apache`

```console
$ docker pull joomla@sha256:11c303b481fdb4568c75ca04e4ad160f6dc34865063447930fed49a64e2ca448
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

### `joomla:5-php8.2-apache` - linux; amd64

```console
$ docker pull joomla@sha256:2c65adf564eb19d45a3f19cd0569b1aa0d342d6419eee65aaf1949764dd616c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.3 MB (274251036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9f2803ad669829e2bf25c548ed0c9a91b1e71ff00330a2d057eb15dd3cb9d54`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:26:57 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 08 May 2026 19:27:11 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 08 May 2026 19:27:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 19:27:11 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 08 May 2026 19:27:11 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 08 May 2026 19:27:11 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 08 May 2026 19:27:11 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 08 May 2026 19:30:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 08 May 2026 19:30:22 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 08 May 2026 19:30:22 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 08 May 2026 19:30:22 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 19:30:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 19:30:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 08 May 2026 19:30:22 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Fri, 08 May 2026 19:30:22 GMT
ENV PHP_VERSION=8.2.31
# Fri, 08 May 2026 19:30:22 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.31.tar.xz.asc
# Fri, 08 May 2026 19:30:22 GMT
ENV PHP_SHA256=95eae411d594fe6f6e5678b76645dc13ae47d3c0a5325c1d969b58dea56ee45a
# Fri, 08 May 2026 19:30:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 08 May 2026 19:30:30 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:32:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 May 2026 19:32:54 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:32:54 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 08 May 2026 19:32:54 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 May 2026 19:32:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 May 2026 19:32:54 GMT
STOPSIGNAL SIGWINCH
# Fri, 08 May 2026 19:32:54 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:32:54 GMT
WORKDIR /var/www/html
# Fri, 08 May 2026 19:32:54 GMT
EXPOSE map[80/tcp:{}]
# Fri, 08 May 2026 19:32:54 GMT
CMD ["apache2-foreground"]
# Fri, 08 May 2026 20:33:05 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Fri, 08 May 2026 20:33:05 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Fri, 08 May 2026 20:33:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:34:59 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libicu-dev 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libmagickwand-dev 		libpq-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	pecl install APCu-5.1.26; 	pecl install memcached-3.3.0; 	pecl install redis-6.2.0; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Fri, 08 May 2026 20:34:59 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 08 May 2026 20:34:59 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Fri, 08 May 2026 20:34:59 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Fri, 08 May 2026 20:34:59 GMT
VOLUME [/var/www/html]
# Fri, 08 May 2026 20:34:59 GMT
ENV JOOMLA_VERSION=5.4.5
# Fri, 08 May 2026 20:34:59 GMT
ENV JOOMLA_SHA512=b13e34397de1c386d6f083ed10b785b507dce5d685cd7388a6d4f6ac9d1497bf8d927c58d4b8847c223eb5886dd1da7357d9ce73a591e04ac66e64c7bfd543f9
# Fri, 08 May 2026 20:35:02 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/5.4.5/Joomla_5.4.5-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Fri, 08 May 2026 20:35:02 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 08 May 2026 20:35:02 GMT
COPY makedb.php /makedb.php # buildkit
# Fri, 08 May 2026 20:35:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 May 2026 20:35:02 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f091f5667dfe900008a0c3c24231a2fbe54aa21627ad9856dcb61667256a3ecc`  
		Last Modified: Fri, 08 May 2026 19:29:58 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:026378697a1f9c045350e6a6d7aacb364a45bb6d0429b5967ae3cd4633f8bda8`  
		Last Modified: Fri, 08 May 2026 19:30:01 GMT  
		Size: 117.8 MB (117843305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6c4048086a940e8e836b47a67d73270a8075a56988ad5d060a80319ba03dad1`  
		Last Modified: Fri, 08 May 2026 19:29:58 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b4c979a20ebc7dc1b09e229c509e7f6013cd176fc251149732f54ce0d76ff4c`  
		Last Modified: Fri, 08 May 2026 19:33:05 GMT  
		Size: 4.2 MB (4227812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0282102d7e2b22933ff137f2c44a0579861511ed12315323753aaf2eba877512`  
		Last Modified: Fri, 08 May 2026 19:33:05 GMT  
		Size: 433.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6c24858623a7d308d783a86215943f2ebfa10473685bcd24c77c12fd36e8102`  
		Last Modified: Fri, 08 May 2026 19:33:05 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7339e95193226cce4a55abcff6d10c381576e84e0781fad375d6c910ee74d0b9`  
		Last Modified: Fri, 08 May 2026 19:33:05 GMT  
		Size: 12.3 MB (12327110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da72641817f6f9dfadd419b9122386c9b29be2cbd8d422f69c819f1e706e2156`  
		Last Modified: Fri, 08 May 2026 19:33:06 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff2335fa2f3bcacfe79573dbe742506d7b32a89d98842b9e57f1e12a8a91fdcd`  
		Last Modified: Fri, 08 May 2026 19:33:06 GMT  
		Size: 11.5 MB (11460304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:498f16823e3d6d282eaa87e5e6415112ae69eaf7b7f5a8163c28c9bc6334b0bd`  
		Last Modified: Fri, 08 May 2026 19:33:06 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f42239b27787ac1276b2e9b044ae9301cb63b3429212adb595c9cfdfaceabf9`  
		Last Modified: Fri, 08 May 2026 19:33:07 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:458e870d099dc97fd68beaa5a7da69012ba5c2120aae01db8a32387761f407ec`  
		Last Modified: Fri, 08 May 2026 19:33:07 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c5dc5059db7e4eec4e7e52a81e2ac299d01093959b8027bd82d23341efc6050`  
		Last Modified: Fri, 08 May 2026 19:33:08 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e569901df577b22d7c2402189224af94b74757ec96bebe6f2cd739f5aeb8245d`  
		Last Modified: Fri, 08 May 2026 20:35:12 GMT  
		Size: 27.3 MB (27274107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff56c9e30d2be1a94f8ebdbe43b880ab9f7f29e5fbe38b0a0d2b8bb5bde14b34`  
		Last Modified: Fri, 08 May 2026 20:35:13 GMT  
		Size: 45.2 MB (45158435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53cdb9dcccbe2641c40170161c8d21f0a91ddc193de5afabeb412399ae70c84d`  
		Last Modified: Fri, 08 May 2026 20:35:10 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d8edfe00bd8a9cb5f502f2e5c837e9710b10a4854af777cd40e6902682b4bac`  
		Last Modified: Fri, 08 May 2026 20:35:10 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec9031131c51f68183f68bd9576c14dd1beeb4aabfd9430cfbeb1ed9a3ca14c1`  
		Last Modified: Fri, 08 May 2026 20:35:11 GMT  
		Size: 18.8 KB (18797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72bff7ce8289dbacc2ae7ec24a7cbb79735e076a0e52c58885fc541ac4b1beaa`  
		Last Modified: Fri, 08 May 2026 20:35:12 GMT  
		Size: 26.1 MB (26149780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45dae37828aa227291deeb906f43c39ebb6b084936da41e0417be6218ecf7b72`  
		Last Modified: Fri, 08 May 2026 20:35:13 GMT  
		Size: 3.7 KB (3656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f3fd5ec8fedafa352aa916a057a6754870dcdc95d4c0c6ee5eafa01c6611d68`  
		Last Modified: Fri, 08 May 2026 20:35:13 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:5-php8.2-apache` - unknown; unknown

```console
$ docker pull joomla@sha256:83766d719b95a53e9b01ad9b4110a797826e5d42a8a95f7f965d5f7a01a6f196
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.5 KB (57469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ec2ef50714bec0bae31f1e4639ec21eb6a4152cdf2cf8db4ef2d2c8e6fe1f33`

```dockerfile
```

-	Layers:
	-	`sha256:09d05fa87c99723938004fb2145dd0a663474f73eafbcab61e5c92d55e7ce8d8`  
		Last Modified: Fri, 08 May 2026 20:35:10 GMT  
		Size: 57.5 KB (57469 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:5-php8.2-apache` - linux; arm variant v5

```console
$ docker pull joomla@sha256:665a372512ab409ad2491aa8c63f42fb99d8eb20b38844944ffcc2030b6495ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.4 MB (245447711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c4686cde0b174e7e4a0d392ac9ddac2988f628e24694315ca3bb10127e366ef`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:36:27 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 08 May 2026 20:36:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 08 May 2026 20:36:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 20:36:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 08 May 2026 20:36:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 08 May 2026 20:36:49 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 08 May 2026 20:36:49 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 08 May 2026 20:36:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 08 May 2026 20:36:59 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 08 May 2026 20:36:59 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 08 May 2026 20:36:59 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 20:36:59 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 20:36:59 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 08 May 2026 20:36:59 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Fri, 08 May 2026 20:36:59 GMT
ENV PHP_VERSION=8.2.31
# Fri, 08 May 2026 20:36:59 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.31.tar.xz.asc
# Fri, 08 May 2026 20:36:59 GMT
ENV PHP_SHA256=95eae411d594fe6f6e5678b76645dc13ae47d3c0a5325c1d969b58dea56ee45a
# Fri, 08 May 2026 20:37:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 08 May 2026 20:37:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 May 2026 20:40:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 May 2026 20:40:07 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 May 2026 20:40:07 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 08 May 2026 20:40:08 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 May 2026 20:40:08 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 May 2026 20:40:08 GMT
STOPSIGNAL SIGWINCH
# Fri, 08 May 2026 20:40:08 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 08 May 2026 20:40:08 GMT
WORKDIR /var/www/html
# Fri, 08 May 2026 20:40:08 GMT
EXPOSE map[80/tcp:{}]
# Fri, 08 May 2026 20:40:08 GMT
CMD ["apache2-foreground"]
# Fri, 08 May 2026 22:00:34 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Fri, 08 May 2026 22:00:34 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Fri, 08 May 2026 22:00:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 22:03:43 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libicu-dev 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libmagickwand-dev 		libpq-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	pecl install APCu-5.1.26; 	pecl install memcached-3.3.0; 	pecl install redis-6.2.0; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Fri, 08 May 2026 22:03:43 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 08 May 2026 22:03:43 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Fri, 08 May 2026 22:03:44 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Fri, 08 May 2026 22:03:44 GMT
VOLUME [/var/www/html]
# Fri, 08 May 2026 22:03:44 GMT
ENV JOOMLA_VERSION=5.4.5
# Fri, 08 May 2026 22:03:44 GMT
ENV JOOMLA_SHA512=b13e34397de1c386d6f083ed10b785b507dce5d685cd7388a6d4f6ac9d1497bf8d927c58d4b8847c223eb5886dd1da7357d9ce73a591e04ac66e64c7bfd543f9
# Fri, 08 May 2026 22:03:45 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/5.4.5/Joomla_5.4.5-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Fri, 08 May 2026 22:03:45 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 08 May 2026 22:03:45 GMT
COPY makedb.php /makedb.php # buildkit
# Fri, 08 May 2026 22:03:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 May 2026 22:03:45 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:8f774e9b92b540806fc05167db7ce09a3e1b12abdb9d496f7b8c82138656065a`  
		Last Modified: Fri, 08 May 2026 18:33:49 GMT  
		Size: 27.9 MB (27948200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67937f580179d5b65b32df92b32bf1ef18360c5b1e116614f996d4b9d8ae90b5`  
		Last Modified: Fri, 08 May 2026 20:40:26 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ef49d330403f39b5877f74222cc47709d2e5c5718ff958ff2f3ee4a0f1a12d9`  
		Last Modified: Fri, 08 May 2026 20:40:29 GMT  
		Size: 94.9 MB (94885288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbffd57de8026cd211e6c2ca36f136a490b377f26d589d5ba36d96a4bab4760c`  
		Last Modified: Fri, 08 May 2026 20:40:27 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9056bbd3844a26ad903cb21d5587d877e7e2beb94e9ba3f2c16a4e63545f8059`  
		Last Modified: Fri, 08 May 2026 20:40:27 GMT  
		Size: 4.1 MB (4090136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dea0db64a43b19663c37d6446bede812d4d5f2874a35f98b1760ebbdcec77295`  
		Last Modified: Fri, 08 May 2026 20:40:28 GMT  
		Size: 432.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6574994d1e1196793c97d69ae0e00f1996cf44be93f1da53452fdc4b09561d23`  
		Last Modified: Fri, 08 May 2026 20:40:28 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dac8f90242849b2a710f07176a0c98b3365455cbcb8de14d4b999a4a6ca6384`  
		Last Modified: Fri, 08 May 2026 20:40:29 GMT  
		Size: 12.3 MB (12324680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f434d984c89a095a50d75a1c5a02ccdae0db37a09ad148b90c893154ced8b9ec`  
		Last Modified: Fri, 08 May 2026 20:40:29 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f5b0154c176525a08138c985f8499b9747969f48602c963002e2d077d2a8258`  
		Last Modified: Fri, 08 May 2026 20:40:29 GMT  
		Size: 10.4 MB (10368180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c07f0335234da6257a66f47336fd73ba463e013c093bccb355e5b1fa53e6858`  
		Last Modified: Fri, 08 May 2026 20:40:30 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d231a50535f5bcc7f78c5dad3c18feab705673e2303f103e651f88990f22e87`  
		Last Modified: Fri, 08 May 2026 20:40:30 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15258a0e6f297e2c32214b5c07b739bd57fa1f21ea23c05bb2ac23994495889a`  
		Last Modified: Fri, 08 May 2026 20:40:31 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf03a7dc8dc197464ac97b79af634377d08452f9d58b335f7f03c496924aef7`  
		Last Modified: Fri, 08 May 2026 20:40:31 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24f536d4c9bfdb51b6a89bdc17048a95871e6883d6f9fa0b57eb99a807a82be5`  
		Last Modified: Fri, 08 May 2026 22:03:55 GMT  
		Size: 26.7 MB (26706884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4fd69c6c8e0c6c3febe15e7bb573238419465d9c53fa003ff91ca46e663ddf2`  
		Last Modified: Fri, 08 May 2026 22:03:56 GMT  
		Size: 42.9 MB (42944590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3894722ba79d42ddaa1c44e1d3ae76bf52b23425fcf9061b46e32cd5e9759ca2`  
		Last Modified: Fri, 08 May 2026 22:03:54 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67107ec248c21c6df485b9489f5cbcc3815edec150feefc31c2fa4d60467da3b`  
		Last Modified: Fri, 08 May 2026 22:03:54 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1fb92a8b30d601b552f14b71c74ae74e03c76a00078684d734ca2549be53420`  
		Last Modified: Fri, 08 May 2026 22:03:55 GMT  
		Size: 18.8 KB (18791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75bb0b17e21793e02c153be0183653466bb991ca144e51b8ba5f7e53fcd24a8a`  
		Last Modified: Fri, 08 May 2026 22:03:56 GMT  
		Size: 26.1 MB (26149802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6d91cf47d7331400a21a80c2fe41dac8eb97fac8b1cf3a580464d559484a360`  
		Last Modified: Fri, 08 May 2026 22:03:57 GMT  
		Size: 3.7 KB (3656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c99d81f605584210af7f82d504d5ec1d2a3625cd133a9802f8a9665746b346c`  
		Last Modified: Fri, 08 May 2026 22:03:58 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:5-php8.2-apache` - unknown; unknown

```console
$ docker pull joomla@sha256:100ff8386ec9e3fcfe37fdb8d02c8d26ced60ad779fe8e8ee4d71a9e6c100654
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.6 KB (57597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e782e1997f6e377ce17adfd1efb5da3ba94df06578a236f28c2e19845e249ab1`

```dockerfile
```

-	Layers:
	-	`sha256:d289db1629ad50acf6d947efb203ea9d5d9e7452d4c23047c723c7dfb02160e8`  
		Last Modified: Fri, 08 May 2026 22:03:54 GMT  
		Size: 57.6 KB (57597 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:5-php8.2-apache` - linux; arm variant v7

```console
$ docker pull joomla@sha256:593dcbea30ea6142a3534ae6367e018c475ea1f614df5c526304da77eddae27c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.8 MB (231821177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe4b072d82e6a194ac8d55386d91dd8bfd9beb39e72cdeae47e5f22e4ffa295e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:25:03 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 08 May 2026 19:25:21 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 08 May 2026 19:25:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 19:25:21 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 08 May 2026 19:25:21 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 08 May 2026 19:25:21 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 08 May 2026 19:25:21 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 08 May 2026 19:25:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 08 May 2026 19:25:28 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 08 May 2026 19:25:28 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 08 May 2026 19:25:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 19:25:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 19:25:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 08 May 2026 19:25:28 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Fri, 08 May 2026 19:25:28 GMT
ENV PHP_VERSION=8.2.31
# Fri, 08 May 2026 19:25:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.31.tar.xz.asc
# Fri, 08 May 2026 19:25:28 GMT
ENV PHP_SHA256=95eae411d594fe6f6e5678b76645dc13ae47d3c0a5325c1d969b58dea56ee45a
# Fri, 08 May 2026 19:25:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 08 May 2026 19:25:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:28:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 May 2026 19:28:16 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:28:16 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 08 May 2026 19:28:16 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 May 2026 19:28:16 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 May 2026 19:28:16 GMT
STOPSIGNAL SIGWINCH
# Fri, 08 May 2026 19:28:16 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:28:16 GMT
WORKDIR /var/www/html
# Fri, 08 May 2026 19:28:16 GMT
EXPOSE map[80/tcp:{}]
# Fri, 08 May 2026 19:28:16 GMT
CMD ["apache2-foreground"]
# Fri, 08 May 2026 21:42:18 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Fri, 08 May 2026 21:42:18 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Fri, 08 May 2026 21:42:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 21:45:03 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libicu-dev 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libmagickwand-dev 		libpq-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	pecl install APCu-5.1.26; 	pecl install memcached-3.3.0; 	pecl install redis-6.2.0; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Fri, 08 May 2026 21:45:03 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 08 May 2026 21:45:03 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Fri, 08 May 2026 21:45:03 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Fri, 08 May 2026 21:45:03 GMT
VOLUME [/var/www/html]
# Fri, 08 May 2026 21:45:03 GMT
ENV JOOMLA_VERSION=5.4.5
# Fri, 08 May 2026 21:45:03 GMT
ENV JOOMLA_SHA512=b13e34397de1c386d6f083ed10b785b507dce5d685cd7388a6d4f6ac9d1497bf8d927c58d4b8847c223eb5886dd1da7357d9ce73a591e04ac66e64c7bfd543f9
# Fri, 08 May 2026 21:45:05 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/5.4.5/Joomla_5.4.5-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Fri, 08 May 2026 21:45:05 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 08 May 2026 21:45:05 GMT
COPY makedb.php /makedb.php # buildkit
# Fri, 08 May 2026 21:45:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 May 2026 21:45:05 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:f1433620eadfdfe016c8054b954f619ae5bca159f35a9459c36a76d9ef4d39c3`  
		Last Modified: Fri, 08 May 2026 18:37:58 GMT  
		Size: 26.2 MB (26214912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:795500bae9b8954ee753386cdb00c6b1b0c1bd7b9518c2c1f664419d3a9125b7`  
		Last Modified: Fri, 08 May 2026 19:28:33 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bda0f82d5dea0a04a91a9a9ee3b7c3792bc1a05b1ec849fc3e82cd9afadb01c`  
		Last Modified: Fri, 08 May 2026 19:28:38 GMT  
		Size: 86.3 MB (86251480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3b8d63ec359a91228167b429ff31b5509c81dcae81fa572587cfe8007e44441`  
		Last Modified: Fri, 08 May 2026 19:28:33 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e93cb3c94544a7caa7cef450f5787058fa92a73c5a518ba2c30aba7e48a6ca3c`  
		Last Modified: Fri, 08 May 2026 19:28:34 GMT  
		Size: 3.8 MB (3756708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:961c47f138e2f2bcfa9ad9b5d8aee08b328de98c33c8f31ca5461c6481b9e04e`  
		Last Modified: Fri, 08 May 2026 19:28:35 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9debb1f79134e0bcb246dd5d9791e843f37cab107889d2ecf1ff3f19b1a9529f`  
		Last Modified: Fri, 08 May 2026 19:28:35 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ede46976e84b2665b57461efffa99679ba0d6aa2a2b878dece887ac61275944`  
		Last Modified: Fri, 08 May 2026 19:28:36 GMT  
		Size: 12.3 MB (12324809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b52eed81a786527489be25fdc209ac1b3eb0f469b2dfac811e5766fefb4080d`  
		Last Modified: Fri, 08 May 2026 19:28:36 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac2a62a5ffb7209cac0616a4a2ea511d5f65bae564e008cbf19b097f29571877`  
		Last Modified: Fri, 08 May 2026 19:28:37 GMT  
		Size: 9.8 MB (9843074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67f90b5b2990e311b736b6a0dda2f20ce7e9f3336d69e9daf0751e52a51f1606`  
		Last Modified: Fri, 08 May 2026 19:28:38 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c418ce7b876b856cdf2538af181a05c69fce2d22b17cdc8f262152167f3ce7b`  
		Last Modified: Fri, 08 May 2026 19:28:38 GMT  
		Size: 254.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf3008d3b53c9b9f287240389493ad10347c42e82d6e1f7757f999d76df1320`  
		Last Modified: Fri, 08 May 2026 19:28:39 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44d04619fc7c9ef7e40f4f587e48ed7e4420c57a2d80c3a2f5b45098bb19ccfc`  
		Last Modified: Fri, 08 May 2026 19:28:39 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b77157f4e37c934cd8b5702ad5a57748cfde4aecae6ef57b8a038bfb19f0911`  
		Last Modified: Fri, 08 May 2026 21:45:14 GMT  
		Size: 25.9 MB (25925740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aab28d37ccb5ec8ada791ece5298a7fc4bfd6d3371d0e936ac84a0b30393522`  
		Last Modified: Fri, 08 May 2026 21:45:15 GMT  
		Size: 41.3 MB (41324675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:437d682b2e32c1cc855a1587bf9344481f24d8651014c92c108c628ef5bae408`  
		Last Modified: Fri, 08 May 2026 21:45:13 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fefbb43dc73dd100603ce7337e0e84c690467757552108988c072e4940f2d1b`  
		Last Modified: Fri, 08 May 2026 21:45:13 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5eedbe617dbbd4d9281fad5dc09296b38782d27e3ff6d75a56bddd9fd6e0433`  
		Last Modified: Fri, 08 May 2026 21:45:14 GMT  
		Size: 18.8 KB (18797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4232992719a34b0e7cf9ec2be90c65d148ef918e70c507094a375dfb01d1e80`  
		Last Modified: Fri, 08 May 2026 21:45:15 GMT  
		Size: 26.1 MB (26149806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e56cf493c524b7349aae8a740c0e1ee94ae170f1301df036af01a9d35c15fe5`  
		Last Modified: Fri, 08 May 2026 21:45:16 GMT  
		Size: 3.7 KB (3656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3da563a07dc284f05c69a69f343f1591b691d973774d947f47f8eadec319656e`  
		Last Modified: Fri, 08 May 2026 21:45:16 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:5-php8.2-apache` - unknown; unknown

```console
$ docker pull joomla@sha256:de911e70e460ec53c0dfbf36645a9ffc77e8c0925514f2a6ea316cc62b45b7c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.6 KB (57588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40b5638adf280e1ceeb0ea48816dbd296382bd0ef3bb127b338b3b02d47ba381`

```dockerfile
```

-	Layers:
	-	`sha256:02b2cbaa2ba7edc49c2952f93f039acf907ab8d8a024859167760f170fc6bc31`  
		Last Modified: Fri, 08 May 2026 21:45:13 GMT  
		Size: 57.6 KB (57588 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:5-php8.2-apache` - linux; arm64 variant v8

```console
$ docker pull joomla@sha256:1958fbbfaff57db20f6bdeab3ffda5e9b3059efccaefa7a9f2ce59b51cb4abf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.8 MB (265778804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:163b5901387aa3ffbdb036319d99a3b89300e764d7ca29f7f58a4d89f354d49c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:22:04 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 08 May 2026 19:22:20 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 08 May 2026 19:22:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 19:22:20 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 08 May 2026 19:22:20 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 08 May 2026 19:22:20 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 08 May 2026 19:22:20 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 08 May 2026 19:30:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 08 May 2026 19:30:04 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 08 May 2026 19:30:04 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 08 May 2026 19:30:04 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 19:30:04 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 19:30:04 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 08 May 2026 19:30:04 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Fri, 08 May 2026 19:30:04 GMT
ENV PHP_VERSION=8.2.31
# Fri, 08 May 2026 19:30:04 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.31.tar.xz.asc
# Fri, 08 May 2026 19:30:04 GMT
ENV PHP_SHA256=95eae411d594fe6f6e5678b76645dc13ae47d3c0a5325c1d969b58dea56ee45a
# Fri, 08 May 2026 19:30:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 08 May 2026 19:30:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:33:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 May 2026 19:33:46 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:33:46 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 08 May 2026 19:33:46 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 May 2026 19:33:46 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 May 2026 19:33:46 GMT
STOPSIGNAL SIGWINCH
# Fri, 08 May 2026 19:33:46 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:33:46 GMT
WORKDIR /var/www/html
# Fri, 08 May 2026 19:33:46 GMT
EXPOSE map[80/tcp:{}]
# Fri, 08 May 2026 19:33:46 GMT
CMD ["apache2-foreground"]
# Fri, 08 May 2026 20:39:44 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Fri, 08 May 2026 20:39:44 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Fri, 08 May 2026 20:39:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:42:09 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libicu-dev 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libmagickwand-dev 		libpq-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	pecl install APCu-5.1.26; 	pecl install memcached-3.3.0; 	pecl install redis-6.2.0; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Fri, 08 May 2026 20:42:09 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 08 May 2026 20:42:09 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Fri, 08 May 2026 20:42:09 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Fri, 08 May 2026 20:42:09 GMT
VOLUME [/var/www/html]
# Fri, 08 May 2026 20:42:09 GMT
ENV JOOMLA_VERSION=5.4.5
# Fri, 08 May 2026 20:42:09 GMT
ENV JOOMLA_SHA512=b13e34397de1c386d6f083ed10b785b507dce5d685cd7388a6d4f6ac9d1497bf8d927c58d4b8847c223eb5886dd1da7357d9ce73a591e04ac66e64c7bfd543f9
# Fri, 08 May 2026 20:42:11 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/5.4.5/Joomla_5.4.5-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Fri, 08 May 2026 20:42:11 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 08 May 2026 20:42:11 GMT
COPY makedb.php /makedb.php # buildkit
# Fri, 08 May 2026 20:42:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 May 2026 20:42:11 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7634e0d1223e12c48544304866bddf850cdc2eeab0345b500c30d6b2123e9cd`  
		Last Modified: Fri, 08 May 2026 19:26:00 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f53fe4c9fa1c2715fa42af575e4d63d04afcbaa9e7c0c0edb5c8e750b82637da`  
		Last Modified: Fri, 08 May 2026 19:26:04 GMT  
		Size: 110.2 MB (110165547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a6f9fe2a8a8e481bda2604a670dc10c7c8113debedf53d5f8c9f039d5d6f52b`  
		Last Modified: Fri, 08 May 2026 19:26:00 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:214228559e4202a744fadb5f36c83682051e6dc61db4a1fcfb72245f483f4328`  
		Last Modified: Fri, 08 May 2026 19:33:57 GMT  
		Size: 4.3 MB (4307891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abd4b46c2db47253d95139ea9fd357a17b04228e92167eb17a8385ffc8bb972f`  
		Last Modified: Fri, 08 May 2026 19:33:57 GMT  
		Size: 431.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d8e6d6dee582f1a7c86888d809c2c0c6092719d9c4d289a3fd13c89033156c`  
		Last Modified: Fri, 08 May 2026 19:33:57 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ab156d378e2e1996b1223a1791bc0aa11ff5d586dff50bac942543363cd5275`  
		Last Modified: Fri, 08 May 2026 19:33:57 GMT  
		Size: 12.3 MB (12326864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b89c120afee1c3d99207fb110731d92d96429a827acea26bbe6fe9165241ea3e`  
		Last Modified: Fri, 08 May 2026 19:33:58 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c87a069009b5e6ef76d06f7f0d2341c16b2888fcdd75736f92f71dd26f9874`  
		Last Modified: Fri, 08 May 2026 19:33:59 GMT  
		Size: 11.5 MB (11495252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36a975fdbecba66e92ccaf0239633393e9a989ef10794b71414bfe841ddea1d9`  
		Last Modified: Fri, 08 May 2026 19:33:59 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81c618fabffff404d995937f66224efec49616ae4747bb673cd0b82f32866907`  
		Last Modified: Fri, 08 May 2026 19:33:59 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47d49ed628e822b9fe84d716cd3f67ee4409b101d86c2f6adeb3b3fe658228fb`  
		Last Modified: Fri, 08 May 2026 19:33:59 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e60a960ba246aeee5639162b92b8deb87e3fa6b00125c7fd71188bb8a3b2f2a4`  
		Last Modified: Fri, 08 May 2026 19:34:00 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33d27add759a7cdf326e9c464e9b9250227b4dacf00176d784c826e15e4ad785`  
		Last Modified: Fri, 08 May 2026 20:42:21 GMT  
		Size: 27.1 MB (27100184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9c9ca803af964bb5e3fe2c1cf4bb109ef00f10700a9669fd71902eec9c6c67e`  
		Last Modified: Fri, 08 May 2026 20:42:22 GMT  
		Size: 44.1 MB (44059683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c0869b2d1c9ff3e409f4659c8e2c50e3aebec7102a3e0795ccb37bc511fa074`  
		Last Modified: Fri, 08 May 2026 20:42:19 GMT  
		Size: 309.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56a51fe01acc4db94884379c3b98c1e07e8eaf1dbaa9426d4319e3ed3fb6a0df`  
		Last Modified: Fri, 08 May 2026 20:42:20 GMT  
		Size: 385.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8b433ae246f6cdf5cdfb5b4b02e721e395e99c34f43574a79ae70a3b3154fc9`  
		Last Modified: Fri, 08 May 2026 20:42:21 GMT  
		Size: 18.8 KB (18794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7adb6630ee20e504e9fb1a8cc1a84a2289afb2f8611a8527c2264ddf77d84382`  
		Last Modified: Fri, 08 May 2026 20:42:22 GMT  
		Size: 26.1 MB (26149808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:963ef116de019f3d3d172aeeb74d51921a55f2dbc23346e59b5f757842cd26e5`  
		Last Modified: Fri, 08 May 2026 20:42:22 GMT  
		Size: 3.7 KB (3656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48a0d2d9d35800a4410eb80826aee798e7054afe77518f635812f70c3bb82fca`  
		Last Modified: Fri, 08 May 2026 20:42:23 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:5-php8.2-apache` - unknown; unknown

```console
$ docker pull joomla@sha256:a8fd1e14eb9295f135b967586805b0ecab9f80d514495c63546ef3e0327470ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.6 KB (57636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f42576d8cf7f08ef63739ea90d08586941f0ba39f2304b13ef9a8e8981b1771a`

```dockerfile
```

-	Layers:
	-	`sha256:7b927b13246f43c682bc5a6cf0f928963e4391c7da56e02813babd70442f7110`  
		Last Modified: Fri, 08 May 2026 20:42:19 GMT  
		Size: 57.6 KB (57636 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:5-php8.2-apache` - linux; 386

```console
$ docker pull joomla@sha256:bbafd15dbc1d23fdc38bb84c85afeabc740b63c1607568a3a1de27b368a18ce9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.2 MB (275195069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f52fba2a996c79faa48685cd60a246c6a933ce3705ac790f7010ad8c592f9fa1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:28:15 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 08 May 2026 19:28:35 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 08 May 2026 19:28:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 19:28:35 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 08 May 2026 19:28:35 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 08 May 2026 19:28:35 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 08 May 2026 19:28:35 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 08 May 2026 19:28:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 08 May 2026 19:28:41 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 08 May 2026 19:28:42 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 08 May 2026 19:28:42 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 19:28:42 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 19:28:42 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 08 May 2026 19:28:42 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Fri, 08 May 2026 19:28:42 GMT
ENV PHP_VERSION=8.2.31
# Fri, 08 May 2026 19:28:42 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.31.tar.xz.asc
# Fri, 08 May 2026 19:28:42 GMT
ENV PHP_SHA256=95eae411d594fe6f6e5678b76645dc13ae47d3c0a5325c1d969b58dea56ee45a
# Fri, 08 May 2026 19:28:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 08 May 2026 19:28:51 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:31:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 May 2026 19:31:44 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:31:44 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 08 May 2026 19:31:44 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 May 2026 19:31:44 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 May 2026 19:31:44 GMT
STOPSIGNAL SIGWINCH
# Fri, 08 May 2026 19:31:44 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:31:44 GMT
WORKDIR /var/www/html
# Fri, 08 May 2026 19:31:44 GMT
EXPOSE map[80/tcp:{}]
# Fri, 08 May 2026 19:31:44 GMT
CMD ["apache2-foreground"]
# Fri, 08 May 2026 23:11:48 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Fri, 08 May 2026 23:11:48 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Fri, 08 May 2026 23:11:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 23:14:03 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libicu-dev 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libmagickwand-dev 		libpq-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	pecl install APCu-5.1.26; 	pecl install memcached-3.3.0; 	pecl install redis-6.2.0; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Fri, 08 May 2026 23:14:04 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 08 May 2026 23:14:04 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Fri, 08 May 2026 23:14:04 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Fri, 08 May 2026 23:14:04 GMT
VOLUME [/var/www/html]
# Fri, 08 May 2026 23:14:04 GMT
ENV JOOMLA_VERSION=5.4.5
# Fri, 08 May 2026 23:14:04 GMT
ENV JOOMLA_SHA512=b13e34397de1c386d6f083ed10b785b507dce5d685cd7388a6d4f6ac9d1497bf8d927c58d4b8847c223eb5886dd1da7357d9ce73a591e04ac66e64c7bfd543f9
# Fri, 08 May 2026 23:14:05 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/5.4.5/Joomla_5.4.5-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Fri, 08 May 2026 23:14:05 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 08 May 2026 23:14:05 GMT
COPY makedb.php /makedb.php # buildkit
# Fri, 08 May 2026 23:14:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 May 2026 23:14:05 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:43e2ffbaa23260ffb4e3de716920f2ed9e6af56e465ca1233a2d84c2cc1cf005`  
		Last Modified: Fri, 08 May 2026 18:32:48 GMT  
		Size: 31.3 MB (31296400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0be1a1c4c68c25605a68908c1e1b859b69befd98d4660b616eb643db952bd65c`  
		Last Modified: Fri, 08 May 2026 19:32:05 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbf1b89303505cc80f25ad053e6fb887bef2105a56cecddad81d198bb88d0d5c`  
		Last Modified: Fri, 08 May 2026 19:32:08 GMT  
		Size: 116.1 MB (116144254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a812eae00e46443801eaea5a1afc105d757bdd9cfab5dc124c68b10c9f25957`  
		Last Modified: Fri, 08 May 2026 19:32:05 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cf582c16c27a3ff5ce30a9e400486413a7c4250494244997123933360f2e66b`  
		Last Modified: Fri, 08 May 2026 19:32:05 GMT  
		Size: 4.5 MB (4459071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8794c9677fba50329adf00c9c27844193460aec95b7ca4f8debb5d1becf7eee`  
		Last Modified: Fri, 08 May 2026 19:32:06 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ba116e5400347a234d7409db3c7c05ed2e2f45e988c2c8366c4d0b34836454d`  
		Last Modified: Fri, 08 May 2026 19:32:06 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d631acccaad71a39885a67676ea023b6b00b4082bdb28cc31218019693f42a04`  
		Last Modified: Fri, 08 May 2026 19:32:07 GMT  
		Size: 12.3 MB (12326212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5d6e19d34d5e5fc7b577684f1e8e27fdbf51c279cbc4e7fa17204402016eaf6`  
		Last Modified: Fri, 08 May 2026 19:32:07 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7024af85ee1e985b109012fcdd0af6bc5b1ac8c6cc8dd67a9f32d0713a181db5`  
		Last Modified: Fri, 08 May 2026 19:32:08 GMT  
		Size: 11.7 MB (11684339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10be3089ff09df92e93f620db879ba4430c7f30bf053329a0a6ae4b274bc57f6`  
		Last Modified: Fri, 08 May 2026 19:32:08 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faf25d18d50c9bef462ef83bb7887e475235308f43c61a0d66d51bde1a0ab92e`  
		Last Modified: Fri, 08 May 2026 19:32:09 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69eac9e94eed2107f989bad82174e7c5bc9f32c6c350b4c586d273acc7ed659e`  
		Last Modified: Fri, 08 May 2026 19:32:10 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6417422a32d62bf0e79b3c53a41f6d24ff831431ee5f7211339734542760165`  
		Last Modified: Fri, 08 May 2026 19:32:10 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51354a4c153d46811819d42b8eaf8497dac99d76d2b058c5389116e1f473bcb9`  
		Last Modified: Fri, 08 May 2026 23:14:15 GMT  
		Size: 27.7 MB (27716125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32a042fe3e39652065437b217fb016cb6dc6735ee64fb5459fd5368d3e09b68d`  
		Last Modified: Fri, 08 May 2026 23:14:15 GMT  
		Size: 45.4 MB (45388877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51ca470ecf81c4d08ad74b3caab895997794e810fe6bb64bc3a014650b83eca6`  
		Last Modified: Fri, 08 May 2026 23:14:14 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f2dfedace5a01cb965ce9be75e6f3d1a8ae46346fd84f16773d0ec9d35fe911`  
		Last Modified: Fri, 08 May 2026 23:14:14 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787b916386bdd307f6a0288dfba6534ced0c4d6581e65651b48c62718a78ead2`  
		Last Modified: Fri, 08 May 2026 23:14:15 GMT  
		Size: 18.8 KB (18794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6fa3bb2ef9ad0453669400e90becbefffe0751412a5b43322d279342589e486`  
		Last Modified: Fri, 08 May 2026 23:14:16 GMT  
		Size: 26.1 MB (26149836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d7422676efaef5c3950456ac4c3401d1f03d73e5514a9ffe17b2b61bc220295`  
		Last Modified: Fri, 08 May 2026 23:14:16 GMT  
		Size: 3.7 KB (3656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:020dcd9049ac894153503b511639b00321f94f839567e2b2f5af9bc557c3f1dd`  
		Last Modified: Fri, 08 May 2026 23:14:17 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:5-php8.2-apache` - unknown; unknown

```console
$ docker pull joomla@sha256:94a3777c83c8c2789de33c49f86539b652d89b429b8a3b4ba604f01aa17d84be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.4 KB (57432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6988f131bf11b013918e898f11879bcac8764c1379d9554812db4c01c37c3945`

```dockerfile
```

-	Layers:
	-	`sha256:27549346d3b6cad4e469eb26e2da5ada05d807dfe0e2a005ca1e187172527dac`  
		Last Modified: Fri, 08 May 2026 23:14:13 GMT  
		Size: 57.4 KB (57432 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:5-php8.2-apache` - linux; ppc64le

```console
$ docker pull joomla@sha256:6d0e831d6595ca300327b29e69f5577f493308f60c7a65dc0babacd0655442c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.8 MB (273816451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a486da2c35b4978f09f82b17fd260478d7b1187733695bc9785125cb2e4b686`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:49:52 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 08 May 2026 20:50:26 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 08 May 2026 20:50:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 20:50:26 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 08 May 2026 20:50:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 08 May 2026 20:50:27 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 08 May 2026 20:50:27 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 08 May 2026 20:52:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 08 May 2026 20:52:16 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 08 May 2026 20:52:17 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 08 May 2026 20:52:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 20:52:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 20:52:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 08 May 2026 20:52:17 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Fri, 08 May 2026 20:52:17 GMT
ENV PHP_VERSION=8.2.31
# Fri, 08 May 2026 20:52:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.31.tar.xz.asc
# Fri, 08 May 2026 20:52:17 GMT
ENV PHP_SHA256=95eae411d594fe6f6e5678b76645dc13ae47d3c0a5325c1d969b58dea56ee45a
# Fri, 08 May 2026 21:50:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 08 May 2026 21:50:19 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 May 2026 21:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 May 2026 21:54:12 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 May 2026 21:54:13 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 08 May 2026 21:54:13 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 May 2026 21:54:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 May 2026 21:54:13 GMT
STOPSIGNAL SIGWINCH
# Fri, 08 May 2026 21:54:13 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 08 May 2026 21:54:13 GMT
WORKDIR /var/www/html
# Fri, 08 May 2026 21:54:13 GMT
EXPOSE map[80/tcp:{}]
# Fri, 08 May 2026 21:54:13 GMT
CMD ["apache2-foreground"]
# Sat, 09 May 2026 04:25:03 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Sat, 09 May 2026 04:25:03 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Sat, 09 May 2026 04:25:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 09 May 2026 04:29:43 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libicu-dev 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libmagickwand-dev 		libpq-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	pecl install APCu-5.1.26; 	pecl install memcached-3.3.0; 	pecl install redis-6.2.0; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Sat, 09 May 2026 04:29:43 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Sat, 09 May 2026 04:29:43 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Sat, 09 May 2026 04:29:44 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Sat, 09 May 2026 04:29:44 GMT
VOLUME [/var/www/html]
# Sat, 09 May 2026 04:29:44 GMT
ENV JOOMLA_VERSION=5.4.5
# Sat, 09 May 2026 04:29:44 GMT
ENV JOOMLA_SHA512=b13e34397de1c386d6f083ed10b785b507dce5d685cd7388a6d4f6ac9d1497bf8d927c58d4b8847c223eb5886dd1da7357d9ce73a591e04ac66e64c7bfd543f9
# Sat, 09 May 2026 04:29:47 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/5.4.5/Joomla_5.4.5-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Sat, 09 May 2026 04:29:48 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Sat, 09 May 2026 04:29:48 GMT
COPY makedb.php /makedb.php # buildkit
# Sat, 09 May 2026 04:29:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 09 May 2026 04:29:48 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:b9baa45d89920bd180d7551ccc5bc535e0c5f55b863ddebddfdc06f9436dfe91`  
		Last Modified: Fri, 08 May 2026 19:46:53 GMT  
		Size: 33.6 MB (33598087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eec2632ee8119dd2f20ca1558eea30c9050dbe76cdeddfc47a82d2a99e3e922`  
		Last Modified: Fri, 08 May 2026 20:55:19 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07c7eeddeb286b4ad82e04422070cc9d0ea14c8385e61c160fdc6de15d44b838`  
		Last Modified: Fri, 08 May 2026 20:55:24 GMT  
		Size: 109.6 MB (109599289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9201651affe69dbeea0b40dd0a01797ab879ad276cbce7b1035fd2abbe6f32`  
		Last Modified: Fri, 08 May 2026 20:55:19 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e51c8a80d6a8bef8f0b2054c11688b31c933849cfa8969dad4e6902019fd92d`  
		Last Modified: Fri, 08 May 2026 20:57:14 GMT  
		Size: 4.9 MB (4883332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad0f49e69dc9fe4788a52a9279ee2ccb8d494fe3d8ff41454f9fb3a16f8054d7`  
		Last Modified: Fri, 08 May 2026 20:57:13 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4482f0abd8de4c23e09415b0ec42b86203a86547f87a68869616944382298375`  
		Last Modified: Fri, 08 May 2026 20:57:13 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:082387acd7a281d87c05c1a5c9eb94d76bd72ba6772ad77c7b658df791846f43`  
		Last Modified: Fri, 08 May 2026 21:54:35 GMT  
		Size: 12.3 MB (12333736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ca46e7b79953e5d7e05993eee4c18b65aab3b30a611da8b394dd7cd19e38c95`  
		Last Modified: Fri, 08 May 2026 21:54:35 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:128c019c28b60433dc7468b5c11c20a9bba17c900424e6b81553170dc52c133a`  
		Last Modified: Fri, 08 May 2026 21:54:35 GMT  
		Size: 11.9 MB (11872830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9457787595654bf638c1c12e61c9b8112e151062716365be051f0550b022e42`  
		Last Modified: Fri, 08 May 2026 21:54:35 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f117d7decd1fccdf82230de830d245cb19c7f5ede91ebab3df1b1e932bb20c6`  
		Last Modified: Fri, 08 May 2026 21:54:36 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8801ce7ee156bd7b5e38a21680fd097c6952fe4d6b6b545c63a7b5095d8612`  
		Last Modified: Fri, 08 May 2026 21:54:36 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e190dc0a45445b18d6f01c44988a68470acb558a2cc253f6e8434c0e679d4f30`  
		Last Modified: Fri, 08 May 2026 21:54:36 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105ad73d9962ffe987a79bea1a2e5df94693d4acbd689ba5b585652c02c8db07`  
		Last Modified: Sat, 09 May 2026 04:30:10 GMT  
		Size: 28.4 MB (28417932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c6e53f0f15ac60fcca39c5d0cef5ff791f508582dfc1f5fcc525011b3b52c4`  
		Last Modified: Sat, 09 May 2026 04:30:10 GMT  
		Size: 46.9 MB (46931455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f0c45f163364a2b4ac91238d16422a3d2b4f7cd0f9e88079880b1f5bee220ad`  
		Last Modified: Sat, 09 May 2026 04:30:08 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dc097ca86a0e5efbb321eb32fff783c9564983d5dab3086b961ad99d8be7f08`  
		Last Modified: Sat, 09 May 2026 04:30:08 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8221c5da9ebaaa06cc4386860904a8921891a353cb4035d6f6309ef3de171160`  
		Last Modified: Sat, 09 May 2026 04:30:09 GMT  
		Size: 18.8 KB (18807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87b0e5b58c58f41f1c0ba1da74ac76c94d2209ce8e8610aaddd1d45e1610cfdb`  
		Last Modified: Sat, 09 May 2026 04:30:10 GMT  
		Size: 26.1 MB (26149803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c481b9828b6f7f6cc1079b973e24f78d537ebf681456f8233ac4fb4127cf30ed`  
		Last Modified: Sat, 09 May 2026 04:30:11 GMT  
		Size: 3.7 KB (3656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:983c554f7c08b22a9aa65865e3b7a64fc3d52bdbcd7013ac65be4eb6367ad331`  
		Last Modified: Sat, 09 May 2026 04:30:11 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:5-php8.2-apache` - unknown; unknown

```console
$ docker pull joomla@sha256:0420eb2afb65dbbc8c2b4b3849f9debffcfc7904427de591dc5db3a59ebe7003
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.5 KB (57516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eac1d4251dcb1d93ceceac8446d4a36c88ad1c7ef3074d4c05da5b8ee7da2357`

```dockerfile
```

-	Layers:
	-	`sha256:8c175057dc8fe9fcd10a6414159a5f06950f8130077bea4926a3789914611ca9`  
		Last Modified: Sat, 09 May 2026 04:30:08 GMT  
		Size: 57.5 KB (57516 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:5-php8.2-apache` - linux; riscv64

```console
$ docker pull joomla@sha256:2e65a0e5cb1d217e59adef98f10653baaeaa8660a23d88c423af3101439f3c0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.2 MB (308230717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:921eaed61a72bf27d1765804a998837d4112669c0f8e1720dd019a321402121b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1777939200'
# Sat, 09 May 2026 21:54:02 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Sat, 09 May 2026 21:56:04 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 09 May 2026 21:56:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Sat, 09 May 2026 21:56:04 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 09 May 2026 21:56:04 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 09 May 2026 21:56:04 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 09 May 2026 21:56:04 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 09 May 2026 23:01:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Sat, 09 May 2026 23:01:52 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Sat, 09 May 2026 23:01:53 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Sat, 09 May 2026 23:01:53 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 09 May 2026 23:01:53 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 09 May 2026 23:01:53 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 09 May 2026 23:01:53 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Sat, 09 May 2026 23:01:53 GMT
ENV PHP_VERSION=8.2.31
# Sat, 09 May 2026 23:01:53 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.31.tar.xz.asc
# Sat, 09 May 2026 23:01:53 GMT
ENV PHP_SHA256=95eae411d594fe6f6e5678b76645dc13ae47d3c0a5325c1d969b58dea56ee45a
# Sun, 10 May 2026 09:55:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sun, 10 May 2026 09:55:44 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sun, 10 May 2026 10:40:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sun, 10 May 2026 10:40:30 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sun, 10 May 2026 10:40:31 GMT
RUN docker-php-ext-enable opcache # buildkit
# Sun, 10 May 2026 10:40:31 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sun, 10 May 2026 10:40:31 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sun, 10 May 2026 10:40:31 GMT
STOPSIGNAL SIGWINCH
# Sun, 10 May 2026 10:40:31 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Sun, 10 May 2026 10:40:32 GMT
WORKDIR /var/www/html
# Sun, 10 May 2026 10:40:32 GMT
EXPOSE map[80/tcp:{}]
# Sun, 10 May 2026 10:40:32 GMT
CMD ["apache2-foreground"]
# Tue, 12 May 2026 07:49:19 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Tue, 12 May 2026 07:49:19 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Tue, 12 May 2026 07:49:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 May 2026 08:16:30 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libicu-dev 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libmagickwand-dev 		libpq-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	pecl install APCu-5.1.26; 	pecl install memcached-3.3.0; 	pecl install redis-6.2.0; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 12 May 2026 08:16:31 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 12 May 2026 08:16:31 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 12 May 2026 08:16:33 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Tue, 12 May 2026 08:16:33 GMT
VOLUME [/var/www/html]
# Tue, 12 May 2026 08:16:33 GMT
ENV JOOMLA_VERSION=5.4.5
# Tue, 12 May 2026 08:16:33 GMT
ENV JOOMLA_SHA512=b13e34397de1c386d6f083ed10b785b507dce5d685cd7388a6d4f6ac9d1497bf8d927c58d4b8847c223eb5886dd1da7357d9ce73a591e04ac66e64c7bfd543f9
# Tue, 12 May 2026 08:16:45 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/5.4.5/Joomla_5.4.5-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Tue, 12 May 2026 08:16:46 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 12 May 2026 08:16:46 GMT
COPY makedb.php /makedb.php # buildkit
# Tue, 12 May 2026 08:16:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 May 2026 08:16:46 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:1e9edef871271ebe58c5a713c7c062e88ff414be0976a2c7baf0aba83823c954`  
		Last Modified: Fri, 08 May 2026 20:38:39 GMT  
		Size: 28.3 MB (28280232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a851920f3b2b9f32390e534dcffd1a0f98fdc6aa8d5199bfd378e81a327288ff`  
		Last Modified: Sat, 09 May 2026 22:59:56 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d0821c675bc014f36787754eae800bec2700775366123fdb7b93402865c4af1`  
		Last Modified: Sat, 09 May 2026 23:00:25 GMT  
		Size: 146.6 MB (146579482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:757b3119d655d94203c15aecf1cc2d93402f4523740a2527b967e186d7693c42`  
		Last Modified: Sat, 09 May 2026 22:59:56 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40fef68a865e77649624e332fc135889fa3e311fd92fbd55efb9283eaf669560`  
		Last Modified: Sun, 10 May 2026 00:03:23 GMT  
		Size: 4.0 MB (4031575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b336a94a4c9567b8427e54f2733c24a8a5678559cf7b51711a20ec3f8d801d63`  
		Last Modified: Sun, 10 May 2026 00:03:21 GMT  
		Size: 437.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:110b6e8491a8e810371841937507898364acf2bcba097426fe8b034aea28f887`  
		Last Modified: Sun, 10 May 2026 00:03:21 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e784f93e66dc2b8019db3391a244b1dab1edd17f6e8cb025132576f5daef4098`  
		Last Modified: Sun, 10 May 2026 10:43:35 GMT  
		Size: 12.3 MB (12341441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:073fa3e97271f014d294db4e95a8b42daad85fefb329f1d84738e2321ceedfaa`  
		Last Modified: Sun, 10 May 2026 10:43:31 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad458dc96d94ca081e0056bdad17f84bfa9e6550c148e5a1c0aa21820602650`  
		Last Modified: Sun, 10 May 2026 10:43:35 GMT  
		Size: 10.8 MB (10791662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5586c236731460dc34e2b14ebe8d631d108d301d39802bedd6b5c559c3be5b4c`  
		Last Modified: Sun, 10 May 2026 10:43:31 GMT  
		Size: 2.5 KB (2466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a89b821146a9310b04290246a43989820248926f24c62a4d077279771f16fd1c`  
		Last Modified: Sun, 10 May 2026 10:43:33 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0e52aaca6d5e1dd4bd0acd1c9c2085aa26b63cd077009e491f92284aa143ad0`  
		Last Modified: Sun, 10 May 2026 10:43:33 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7426ecc72aaee483c1869afc5546564df310db04141aa534b5739793bdd42cfa`  
		Last Modified: Sun, 10 May 2026 10:43:35 GMT  
		Size: 896.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e51cbc3561835960f81fc8b1c6ee5f58cbed798e22a0059f1360b81f2b6fbe76`  
		Last Modified: Tue, 12 May 2026 08:19:05 GMT  
		Size: 27.2 MB (27210741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf9dd5d702c49da3c8b485c5e2fe097a34302a12e69ca2ebb372b30d924f0ff4`  
		Last Modified: Tue, 12 May 2026 08:19:09 GMT  
		Size: 52.8 MB (52815752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43a5098db3b126bb61e0eff2728b157a4ba7dc3a1fbb215211131b24ab6299e4`  
		Last Modified: Tue, 12 May 2026 08:18:54 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17f9ac74feb4902b78e7addf297b3620909001f47d908cdc0bf071ae892c7f6e`  
		Last Modified: Tue, 12 May 2026 08:18:54 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fdbb28e80a839795b0f68929233435b28c4f3e8f058817536a387116e10b78d`  
		Last Modified: Tue, 12 May 2026 08:18:56 GMT  
		Size: 18.8 KB (18808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4856011bd00bf2f39db0d5d760fa599f2a9d2e40bbaef8e2b596d5b5492b5d19`  
		Last Modified: Tue, 12 May 2026 08:19:06 GMT  
		Size: 26.1 MB (26149825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee3918b15250495d2dd296e97bab401cc2c1e458e5ced4b05df2917eac15690b`  
		Last Modified: Tue, 12 May 2026 08:18:59 GMT  
		Size: 3.7 KB (3656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56102d128d5ef9bfdd0b1589f0a1f33605a41e2f3ad0a93879339499fc414807`  
		Last Modified: Tue, 12 May 2026 08:19:01 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:5-php8.2-apache` - unknown; unknown

```console
$ docker pull joomla@sha256:99b26b887713c862488ac0928c643c2b01cb948200aaa36c3e2137ddec72a0ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.5 KB (57515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dde47f24cc825f25a4c0f1d2e391ff609a1e7b361eeffc3d032ab0bdc960431`

```dockerfile
```

-	Layers:
	-	`sha256:25dc3129cdf52c254a7d4da990c855ba0aea9d8a77198019c1291832fbbecfaf`  
		Last Modified: Tue, 12 May 2026 08:18:54 GMT  
		Size: 57.5 KB (57515 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:5-php8.2-apache` - linux; s390x

```console
$ docker pull joomla@sha256:9e15e8f2b8b63ef1ddfd91afd6febe51b667ef0287bd1e7bcb3ad05e7b22b99d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.8 MB (248814254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8413bda317f388558c876efa7c1e3d66df454ef8c924a46598746b62e682c08b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:34:21 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 08 May 2026 19:34:43 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 08 May 2026 19:34:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 19:34:43 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 08 May 2026 19:34:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 08 May 2026 19:34:43 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 08 May 2026 19:34:43 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 08 May 2026 19:35:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 08 May 2026 19:35:38 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 08 May 2026 19:35:38 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 08 May 2026 19:35:38 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 19:35:38 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 19:35:38 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 08 May 2026 19:35:38 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Fri, 08 May 2026 19:35:38 GMT
ENV PHP_VERSION=8.2.31
# Fri, 08 May 2026 19:35:38 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.31.tar.xz.asc
# Fri, 08 May 2026 19:35:38 GMT
ENV PHP_SHA256=95eae411d594fe6f6e5678b76645dc13ae47d3c0a5325c1d969b58dea56ee45a
# Fri, 08 May 2026 19:59:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 08 May 2026 19:59:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 May 2026 20:03:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 May 2026 20:03:39 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 May 2026 20:03:40 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 08 May 2026 20:03:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 May 2026 20:03:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 May 2026 20:03:40 GMT
STOPSIGNAL SIGWINCH
# Fri, 08 May 2026 20:03:40 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 08 May 2026 20:03:40 GMT
WORKDIR /var/www/html
# Fri, 08 May 2026 20:03:40 GMT
EXPOSE map[80/tcp:{}]
# Fri, 08 May 2026 20:03:40 GMT
CMD ["apache2-foreground"]
# Fri, 08 May 2026 22:49:22 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Fri, 08 May 2026 22:49:22 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Fri, 08 May 2026 22:49:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 22:51:42 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libicu-dev 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libmagickwand-dev 		libpq-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	pecl install APCu-5.1.26; 	pecl install memcached-3.3.0; 	pecl install redis-6.2.0; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Fri, 08 May 2026 22:51:43 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 08 May 2026 22:51:43 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Fri, 08 May 2026 22:51:43 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Fri, 08 May 2026 22:51:43 GMT
VOLUME [/var/www/html]
# Fri, 08 May 2026 22:51:43 GMT
ENV JOOMLA_VERSION=5.4.5
# Fri, 08 May 2026 22:51:43 GMT
ENV JOOMLA_SHA512=b13e34397de1c386d6f083ed10b785b507dce5d685cd7388a6d4f6ac9d1497bf8d927c58d4b8847c223eb5886dd1da7357d9ce73a591e04ac66e64c7bfd543f9
# Fri, 08 May 2026 22:51:44 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/5.4.5/Joomla_5.4.5-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Fri, 08 May 2026 22:51:44 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 08 May 2026 22:51:44 GMT
COPY makedb.php /makedb.php # buildkit
# Fri, 08 May 2026 22:51:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 May 2026 22:51:44 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:2fbbc68c452b3ba3a496488f38159dac53afe693311bee1c04f555d854ff4a2e`  
		Last Modified: Fri, 08 May 2026 18:29:20 GMT  
		Size: 29.8 MB (29840347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8d1ae8e8dfc4770fdd123ecb7898605c813fac030d26ac659eb819aed4987b2`  
		Last Modified: Fri, 08 May 2026 19:39:58 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:152764c8b29d169484010780d4e0129b4cf3928183a3c8aab4689b1efc648a69`  
		Last Modified: Fri, 08 May 2026 19:40:01 GMT  
		Size: 92.6 MB (92573230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b279701afd4f9609f8e7b757e186ed9dbe4cb66b642fd4c8b7b430f8c207dca3`  
		Last Modified: Fri, 08 May 2026 19:39:58 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:443a2ae9467066af4a61c68a863c0d9e1cb13300cf313ae92c0ad4b99c07f95b`  
		Last Modified: Fri, 08 May 2026 19:40:59 GMT  
		Size: 4.3 MB (4331427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f675391d1fc0955022fd7f0e290d4813e23ca06fb22135134949afbe44d4ac98`  
		Last Modified: Fri, 08 May 2026 19:40:59 GMT  
		Size: 436.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7cebae6d33fb114425cf3f11ff4ec10f9f522e2611004923f62468194f3fc65`  
		Last Modified: Fri, 08 May 2026 19:40:59 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08286cb0e561cfc2f90245615b8e7e5adeb607511d1e945ce024d77b436268d7`  
		Last Modified: Fri, 08 May 2026 20:04:02 GMT  
		Size: 12.3 MB (12332222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1589874896b9edb533d1cbcfe19e9e6637a7cb293fc57acc21f8a33b8ca5770e`  
		Last Modified: Fri, 08 May 2026 20:04:01 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daedcc750bbec3312841bd6c19f5af50715554bcdfeb5c897031a487b3bca224`  
		Last Modified: Fri, 08 May 2026 20:04:03 GMT  
		Size: 11.3 MB (11327269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a199efa827b524cbd1fe93aad097c38e9307819b97bde9fa0d27061dee4c2247`  
		Last Modified: Fri, 08 May 2026 20:04:00 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26c25b2aca221a332a171a9a87228ba852c66c0c77af599c6baee5ec10bb61ec`  
		Last Modified: Fri, 08 May 2026 20:04:02 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5b8bdfcf8058ad24486e29619cae0e82abb096c9e54ca9e1b719f0404d3ffae`  
		Last Modified: Fri, 08 May 2026 20:04:02 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ff588b95a32c46e3551b4ddf1f97b3dc1b8a0997b4ed9d8e5c13cf44e213caa`  
		Last Modified: Fri, 08 May 2026 20:04:03 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:037a0296683cf4a25ccdd38ebf85f3dbd6d911a4a65bf87c224c437fb88a4445`  
		Last Modified: Fri, 08 May 2026 22:51:58 GMT  
		Size: 27.6 MB (27551523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf6ffd0c413beb037e55367a1916a2c086ae2c62fb3a69226907d620a1edbc2`  
		Last Modified: Fri, 08 May 2026 22:51:58 GMT  
		Size: 44.7 MB (44678461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:000f4c8ed97b591a9ce8dcd0ed0567ca7c6eeb70a6d84e5874930980d7517103`  
		Last Modified: Fri, 08 May 2026 22:51:57 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dadef94052692303689feb7ab90dba66b34963c2d380a91efa4deeecd3aa699`  
		Last Modified: Fri, 08 May 2026 22:51:57 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b43324f6c8ccf13463d385a37c094da44c6de0c148ef08f975750c8f7ddb43e4`  
		Last Modified: Fri, 08 May 2026 22:51:58 GMT  
		Size: 18.8 KB (18798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6122ddffc9c4e64f365cc3e9ef410a5a53ddbe588e7a141a915d5ad6171d945d`  
		Last Modified: Fri, 08 May 2026 22:51:59 GMT  
		Size: 26.1 MB (26149804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8397a4291154a3584e0d8375cf686c1ea4753f52413e633705d39d1ea9ee148c`  
		Last Modified: Fri, 08 May 2026 22:51:54 GMT  
		Size: 3.7 KB (3656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f27065360096a82184355aad74cee0919c63747d412a21fba42d78e09c61e18`  
		Last Modified: Fri, 08 May 2026 22:51:55 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:5-php8.2-apache` - unknown; unknown

```console
$ docker pull joomla@sha256:62ac5afac2f3095bb2b617546cbd58eea80b1386c2d25bf9185a9d9f6732e4cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.5 KB (57460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e55dcb179731081fd0cf29ffa552f4e1b01342f26a2274895677188964c6d87`

```dockerfile
```

-	Layers:
	-	`sha256:34364894192c10707f8f75f6306fba33e7293579d6bf6b956454229e84b01549`  
		Last Modified: Fri, 08 May 2026 22:51:57 GMT  
		Size: 57.5 KB (57460 bytes)  
		MIME: application/vnd.in-toto+json
