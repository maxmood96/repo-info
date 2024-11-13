## `matomo:apache`

```console
$ docker pull matomo@sha256:8fe631db0f8a2da593e588458d8c34f66f3ee25b0b6de3f882d53c4cbc11f54a
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

### `matomo:apache` - linux; amd64

```console
$ docker pull matomo@sha256:627554f657b7e1771411596384610f485c8d7569d0a1e9030bae722b16c6beb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.9 MB (201872663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92d6e042d3c30cf254cba0902960c44881e9419c6e3a503598c63c7af769ab29`
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
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:400f75d9900933d30012ae07a280ee314031d6a2601fe469564c57626344628a`  
		Last Modified: Tue, 12 Nov 2024 02:35:50 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e532b66579ca9090a88a11bcdf58bc8e3a1905bfa119ce4b8ae488acba54ca93`  
		Last Modified: Tue, 12 Nov 2024 02:35:52 GMT  
		Size: 104.3 MB (104345685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ac50b358b78087371933f3818b150ef49b93a4f520a04c6942d6e5966c97fad`  
		Last Modified: Tue, 12 Nov 2024 02:35:50 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8ecb69d311b1181be24831dde5171ea00f5e4d6bed8d31e51d620106415aaaf`  
		Last Modified: Tue, 12 Nov 2024 02:35:50 GMT  
		Size: 20.1 MB (20123880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c047dfa11941ada6ddbe46380f704a04a17f208756469239974a7af0df7378d0`  
		Last Modified: Tue, 12 Nov 2024 02:35:51 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef42461ff613cf822d2b86e0063b7d0599c29de666a23ef2ba283a86a24c1a88`  
		Last Modified: Tue, 12 Nov 2024 02:35:51 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c524fd1548ce282b7066301e749020ccd5aa2863cb86531c47c58e092404d93`  
		Last Modified: Tue, 12 Nov 2024 02:35:52 GMT  
		Size: 12.3 MB (12254756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50edcb1570eff66dd9e3b25933366082da74bf20ea6e96457b8a039a5ee0c517`  
		Last Modified: Tue, 12 Nov 2024 02:35:51 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb08836f49b3f0d2273b0462d9adc33862bd8728182d43cd49efaead28aeb67e`  
		Last Modified: Tue, 12 Nov 2024 02:35:52 GMT  
		Size: 11.4 MB (11409884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c23822149981d4e949a62c840ed95968ad6435207101bed113cb17c69e7d9ff`  
		Last Modified: Tue, 12 Nov 2024 02:35:52 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3e55308e305faad7e8a7364cd3103e3393c916147a4e5713684137201c2588`  
		Last Modified: Tue, 12 Nov 2024 02:35:53 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f217c2e0f353496b2100626fbcdfde08d294f33435bfe71a85b11482ece6c1e`  
		Last Modified: Tue, 12 Nov 2024 02:35:53 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22ba270a6b954d8ddb0ab5f7f4e93d46cd3fae5f14e8d6e960b4fb7e1c6783f`  
		Last Modified: Tue, 12 Nov 2024 03:10:05 GMT  
		Size: 3.3 MB (3255835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6979e27bd3220d6f27b82f88ce9aa15647bb50475af11e43326366dc4417fb79`  
		Last Modified: Tue, 12 Nov 2024 03:10:04 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b41453d0591b7de2f9fcd969670c23b9aa56416fdb44c20ba6dc61f2c976ad3`  
		Last Modified: Tue, 12 Nov 2024 03:10:05 GMT  
		Size: 21.3 MB (21347666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d6406eb24f744382991d34b207113301268666a02da73f6e09b2a809088691c`  
		Last Modified: Tue, 12 Nov 2024 03:10:04 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a64e51263d3b0c53718d3b8b1dde34665d59953c4dfc0f578f16d52ae64598fc`  
		Last Modified: Tue, 12 Nov 2024 03:10:05 GMT  
		Size: 823.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:apache` - unknown; unknown

```console
$ docker pull matomo@sha256:5222e04401ca1eff9d8220b25da6bde57f5c3d43617fdb39113d0b8aced93a66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 KB (36373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8de336e5742d84a74a234a9724b018aafaffe4b5be94c5e9326f64536d37ee30`

```dockerfile
```

-	Layers:
	-	`sha256:be737ed124abb887da16c49072af55e70e1043fc5522a4217f030dcca68a0e9e`  
		Last Modified: Tue, 12 Nov 2024 03:10:04 GMT  
		Size: 36.4 KB (36373 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:apache` - linux; arm variant v5

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

### `matomo:apache` - unknown; unknown

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

### `matomo:apache` - linux; arm variant v7

```console
$ docker pull matomo@sha256:66b29c5324e75bb84f162338e15f6f5de5c73acfbbffe211ec2f0f7b75ab9a85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.8 MB (165771603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e0359c89733ea290263f586a3ac2f5bb4e62441b36c59c4215edd0adefa6ada`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 25 Sep 2024 20:44:12 GMT
ADD file:e76e8ba7ebca0b1dcaec16ad1e863ab59c7e155f0b95ba46f5543e418a904b35 in / 
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
	-	`sha256:d6319e551f4eae5cadf245338228c7b7cbad94a77c481a88ccbffef7b89f0aee`  
		Last Modified: Thu, 17 Oct 2024 03:06:55 GMT  
		Size: 24.7 MB (24718197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bcfcb380cfbd1992d2f15637ef37999cbc4f9934874d34a17b217098fa8c2f4`  
		Last Modified: Mon, 28 Oct 2024 22:06:03 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63df587ed65ffaf4f0e56a3ade450a0c2f4bd0ec52cb90e0193d9ec9a394a939`  
		Last Modified: Mon, 28 Oct 2024 22:06:06 GMT  
		Size: 76.2 MB (76163014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7f4e906cd29de73704abed83d01761162847c368f1a7c597dc584fd985a75c2`  
		Last Modified: Mon, 28 Oct 2024 22:06:03 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b42cf4a791cfd52dd382314b8b0f4cbf7a46e61d6c6c664a4299bfc5656b5a8`  
		Last Modified: Mon, 28 Oct 2024 22:11:48 GMT  
		Size: 18.9 MB (18857494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95bf1529cc0e5c50582fc58382ef311e785b9a8a182db98e8831efef019fe199`  
		Last Modified: Mon, 28 Oct 2024 22:11:48 GMT  
		Size: 435.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fca32620845d0574b19199a5b046dcb2260722f191ef3f55c582ed51287e788`  
		Last Modified: Mon, 28 Oct 2024 22:11:48 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91f17dd877da997c8a90b113b7a3a4de0ee78417ba4b164a23a9777eef7dd204`  
		Last Modified: Tue, 29 Oct 2024 00:25:10 GMT  
		Size: 12.3 MB (12253195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:748f43683d049b79e391e67b566556cb312d20c9370a01c10ccebd349ca230ee`  
		Last Modified: Tue, 29 Oct 2024 00:25:10 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c00ff6f81dc6513808f18442c74f3b43791ec1b5da394df42d1324ae52fe537a`  
		Last Modified: Tue, 29 Oct 2024 00:25:10 GMT  
		Size: 9.8 MB (9824909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c316f912b8a7b2e76994f1fc1b878024fd4b659844a75a282abca38a7ba31b39`  
		Last Modified: Tue, 29 Oct 2024 00:25:09 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b196057f12e508610b6fc95d578535e1364909ce3f68af288c92b405317b59b2`  
		Last Modified: Tue, 29 Oct 2024 00:25:10 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ced0ecd09dbb9fd88729e8c4351c27230f165445c0bebb94f5e31c3265985eb`  
		Last Modified: Tue, 29 Oct 2024 00:25:11 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:407916ac00be89daf0cec5fa8a9f82e05ff0e2a492d1318a4b231c34e68a9c79`  
		Last Modified: Tue, 29 Oct 2024 03:51:23 GMT  
		Size: 2.6 MB (2602002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf8acb44138f6a827be1957733dbb02998866c66e31c1acce94a73ccbbb2f83`  
		Last Modified: Tue, 29 Oct 2024 03:51:22 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9ce28a6458016b8e98fca31f33b54f8ee6a3b95b123a8d7d45475d5a8726b9`  
		Last Modified: Tue, 29 Oct 2024 03:51:23 GMT  
		Size: 21.3 MB (21345814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3a1f54497ec293c41467baa08a1f1d1dac76825dce789f9d3152a2e78b3ac93`  
		Last Modified: Tue, 29 Oct 2024 03:51:22 GMT  
		Size: 342.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f99ebff92fbb1ae8dde9b9401132fb3b6bb270634e983a5aa68cf0dcf8156565`  
		Last Modified: Tue, 29 Oct 2024 03:51:23 GMT  
		Size: 823.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:apache` - unknown; unknown

```console
$ docker pull matomo@sha256:18b333a05ac735d6865e66e333e4fa12276a812057ba9e37d702e8a50e8f7879
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.5 KB (36530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bf7d9c2dd257014409acc26ccf70438f5b7e1f4c02c4a7f398c7e981a552e04`

```dockerfile
```

-	Layers:
	-	`sha256:d3d4e21635005154ede004069fbac2d08c090a88f7e617119aec2b55c7c8d476`  
		Last Modified: Tue, 29 Oct 2024 03:51:22 GMT  
		Size: 36.5 KB (36530 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:apache` - linux; arm64 variant v8

```console
$ docker pull matomo@sha256:208b18f82ed76fa677d2db8f31e869db7aa3ac0590612e76b44b70b811f2ce93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.9 MB (195936031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7af6c7cef4898cad06e2fc95ca5229fd094dff12e2cd7fd4e8d82605ac42d98b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 25 Sep 2024 20:44:12 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
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
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77074644eeb7cdf46475293fba2c88bbb04a0d4639f8fe1072fb11d7a6434fb4`  
		Last Modified: Mon, 28 Oct 2024 22:03:20 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1844b6c933ada1472f6f12b5dab5dbb974ff7c8299bc6ba9312586feada41bf1`  
		Last Modified: Mon, 28 Oct 2024 22:03:23 GMT  
		Size: 98.1 MB (98130054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d350ecad63f801fc61e8fb71f1da4b5052fb1caae60ea46e1ab87d2c3cd4ae7`  
		Last Modified: Mon, 28 Oct 2024 22:03:20 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b420f8be6082fd2562efa3ab5c5be52021e75fc1ad60aad50264cc70250ea8e6`  
		Last Modified: Mon, 28 Oct 2024 22:07:10 GMT  
		Size: 20.1 MB (20120934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10bb8443b199e35f18d67d4df1195046c90b460eafe7450bdddc9b0b0b45531b`  
		Last Modified: Mon, 28 Oct 2024 22:07:09 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65caf96ff18c89bce6dd79217c16e38c511df6d517eb60ca2ec174387a81a432`  
		Last Modified: Mon, 28 Oct 2024 22:07:09 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e9b3bc8b26f6a5a92ffbc06ad21656a2707305832a76b0fa28f313b5625bfb2`  
		Last Modified: Tue, 29 Oct 2024 00:00:56 GMT  
		Size: 12.3 MB (12254536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8d51fa612b7c5c6cf9f22ef3eccbda3a5e594b6460e11433c9c888e2f66d1ab`  
		Last Modified: Tue, 29 Oct 2024 00:00:55 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7799b0cdc2a8ca2df3ec16c24c1bd7ba7b3f9692f3e6ce2b22900c93b9832641`  
		Last Modified: Tue, 29 Oct 2024 00:00:56 GMT  
		Size: 11.4 MB (11417332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b4c59e9f8a34fdcb604f7a858f3dfe169d4274ba52f5e42688893b95e3bf75f`  
		Last Modified: Tue, 29 Oct 2024 00:00:55 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73298e8100b0009502d517a801ae75e03654a75e76c0043743227ecd5a17a606`  
		Last Modified: Tue, 29 Oct 2024 00:00:56 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c04fb95a44d07c7a96f3ed4d463be60f41bae3da8a87e83ab65cd4c27a04f0c`  
		Last Modified: Tue, 29 Oct 2024 00:00:56 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7208e4664e177dbce7c46ddac336c4aeb0aace0e792124a118e6cfe702651e20`  
		Last Modified: Tue, 29 Oct 2024 04:16:10 GMT  
		Size: 3.5 MB (3502489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2720cc9b931d63ee5882b14e67d4c3346dbb05b705210347dd7bbf96b13a59d`  
		Last Modified: Tue, 29 Oct 2024 04:16:09 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3c82021cb285d7ea8ec0d646ab9c18cb5b76b1107798ee68f91c2d4b5557911`  
		Last Modified: Tue, 29 Oct 2024 04:16:10 GMT  
		Size: 21.3 MB (21347380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1408ffffc1121274f62a764b72ec3c34dc233fb2a0b61b613f3d493c321cc377`  
		Last Modified: Tue, 29 Oct 2024 04:16:09 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c9f89ba311384087176ad01aa9e6e6c10e12a876c452d4ca10f583f154cda03`  
		Last Modified: Tue, 29 Oct 2024 04:16:10 GMT  
		Size: 824.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:apache` - unknown; unknown

```console
$ docker pull matomo@sha256:f36573e94b7f5abb56dc85731eee634519a05e31b207c312a390111d73d01de0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.6 KB (36585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69b8816c87ab25c32a5801dbe5b14cf68db43b5dd76935e63e6cd33dbac33c5d`

```dockerfile
```

-	Layers:
	-	`sha256:a6bad13ac4926b6bfcf517a645b5eafe51a0530c9e63406ec234ec7ff3371e3d`  
		Last Modified: Tue, 29 Oct 2024 04:16:09 GMT  
		Size: 36.6 KB (36585 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:apache` - linux; 386

```console
$ docker pull matomo@sha256:ce6dc4acc1a00679e156f85e341d735d728a000028b6d763dd14b0cd3255b09a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.8 MB (200753970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9773615871a6f4e74c97a9814bc5418d35168db3e4452b34f20127aaa6347c33`
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
	-	`sha256:7379b58056e85869f90d8f78478cafd0c7468ad3b5085482a0850cee625a847a`  
		Last Modified: Tue, 12 Nov 2024 00:54:51 GMT  
		Size: 30.1 MB (30145450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e6aa68959e3142bef810ae40ce9d9fb27e8aee9ff4ae8634d70dca35f5fc4e5`  
		Last Modified: Tue, 12 Nov 2024 02:36:23 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16e621bc54389a6f4cc5195f76e44c98c06bea2f204a92b49ff9b5c2e8b012e0`  
		Last Modified: Tue, 12 Nov 2024 02:36:26 GMT  
		Size: 101.5 MB (101515043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f6833c9d664ad5005a990b8b5f5f9d7fc24ef88928bb6da2023075b78a98ac5`  
		Last Modified: Tue, 12 Nov 2024 02:36:14 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:365a9bdc5399c60371e8771ef0a38b9fe64fbb046be31fd5b859f91f9f896284`  
		Last Modified: Tue, 12 Nov 2024 02:36:24 GMT  
		Size: 20.6 MB (20638469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc4c46338eff630426f34653b21d0488b3bb16c93073fa52291f308b50da975c`  
		Last Modified: Tue, 12 Nov 2024 02:36:24 GMT  
		Size: 437.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:399974df35da6e022f4a2a50f56e70a355380268d1c9d3af38ac72e0105d3094`  
		Last Modified: Tue, 12 Nov 2024 02:36:24 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9f4640c43e435175f4c0e0600449beab7c1d3cd76fe3c600f143c52bf4df7d3`  
		Last Modified: Tue, 12 Nov 2024 02:36:25 GMT  
		Size: 12.3 MB (12254054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23328ade74f6167ee11a5782a1d7157e07ed4031652b522082ad12c02ef21917`  
		Last Modified: Tue, 12 Nov 2024 02:36:25 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50ace98562889741964d8e5699e9148e29110de00c2fdc5fa0df9250d2f0e968`  
		Last Modified: Tue, 12 Nov 2024 02:36:26 GMT  
		Size: 11.6 MB (11640486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e265d0896f0be609cb15bd9f78d78b47e5f51127b1c9260f50de7d0c9cd2ea8`  
		Last Modified: Tue, 12 Nov 2024 02:36:26 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:218b05273739a656a2a25f3d8a9142885eed375cb2a52f47081ebac9ca355ba7`  
		Last Modified: Tue, 12 Nov 2024 02:36:27 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26fb315c2ac5d41b19bcd26ace02ea591453735f2611b9d67f0ca8d33a6a76ac`  
		Last Modified: Tue, 12 Nov 2024 02:36:27 GMT  
		Size: 887.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea3908e37da243ac2c119ef1bad8a1f1079c23f707cb87508f9d6256d1cb66ad`  
		Last Modified: Tue, 12 Nov 2024 03:10:13 GMT  
		Size: 3.2 MB (3207012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1ee45f2d2ea548f4ed93f7fd0d0637e6c2d93cc9b8497263cfaab6f8a83af12`  
		Last Modified: Tue, 12 Nov 2024 03:10:13 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ccfcc4a62cb0142e0b31756f323433a79e489221f47ff671d81b93f33b6051f`  
		Last Modified: Tue, 12 Nov 2024 03:10:14 GMT  
		Size: 21.3 MB (21346493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4d635651dd941ddd422642cf41b00930423665d851a485d7171bbb18b0eefd4`  
		Last Modified: Tue, 12 Nov 2024 03:10:13 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3586e295cf5155a1e98b1f907081941d1018c25a56b67ec8a7a9e8bb9dc9246`  
		Last Modified: Tue, 12 Nov 2024 03:10:14 GMT  
		Size: 824.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:apache` - unknown; unknown

```console
$ docker pull matomo@sha256:b574f42548cb2a6efebb33f23d3559f19cbbd331c85828266f430fbbdb06b397
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.3 KB (36317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f49738a0bd3092ecd2e9f24b8021a898ad62f3724499c1a82b39538146153e00`

```dockerfile
```

-	Layers:
	-	`sha256:e3d203fb0ac5176f74d656bd550cd19047506542f686f23add156d9586cc96aa`  
		Last Modified: Tue, 12 Nov 2024 03:10:13 GMT  
		Size: 36.3 KB (36317 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:apache` - linux; mips64le

```console
$ docker pull matomo@sha256:29c0a4ad22c52de5b00fbe6172ba970df07e48fb506fbe58aa019453bd0ae56a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.8 MB (176786604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f67fd511e8a501e0c7544fcb8c161924a508bd3c48a533c91094ce0146ce754f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 25 Sep 2024 20:44:12 GMT
ADD file:6c11edc513b28b5a4034ee9c0d4cdcf019a82635ebb8a9e02732800fa457f683 in / 
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
	-	`sha256:8f9d02f0305fc460f51690aebcb328c22e13a197228c0910e24b813db943a15b`  
		Last Modified: Thu, 17 Oct 2024 01:18:03 GMT  
		Size: 29.1 MB (29124779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75971b85139441fe144cb93dcb63eda60c20b8b82bcc4cc161a345662be6e248`  
		Last Modified: Mon, 28 Oct 2024 22:20:30 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae54a087649536e7da942bb23de64ede6ba55259b78328b804de7695cf731369`  
		Last Modified: Mon, 28 Oct 2024 22:20:39 GMT  
		Size: 80.7 MB (80666666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf9d1ae69be6bff3b5f486ce83dc2a01329491bc64c77e183361743695495d62`  
		Last Modified: Mon, 28 Oct 2024 22:20:30 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9805e4def2c522f97a948ff0a106d6753819d71887cabeca9b1ab8355a0ec3f5`  
		Last Modified: Mon, 28 Oct 2024 22:40:31 GMT  
		Size: 20.1 MB (20069130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f108a36b91c4b30f45222f94048f45b028abb9cbd4872f312cc17b7ebdf9e0a`  
		Last Modified: Mon, 28 Oct 2024 22:40:28 GMT  
		Size: 436.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:badc8de30d0eaabcca7399faec8b52772f4a699389c0f6ee67d901929b205efb`  
		Last Modified: Mon, 28 Oct 2024 22:40:28 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f71e34b2800dfd629e12d65e7baccaaac611c653bf035588f288d647c6cb18d`  
		Last Modified: Tue, 29 Oct 2024 01:00:32 GMT  
		Size: 12.3 MB (12252938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a70c912fe40d48831bad52dcdc3407fdc46c13fdfa244a823b25cb875f194ec`  
		Last Modified: Tue, 29 Oct 2024 01:00:30 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edb0f1a43efa39a5c5633fe7071273c90673c2d33ccac2557b89a351ca8a140f`  
		Last Modified: Tue, 29 Oct 2024 01:00:32 GMT  
		Size: 10.5 MB (10490881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff006eac1edc92afd7e0e7d2fa3dcb515e4b395e7aefe397576166249ea625b2`  
		Last Modified: Tue, 29 Oct 2024 01:00:30 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93592b97a6b773a2f914323dfd205c121226db02040b6b8d1d9bf03470ae1cb7`  
		Last Modified: Tue, 29 Oct 2024 01:00:31 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcfa01b49e578511a4a4322d6fb0a2c9f8a40ad3a1abe992b3bf142d91c31169`  
		Last Modified: Tue, 29 Oct 2024 01:00:32 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:614ef77f0ee6c6787f8f5262674dd9ef6ab2556f1bfcccf7a0206bea844ef5d7`  
		Last Modified: Tue, 29 Oct 2024 05:31:24 GMT  
		Size: 2.8 MB (2829716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ca2500494367532f16bd35105a8c131b0a05cfe821f77a23a393fc1f0590d8f`  
		Last Modified: Tue, 29 Oct 2024 05:31:24 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17a68578b255c920bd75db227ccc0a15011a35226013467da3f59739ffadd401`  
		Last Modified: Tue, 29 Oct 2024 05:31:26 GMT  
		Size: 21.3 MB (21345513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9322276dd3e25b1cb978dc1fb7d6495b4845380c3e4952b163c706599a2f6e0d`  
		Last Modified: Tue, 29 Oct 2024 05:31:24 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f8329f13f325e829b42776fd68857b73468e2d8115b64dac2f2661060ba3b2e`  
		Last Modified: Tue, 29 Oct 2024 05:31:25 GMT  
		Size: 823.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:apache` - unknown; unknown

```console
$ docker pull matomo@sha256:46340a35335e811c12099a55882d4495b6450887f8044f5d53f1e20327bcff83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.5 KB (36511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d92881d86dffa9b12f42f0b24b569d4517b1fa89762599024562a274afb8acb`

```dockerfile
```

-	Layers:
	-	`sha256:bc90e096f8ea5c42c5387905863c874db69b5db674559459b4be9b80fe7f1ccd`  
		Last Modified: Tue, 29 Oct 2024 05:31:23 GMT  
		Size: 36.5 KB (36511 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:apache` - linux; ppc64le

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

### `matomo:apache` - unknown; unknown

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

### `matomo:apache` - linux; s390x

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

### `matomo:apache` - unknown; unknown

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
