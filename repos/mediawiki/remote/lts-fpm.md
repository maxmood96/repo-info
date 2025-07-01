## `mediawiki:lts-fpm`

```console
$ docker pull mediawiki@sha256:a115e2c18f5b953f28d305e146c1d683ad5641af534e1ed11457cb9aae6327b0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
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

### `mediawiki:lts-fpm` - linux; amd64

```console
$ docker pull mediawiki@sha256:93fb7113a1ba4f9964552c09e79db621d278126865bf7db578ee9f3e108e0a70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.4 MB (321396095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8b6ffcc997c28c33fc86e38499da4ac07e42ca27b5cabcc4a40042d719e0fd9`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 10 Apr 2025 18:10:22 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 10 Apr 2025 18:10:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 10 Apr 2025 18:10:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 10 Apr 2025 18:10:22 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Thu, 10 Apr 2025 18:10:22 GMT
ENV PHP_VERSION=8.1.32
# Thu, 10 Apr 2025 18:10:22 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.32.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.32.tar.xz.asc
# Thu, 10 Apr 2025 18:10:22 GMT
ENV PHP_SHA256=c582ac682a280bbc69bc2186c21eb7e3313cc73099be61a6bc1d2cd337cbf383
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 10 Apr 2025 18:10:22 GMT
WORKDIR /var/www/html
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
STOPSIGNAL SIGQUIT
# Thu, 10 Apr 2025 18:10:22 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 10 Apr 2025 18:10:22 GMT
CMD ["php-fpm"]
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 		apt-get update; 	apt-get install -y --no-install-recommends 		git 		librsvg2-bin 		imagemagick 		python3 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libicu-dev 		libonig-dev 		liblua5.1-0-dev 	; 		docker-php-ext-install -j "$(nproc)" 		calendar 		intl 		mbstring 		mysqli 		opcache 	; 		pecl install APCu-5.1.24; 	pecl install LuaSandbox-4.1.2; 	docker-php-ext-enable 		apcu 		luasandbox 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 	mkdir -p /var/www/data; 	chown -R www-data:www-data /var/www/data # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
ENV MEDIAWIKI_MAJOR_VERSION=1.43
# Thu, 10 Apr 2025 18:10:22 GMT
ENV MEDIAWIKI_VERSION=1.43.1
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 	fetchDeps=" 		gnupg 		dirmngr 	"; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 		curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz" -o mediawiki.tar.gz; 	curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz.sig" -o mediawiki.tar.gz.sig; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 		D7D6767D135A514BEB86E9BA75682B08E8A3FEC4 		441276E9CCD15F44F6D97D18C119E1A64D70938E 		F7F780D82EBFB8A56556E7EE82403E59F9F8CD79 		1D98867E82982C8FE0ABC25F9B69B3109D3BB7B0 		E059C034E7A430583C252F4AA8F734246D73B586 	; 	gpg --batch --verify mediawiki.tar.gz.sig mediawiki.tar.gz; 	tar -x --strip-components=1 -f mediawiki.tar.gz; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" mediawiki.tar.gz.sig mediawiki.tar.gz; 	chown -R www-data:www-data extensions skins cache images; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:3da95a905ed546f99c4564407923a681757d89651a388ec3f1f5e9bf5ed0b39d`  
		Last Modified: Tue, 01 Jul 2025 01:14:43 GMT  
		Size: 28.2 MB (28230143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b73a248c8e29e7a39d07ff731f78e8d388aadbbfebf395c26c1915ac2d6db80`  
		Last Modified: Tue, 01 Jul 2025 02:25:12 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ef76c8c02583a020c56523a65354256e0f6e2cba2ec94c2c61271bdc78e1b2`  
		Last Modified: Tue, 01 Jul 2025 02:25:20 GMT  
		Size: 104.3 MB (104331319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7136b2f873f09020a594823332acdd8f49a508e31bb4189a67a08f0a121e90bf`  
		Last Modified: Tue, 01 Jul 2025 02:25:12 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fe2ada55707feb22f80e9419b4fadf2c1aa3caef73bfaab6ff777e0d4330d0e`  
		Last Modified: Tue, 01 Jul 2025 02:25:14 GMT  
		Size: 12.0 MB (12003220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c93762690989e9af3989c074bbdf412091f57edf25c08bcd07e85ff83d39dbac`  
		Last Modified: Tue, 01 Jul 2025 02:25:12 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44fa28ff51dc601b89e48c3eb3a6f92fac5928e750b8d6d0ce41a1a03ace1afd`  
		Last Modified: Tue, 01 Jul 2025 02:25:14 GMT  
		Size: 27.3 MB (27331112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94c4277911da42a05a298d16db80b1defff06bcd021c5d8ba7f23ea8ff2122e9`  
		Last Modified: Tue, 01 Jul 2025 02:25:12 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:715719c5ac9366a91c5623630b087996970ed9ec7a20fa70bbd51e3f9d02c574`  
		Last Modified: Tue, 01 Jul 2025 02:25:12 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e0357262d1105ae01d506cbfe626f20b6d956b982275c92b06dc88bf7149e1`  
		Last Modified: Tue, 01 Jul 2025 02:25:12 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6cd69df43866afb1822296a5d6db29187e4efa33785a4a887f017de18b35789`  
		Last Modified: Tue, 01 Jul 2025 02:25:13 GMT  
		Size: 8.9 KB (8880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f87fd1ac699d5c592b487872f4b3df5e801f899545436139cf5507eaad9bbe3`  
		Last Modified: Tue, 01 Jul 2025 03:26:33 GMT  
		Size: 54.2 MB (54218289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8393a15f35d40731ce3f665d45af8d72123aa4ab0091e153b9e25f63820e1118`  
		Last Modified: Tue, 01 Jul 2025 03:26:30 GMT  
		Size: 2.1 MB (2060899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e58cb3e7fb42bc4dc7b494feb72d66ff2e41a8330fc0073d71179dc89293e039`  
		Last Modified: Tue, 01 Jul 2025 03:26:29 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37164347b4057d355103bacf3283ff63181414f9dd0836fb9dff2ed0879b8069`  
		Last Modified: Tue, 01 Jul 2025 03:26:29 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d99f97ed54cb716fd3e9ce3dcfff7e08d2e57819dde758024c83e680f5e4fbdc`  
		Last Modified: Tue, 01 Jul 2025 03:26:39 GMT  
		Size: 93.2 MB (93207861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mediawiki:lts-fpm` - unknown; unknown

```console
$ docker pull mediawiki@sha256:57f34da0f3a7e155f703d4250630f849089a8b3273ece85caf3505218f3ceced
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.9 KB (34918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:903f219a366ceda9c4fb66525df577de4403c00005e858697c05cee72184a2cc`

```dockerfile
```

-	Layers:
	-	`sha256:7497e3f794f5cad960332f23cc7c4dfba8ea79a8b1dcc9fda11bf13403afd91f`  
		Last Modified: Tue, 01 Jul 2025 06:17:34 GMT  
		Size: 34.9 KB (34918 bytes)  
		MIME: application/vnd.in-toto+json

### `mediawiki:lts-fpm` - linux; arm variant v5

```console
$ docker pull mediawiki@sha256:0fe98ed57f268fe2c34f41d168e3a1e80481bfc361c4d004d1c41442707b93c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.1 MB (290065162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e99b9990d57692fc80e36f2cd5d879b0ad0b42da1e78cb8b03ec5646b2963e44`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 10 Apr 2025 18:10:22 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1751241600'
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 10 Apr 2025 18:10:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 10 Apr 2025 18:10:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 10 Apr 2025 18:10:22 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Thu, 10 Apr 2025 18:10:22 GMT
ENV PHP_VERSION=8.1.32
# Thu, 10 Apr 2025 18:10:22 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.32.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.32.tar.xz.asc
# Thu, 10 Apr 2025 18:10:22 GMT
ENV PHP_SHA256=c582ac682a280bbc69bc2186c21eb7e3313cc73099be61a6bc1d2cd337cbf383
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 10 Apr 2025 18:10:22 GMT
WORKDIR /var/www/html
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
STOPSIGNAL SIGQUIT
# Thu, 10 Apr 2025 18:10:22 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 10 Apr 2025 18:10:22 GMT
CMD ["php-fpm"]
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 		apt-get update; 	apt-get install -y --no-install-recommends 		git 		librsvg2-bin 		imagemagick 		python3 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libicu-dev 		libonig-dev 		liblua5.1-0-dev 	; 		docker-php-ext-install -j "$(nproc)" 		calendar 		intl 		mbstring 		mysqli 		opcache 	; 		pecl install APCu-5.1.24; 	pecl install LuaSandbox-4.1.2; 	docker-php-ext-enable 		apcu 		luasandbox 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 	mkdir -p /var/www/data; 	chown -R www-data:www-data /var/www/data # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
ENV MEDIAWIKI_MAJOR_VERSION=1.43
# Thu, 10 Apr 2025 18:10:22 GMT
ENV MEDIAWIKI_VERSION=1.43.1
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 	fetchDeps=" 		gnupg 		dirmngr 	"; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 		curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz" -o mediawiki.tar.gz; 	curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz.sig" -o mediawiki.tar.gz.sig; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 		D7D6767D135A514BEB86E9BA75682B08E8A3FEC4 		441276E9CCD15F44F6D97D18C119E1A64D70938E 		F7F780D82EBFB8A56556E7EE82403E59F9F8CD79 		1D98867E82982C8FE0ABC25F9B69B3109D3BB7B0 		E059C034E7A430583C252F4AA8F734246D73B586 	; 	gpg --batch --verify mediawiki.tar.gz.sig mediawiki.tar.gz; 	tar -x --strip-components=1 -f mediawiki.tar.gz; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" mediawiki.tar.gz.sig mediawiki.tar.gz; 	chown -R www-data:www-data extensions skins cache images; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:57a7872a7ce75b95d171f720f215d4e72b887ae709c5c0b319f93f704bd71e07`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 25.8 MB (25762460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69b05322491f7f224fdb6afd1a4feb0c269fe0910bd44e82e37a846aec3e465c`  
		Last Modified: Tue, 01 Jul 2025 03:03:10 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e58b493a89b33667d984de07320c027ba0599d73427f434c8ec42c944a6bd4aa`  
		Last Modified: Tue, 01 Jul 2025 03:03:27 GMT  
		Size: 82.0 MB (81973614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eef43b7ed80f2af53848f0179316741b5f6d73203876a5f0f62b038d570f6c8`  
		Last Modified: Tue, 01 Jul 2025 03:03:10 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54b00c7332808f800668755304252150319eb345638cd7d436d6e09ebc98db53`  
		Last Modified: Tue, 01 Jul 2025 04:16:08 GMT  
		Size: 12.0 MB (12001319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87f46d632cab72e8a2e5bc0221fdf23dcdf97aeb4d4ba681267f6f9953b9d844`  
		Last Modified: Tue, 01 Jul 2025 04:16:08 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf37b0cedcc5ba389239bf90a3b9b6900196823f07608dbfab4c94c9f828838`  
		Last Modified: Tue, 01 Jul 2025 04:24:30 GMT  
		Size: 25.8 MB (25811436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f2511edfc1a42399dc74beda543c39cf84354b593f0804b0cf9fc1254d60996`  
		Last Modified: Tue, 01 Jul 2025 04:24:27 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15fb558caa3127abec38738ccd5f6a7265a11b89aaf72e04b8da92ecea7669ca`  
		Last Modified: Tue, 01 Jul 2025 04:24:27 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df747244aaebda155e5bd44958981cda4420262d90d5f14cbd6f014f43f0900d`  
		Last Modified: Tue, 01 Jul 2025 04:24:27 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:037f258ea65fe94373fe59306a44b3d100b9eec7af37bc38c2f4ec21b6e9c43e`  
		Last Modified: Tue, 01 Jul 2025 04:24:28 GMT  
		Size: 8.9 KB (8882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85a953e03663ff397a06fea103a092310332ac51ef4effee80c0066fa0761597`  
		Last Modified: Tue, 01 Jul 2025 10:25:13 GMT  
		Size: 49.7 MB (49687851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8759b1ba1874bf140d570a3038932bba7f0afcd7a5441ca1b804ea0546b0c9f8`  
		Last Modified: Tue, 01 Jul 2025 10:25:10 GMT  
		Size: 1.6 MB (1612450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bff16f9d42331f6991d5e428db46fe68f3ad782ff4b1fac0790b1a53d2f79458`  
		Last Modified: Tue, 01 Jul 2025 10:25:09 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87b777d1632ffb353f555562599a159cf5b524f51a1706a65d07f0aea3f6805a`  
		Last Modified: Tue, 01 Jul 2025 10:25:09 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:732e0f67bad5de93af6feba956ef3a564686af91bdf022cfb8a00d6db062a924`  
		Last Modified: Tue, 01 Jul 2025 10:25:18 GMT  
		Size: 93.2 MB (93202776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mediawiki:lts-fpm` - unknown; unknown

```console
$ docker pull mediawiki@sha256:c1a33df0528d149258ede8bceb902b42817d9a02b13d52a6faa390efaa9c4b29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.0 KB (35040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:457d523fbb06612848348961fb47e1f985c9e0d81179a47cf064ad394f213122`

```dockerfile
```

-	Layers:
	-	`sha256:033405836cbe9d2e0e5456e4c99ea96cfede559bdc807dcfa9cc827cc4f2ded0`  
		Last Modified: Tue, 01 Jul 2025 12:17:11 GMT  
		Size: 35.0 KB (35040 bytes)  
		MIME: application/vnd.in-toto+json

### `mediawiki:lts-fpm` - linux; arm variant v7

```console
$ docker pull mediawiki@sha256:3082e5ea9d79cddfdcb1fbfdf4abd275f5a8a4d6ba40d93f8c10b3b624b32936
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.1 MB (278052042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b358a22fefe59607f169daa834cb1255bcb9ee6a6a9405db5f172a4aa599550`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 10 Apr 2025 18:10:22 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1751241600'
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 10 Apr 2025 18:10:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 10 Apr 2025 18:10:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 10 Apr 2025 18:10:22 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Thu, 10 Apr 2025 18:10:22 GMT
ENV PHP_VERSION=8.1.32
# Thu, 10 Apr 2025 18:10:22 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.32.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.32.tar.xz.asc
# Thu, 10 Apr 2025 18:10:22 GMT
ENV PHP_SHA256=c582ac682a280bbc69bc2186c21eb7e3313cc73099be61a6bc1d2cd337cbf383
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 10 Apr 2025 18:10:22 GMT
WORKDIR /var/www/html
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
STOPSIGNAL SIGQUIT
# Thu, 10 Apr 2025 18:10:22 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 10 Apr 2025 18:10:22 GMT
CMD ["php-fpm"]
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 		apt-get update; 	apt-get install -y --no-install-recommends 		git 		librsvg2-bin 		imagemagick 		python3 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libicu-dev 		libonig-dev 		liblua5.1-0-dev 	; 		docker-php-ext-install -j "$(nproc)" 		calendar 		intl 		mbstring 		mysqli 		opcache 	; 		pecl install APCu-5.1.24; 	pecl install LuaSandbox-4.1.2; 	docker-php-ext-enable 		apcu 		luasandbox 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 	mkdir -p /var/www/data; 	chown -R www-data:www-data /var/www/data # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
ENV MEDIAWIKI_MAJOR_VERSION=1.43
# Thu, 10 Apr 2025 18:10:22 GMT
ENV MEDIAWIKI_VERSION=1.43.1
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 	fetchDeps=" 		gnupg 		dirmngr 	"; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 		curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz" -o mediawiki.tar.gz; 	curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz.sig" -o mediawiki.tar.gz.sig; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 		D7D6767D135A514BEB86E9BA75682B08E8A3FEC4 		441276E9CCD15F44F6D97D18C119E1A64D70938E 		F7F780D82EBFB8A56556E7EE82403E59F9F8CD79 		1D98867E82982C8FE0ABC25F9B69B3109D3BB7B0 		E059C034E7A430583C252F4AA8F734246D73B586 	; 	gpg --batch --verify mediawiki.tar.gz.sig mediawiki.tar.gz; 	tar -x --strip-components=1 -f mediawiki.tar.gz; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" mediawiki.tar.gz.sig mediawiki.tar.gz; 	chown -R www-data:www-data extensions skins cache images; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:aa4115c1f73522274017cc9ef4668eb7be9359f354969cd6ffca48411714e948`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef237a39acf4f8b50140ea0e65e44fb78759dd5c3014dea07a2e868cbaea5448`  
		Last Modified: Tue, 01 Jul 2025 02:37:03 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95d1f66f2aaac83b6eaf2006cda16a0feae7d183fb4de3fc7f021a3b94f4d2f5`  
		Last Modified: Tue, 01 Jul 2025 02:37:09 GMT  
		Size: 76.1 MB (76149625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:834cb9f18ec360ae1dafdba9049fa98c9a4c9dff8f407122be76f6644c8deb27`  
		Last Modified: Tue, 01 Jul 2025 02:37:03 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83b6dde3dbf9120713f9fe58a6ef7d1d4016253d097a6aac238d26fdd4cae437`  
		Last Modified: Tue, 01 Jul 2025 05:16:31 GMT  
		Size: 12.0 MB (12001349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17d565852efbfb5e4e73e68c26761fc2ac584b50d9fad2da488f3369b80b178e`  
		Last Modified: Tue, 01 Jul 2025 05:16:29 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5afc915588685ca3ef060732a5d1894c4b6b3691afc9897ebd7ee0f1764e67a`  
		Last Modified: Tue, 01 Jul 2025 06:11:25 GMT  
		Size: 25.0 MB (24955085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1d14f7fb5bce5150559981e5265f2b0766e09e17eb705b0f09d769b5e357cd6`  
		Last Modified: Tue, 01 Jul 2025 06:11:23 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19a2f6feea55fd20a7ade8e5de659b10c7e860930fc2bd4db40ec3886ee82652`  
		Last Modified: Tue, 01 Jul 2025 06:11:23 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b90275b9e37bd49821ab6461b664945b2fd2bceb4eaa289356273a65cc8bd742`  
		Last Modified: Tue, 01 Jul 2025 06:11:23 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0779c3b6403743e72b33568046f5b353a099e59a49c528dae6e150f5f35e5490`  
		Last Modified: Tue, 01 Jul 2025 06:11:23 GMT  
		Size: 8.9 KB (8881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5abe75141889e0df937b3936ca0f64431274d581195b5dbf4a92a15d0584da6b`  
		Last Modified: Tue, 01 Jul 2025 19:57:10 GMT  
		Size: 46.2 MB (46236718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d964d19f64e33673ac8c6da2130487df9bfb9647dd4d3aef2363dcbdc29122`  
		Last Modified: Tue, 01 Jul 2025 19:57:06 GMT  
		Size: 1.6 MB (1554582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a94f26397bccad1e6dbd965b32f1a100244352147a72a3f3fd07aca11df7474`  
		Last Modified: Tue, 01 Jul 2025 19:57:07 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36e2fae6d3c73e557ec23189d860a37fd4b7c9eb9e428c2f710f525e9010383f`  
		Last Modified: Tue, 01 Jul 2025 19:57:08 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8de8486c7cb5573ed3099796f79e156290ff4f675de85300ad1f7b2e076210ab`  
		Last Modified: Tue, 01 Jul 2025 19:57:11 GMT  
		Size: 93.2 MB (93202687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mediawiki:lts-fpm` - unknown; unknown

```console
$ docker pull mediawiki@sha256:b5657e8f367aa39616fe714b6752f12d2a027cff88207ea9aefcdfdf88bbdaaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.0 KB (35040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:680283109da28393f35ee3cb8f98aa4c671eed1f1b277bb04579c4c6778d113b`

```dockerfile
```

-	Layers:
	-	`sha256:0b298e7101ed033cc0e6c9399bb8d24df34a1a8dde6de7ed9f0e419170b08c97`  
		Last Modified: Tue, 01 Jul 2025 21:17:09 GMT  
		Size: 35.0 KB (35040 bytes)  
		MIME: application/vnd.in-toto+json

### `mediawiki:lts-fpm` - linux; arm64 variant v8

```console
$ docker pull mediawiki@sha256:d5961feb1ed5a3ceea000735b8ec93a20a81981dbb76f0703df8e1d875550f18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.5 MB (312474125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1965540de5ae1908b3d687c7170cffc3bd57e25a636b28adcee84fef201e8929`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 10 Apr 2025 18:10:22 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 10 Apr 2025 18:10:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 10 Apr 2025 18:10:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 10 Apr 2025 18:10:22 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Thu, 10 Apr 2025 18:10:22 GMT
ENV PHP_VERSION=8.1.32
# Thu, 10 Apr 2025 18:10:22 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.32.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.32.tar.xz.asc
# Thu, 10 Apr 2025 18:10:22 GMT
ENV PHP_SHA256=c582ac682a280bbc69bc2186c21eb7e3313cc73099be61a6bc1d2cd337cbf383
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 10 Apr 2025 18:10:22 GMT
WORKDIR /var/www/html
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
STOPSIGNAL SIGQUIT
# Thu, 10 Apr 2025 18:10:22 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 10 Apr 2025 18:10:22 GMT
CMD ["php-fpm"]
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 		apt-get update; 	apt-get install -y --no-install-recommends 		git 		librsvg2-bin 		imagemagick 		python3 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libicu-dev 		libonig-dev 		liblua5.1-0-dev 	; 		docker-php-ext-install -j "$(nproc)" 		calendar 		intl 		mbstring 		mysqli 		opcache 	; 		pecl install APCu-5.1.24; 	pecl install LuaSandbox-4.1.2; 	docker-php-ext-enable 		apcu 		luasandbox 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 	mkdir -p /var/www/data; 	chown -R www-data:www-data /var/www/data # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
ENV MEDIAWIKI_MAJOR_VERSION=1.43
# Thu, 10 Apr 2025 18:10:22 GMT
ENV MEDIAWIKI_VERSION=1.43.1
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 	fetchDeps=" 		gnupg 		dirmngr 	"; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 		curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz" -o mediawiki.tar.gz; 	curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz.sig" -o mediawiki.tar.gz.sig; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 		D7D6767D135A514BEB86E9BA75682B08E8A3FEC4 		441276E9CCD15F44F6D97D18C119E1A64D70938E 		F7F780D82EBFB8A56556E7EE82403E59F9F8CD79 		1D98867E82982C8FE0ABC25F9B69B3109D3BB7B0 		E059C034E7A430583C252F4AA8F734246D73B586 	; 	gpg --batch --verify mediawiki.tar.gz.sig mediawiki.tar.gz; 	tar -x --strip-components=1 -f mediawiki.tar.gz; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" mediawiki.tar.gz.sig mediawiki.tar.gz; 	chown -R www-data:www-data extensions skins cache images; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:37259e7330667afd74c3386d3ed869f06bd9b7714370c78e3065f4e28607cc02`  
		Last Modified: Tue, 01 Jul 2025 01:15:09 GMT  
		Size: 28.1 MB (28077678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d11709a68ca8c2093073c9a1d4b656c3cf0443563f219a68b0b4d26313c3ea1`  
		Last Modified: Tue, 01 Jul 2025 03:15:53 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af5584d1cd13b2f94aca836225a1f54b5de7c1c9943fe27f25088a0be3a7059a`  
		Last Modified: Tue, 01 Jul 2025 03:16:04 GMT  
		Size: 98.1 MB (98130658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e73f9696b074c2e8b1d467becd89db85a06286c5c522e385d7dfe3d5c3e8c565`  
		Last Modified: Tue, 01 Jul 2025 03:15:54 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30bd546738dee5586996509b8eb844e7dc4a9287623a192e572820d4b73480bb`  
		Last Modified: Tue, 01 Jul 2025 05:40:54 GMT  
		Size: 12.0 MB (12003062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a02189c33035abe8d81ced77ed20f96f068d216fd9848f8adc6536b68a69535e`  
		Last Modified: Tue, 01 Jul 2025 05:40:53 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e73902433964f3843dd0bcc3a49bc9348a7f0254aa915423abe27bb1f17f76`  
		Last Modified: Tue, 01 Jul 2025 05:48:34 GMT  
		Size: 27.3 MB (27321844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e44af31ced3d93a8ae203270956864dd8c09d43c1964820e143027460d7f51e`  
		Last Modified: Tue, 01 Jul 2025 05:48:32 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:252fce50031fb4d7673eea0eea827cb20fb64587ae7e85b4361ac0c868b3bde5`  
		Last Modified: Tue, 01 Jul 2025 05:48:32 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b728485c94b0018ae713890149783bc3baa78186606c3bdce55cac85c0763996`  
		Last Modified: Tue, 01 Jul 2025 05:48:32 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a8321dbdf560bd7a7cd397778bb5f3ca70768f51e756c04e290c4c684f20bf`  
		Last Modified: Tue, 01 Jul 2025 05:48:32 GMT  
		Size: 8.9 KB (8884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb357eebe239e316818c533a04da9d44d49ea68c348586c9aad4374829ac2ac`  
		Last Modified: Tue, 01 Jul 2025 15:21:52 GMT  
		Size: 51.4 MB (51403350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e24a1105940cb2a5f16dba742707280c40673bc42f9e3aefed60c3fc766d2e`  
		Last Modified: Tue, 01 Jul 2025 15:21:48 GMT  
		Size: 2.3 MB (2316507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e273da2def4fbeea6ac3a867bb101d20a37c75e7ec13cdbdb669f3065355e380`  
		Last Modified: Tue, 01 Jul 2025 15:21:47 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4703112ea6a9d13bbec173e991b472adba0b3698b89b27c64052ba4ce8bd93cc`  
		Last Modified: Tue, 01 Jul 2025 15:21:48 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d338e39119420237c04fb8145bf67e1ed9475602e6caf90493d5d55bb7523705`  
		Last Modified: Tue, 01 Jul 2025 15:21:59 GMT  
		Size: 93.2 MB (93207773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mediawiki:lts-fpm` - unknown; unknown

```console
$ docker pull mediawiki@sha256:994427cb571092016c297563ad76a20b0ec7759139d1cef1b931f1752e609e2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.1 KB (35076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8ebb1dc3c6dbf175c99396010059e9b54185248b214adc120bbb185dcd72e8b`

```dockerfile
```

-	Layers:
	-	`sha256:219552707c16d37fcf8cec30e3639dbfa41ed85d52f979b8dfdea7ffde85f1d2`  
		Last Modified: Tue, 01 Jul 2025 18:17:11 GMT  
		Size: 35.1 KB (35076 bytes)  
		MIME: application/vnd.in-toto+json

### `mediawiki:lts-fpm` - linux; 386

```console
$ docker pull mediawiki@sha256:76f06d2d0ab1c179ec2fc4069a0f0abebfee0a44c82db5c9129627f995bd3dd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.6 MB (321620870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25e2ca019f48916ddadf94e347b28e525bee3da993f8c43eb200fd628d820dc9`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 10 Apr 2025 18:10:22 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1751241600'
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 10 Apr 2025 18:10:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 10 Apr 2025 18:10:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 10 Apr 2025 18:10:22 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Thu, 10 Apr 2025 18:10:22 GMT
ENV PHP_VERSION=8.1.32
# Thu, 10 Apr 2025 18:10:22 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.32.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.32.tar.xz.asc
# Thu, 10 Apr 2025 18:10:22 GMT
ENV PHP_SHA256=c582ac682a280bbc69bc2186c21eb7e3313cc73099be61a6bc1d2cd337cbf383
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 10 Apr 2025 18:10:22 GMT
WORKDIR /var/www/html
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
STOPSIGNAL SIGQUIT
# Thu, 10 Apr 2025 18:10:22 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 10 Apr 2025 18:10:22 GMT
CMD ["php-fpm"]
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 		apt-get update; 	apt-get install -y --no-install-recommends 		git 		librsvg2-bin 		imagemagick 		python3 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libicu-dev 		libonig-dev 		liblua5.1-0-dev 	; 		docker-php-ext-install -j "$(nproc)" 		calendar 		intl 		mbstring 		mysqli 		opcache 	; 		pecl install APCu-5.1.24; 	pecl install LuaSandbox-4.1.2; 	docker-php-ext-enable 		apcu 		luasandbox 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 	mkdir -p /var/www/data; 	chown -R www-data:www-data /var/www/data # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
ENV MEDIAWIKI_MAJOR_VERSION=1.43
# Thu, 10 Apr 2025 18:10:22 GMT
ENV MEDIAWIKI_VERSION=1.43.1
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 	fetchDeps=" 		gnupg 		dirmngr 	"; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 		curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz" -o mediawiki.tar.gz; 	curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz.sig" -o mediawiki.tar.gz.sig; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 		D7D6767D135A514BEB86E9BA75682B08E8A3FEC4 		441276E9CCD15F44F6D97D18C119E1A64D70938E 		F7F780D82EBFB8A56556E7EE82403E59F9F8CD79 		1D98867E82982C8FE0ABC25F9B69B3109D3BB7B0 		E059C034E7A430583C252F4AA8F734246D73B586 	; 	gpg --batch --verify mediawiki.tar.gz.sig mediawiki.tar.gz; 	tar -x --strip-components=1 -f mediawiki.tar.gz; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" mediawiki.tar.gz.sig mediawiki.tar.gz; 	chown -R www-data:www-data extensions skins cache images; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:88e96ee0cb4c7106f4d6a5cdeaeb171ec22a2484245e406cb5267b2be095937c`  
		Last Modified: Tue, 01 Jul 2025 01:14:33 GMT  
		Size: 29.2 MB (29212432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38799d2ddc895aad8e2ff08f9eef10e5388c7f7e78be838767e4c8951c0d43e2`  
		Last Modified: Tue, 01 Jul 2025 02:24:54 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5cd3af501eadb8c202ef070a8defc845ff4ce34bd38fa4dc554742e45abb6a1`  
		Last Modified: Tue, 01 Jul 2025 02:25:03 GMT  
		Size: 101.5 MB (101515435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:550befc6db41e6e027a81f6bf10bb1e1aebd01e8e405629df222c1f5eb6ac629`  
		Last Modified: Tue, 01 Jul 2025 02:24:54 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7fb6b1fd6927463580cd22b08ad70ae3edd2b917a9b879886a3ce8ba2fb72ca`  
		Last Modified: Tue, 01 Jul 2025 02:25:04 GMT  
		Size: 12.0 MB (12002365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8deeacb84ce73df99cd293689dd2cdabc0a01737c55651a72d8f30e1b52ace75`  
		Last Modified: Tue, 01 Jul 2025 02:24:53 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e34bf26568c2478aaf9a2353743f2eee704c4d79642a345ce59a968cc4966f18`  
		Last Modified: Tue, 01 Jul 2025 02:24:55 GMT  
		Size: 27.8 MB (27840118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:723b9e3e8dbddd3426a822c43ee46e5cd65c68eadacafd7d519b61112417d35e`  
		Last Modified: Tue, 01 Jul 2025 02:24:53 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2ef3f9c27311971bbe564700c09c8c3b9368ab161855688546f4f24c528bdea`  
		Last Modified: Tue, 01 Jul 2025 02:24:53 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0750121205202b2b889cac8abe7ddfcd67f6fae865aad60c82397baebc95f1c7`  
		Last Modified: Tue, 01 Jul 2025 02:24:53 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06cd41d90dee4f9a091c7227aba45210ad63167cd7adcb55171ed744b6831ad3`  
		Last Modified: Tue, 01 Jul 2025 02:24:54 GMT  
		Size: 8.9 KB (8881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71850fe7518e4440c4994c7b20d85b3e9d5100d50daf563bf4b03d91eeefbf84`  
		Last Modified: Tue, 01 Jul 2025 03:25:39 GMT  
		Size: 55.8 MB (55771477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff552c273dc99de6daa8a4826a9eb1bbb291f8aedbb402173e6231558036485e`  
		Last Modified: Tue, 01 Jul 2025 03:25:32 GMT  
		Size: 2.1 MB (2059848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf2ae4961e326b59ebc44cb1a9e2b4ee13d094f49c8136286a4f29f7eb9a6eda`  
		Last Modified: Tue, 01 Jul 2025 03:25:32 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93d2adab7f487251d282665abaf21369fb8c3480a48688685ef03f3525f388ae`  
		Last Modified: Tue, 01 Jul 2025 03:25:33 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db19869308d0e8e0f148dd265551558a0915f209db9ba0885daf6c122d21987f`  
		Last Modified: Tue, 01 Jul 2025 03:25:43 GMT  
		Size: 93.2 MB (93205944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mediawiki:lts-fpm` - unknown; unknown

```console
$ docker pull mediawiki@sha256:9e0ab58f5d5900e4c046bbb6dff5473e3de7c17f143e9735780182f703727a90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.9 KB (34878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a7acabb5ba69d74043b8104ed6f305393f31a0d0932fc90ffa18670e37b7d20`

```dockerfile
```

-	Layers:
	-	`sha256:d1903f3ad094c514b20c56d1f4f99b3d2ce1b917e60e8dc26f90ac000b10abe5`  
		Last Modified: Tue, 01 Jul 2025 06:17:47 GMT  
		Size: 34.9 KB (34878 bytes)  
		MIME: application/vnd.in-toto+json

### `mediawiki:lts-fpm` - linux; ppc64le

```console
$ docker pull mediawiki@sha256:89f2ea9021fb5b9d4834c5a9b38c65ced093c8469e7c0c6f57dd1ac3b04d8c5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.2 MB (329235603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d32a53d93c0e9311d351d67933481f236ea9ba209a922ce63caf001e19bc02f`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 10 Apr 2025 18:10:22 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1751241600'
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 10 Apr 2025 18:10:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 10 Apr 2025 18:10:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 10 Apr 2025 18:10:22 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Thu, 10 Apr 2025 18:10:22 GMT
ENV PHP_VERSION=8.1.32
# Thu, 10 Apr 2025 18:10:22 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.32.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.32.tar.xz.asc
# Thu, 10 Apr 2025 18:10:22 GMT
ENV PHP_SHA256=c582ac682a280bbc69bc2186c21eb7e3313cc73099be61a6bc1d2cd337cbf383
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 10 Apr 2025 18:10:22 GMT
WORKDIR /var/www/html
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
STOPSIGNAL SIGQUIT
# Thu, 10 Apr 2025 18:10:22 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 10 Apr 2025 18:10:22 GMT
CMD ["php-fpm"]
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 		apt-get update; 	apt-get install -y --no-install-recommends 		git 		librsvg2-bin 		imagemagick 		python3 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libicu-dev 		libonig-dev 		liblua5.1-0-dev 	; 		docker-php-ext-install -j "$(nproc)" 		calendar 		intl 		mbstring 		mysqli 		opcache 	; 		pecl install APCu-5.1.24; 	pecl install LuaSandbox-4.1.2; 	docker-php-ext-enable 		apcu 		luasandbox 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 	mkdir -p /var/www/data; 	chown -R www-data:www-data /var/www/data # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
ENV MEDIAWIKI_MAJOR_VERSION=1.43
# Thu, 10 Apr 2025 18:10:22 GMT
ENV MEDIAWIKI_VERSION=1.43.1
# Thu, 10 Apr 2025 18:10:22 GMT
RUN set -eux; 	fetchDeps=" 		gnupg 		dirmngr 	"; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 		curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz" -o mediawiki.tar.gz; 	curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz.sig" -o mediawiki.tar.gz.sig; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 		D7D6767D135A514BEB86E9BA75682B08E8A3FEC4 		441276E9CCD15F44F6D97D18C119E1A64D70938E 		F7F780D82EBFB8A56556E7EE82403E59F9F8CD79 		1D98867E82982C8FE0ABC25F9B69B3109D3BB7B0 		E059C034E7A430583C252F4AA8F734246D73B586 	; 	gpg --batch --verify mediawiki.tar.gz.sig mediawiki.tar.gz; 	tar -x --strip-components=1 -f mediawiki.tar.gz; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" mediawiki.tar.gz.sig mediawiki.tar.gz; 	chown -R www-data:www-data extensions skins cache images; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Apr 2025 18:10:22 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:c5884d20b08634214a92bd5de559876bf30e6c5453807c3014f5480eeba20662`  
		Last Modified: Tue, 01 Jul 2025 01:15:20 GMT  
		Size: 32.1 MB (32072820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceff3d73088eb90a29a3888d344cedd86858df29b36df7932d3fe0d16eda4e7d`  
		Last Modified: Tue, 01 Jul 2025 02:58:07 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08259e2c7cacc0405f0da4ea7142f0be36234c1b63d584779538944c8319235f`  
		Last Modified: Tue, 01 Jul 2025 02:58:21 GMT  
		Size: 103.3 MB (103326709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2fcb5df575fa0806e458d09147e66250dc80c744fe65c46881d5d2395c98374`  
		Last Modified: Tue, 01 Jul 2025 02:58:07 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2718b0b6a84e4474554625fe5b711bca8f01993040bf157d0904d4016859262`  
		Last Modified: Tue, 01 Jul 2025 04:16:35 GMT  
		Size: 12.0 MB (12002648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f17b5a58f2dc32097343688e1fdf9cd0f63a13d286057769878a7f3ef695ecfc`  
		Last Modified: Tue, 01 Jul 2025 04:16:35 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57d98ea3850293cb8cc83563c343f19767c7751af70d5f3d5ce9dc3cf379b884`  
		Last Modified: Tue, 01 Jul 2025 04:24:57 GMT  
		Size: 28.4 MB (28353635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd5d9216e0e3985e96dae773b0d814e671df8fed4f334da0549de76a478d310`  
		Last Modified: Tue, 01 Jul 2025 04:24:55 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f7e8ff82468806468a5c963951e896bd073a615f26e62bd5a067ae428804c1a`  
		Last Modified: Tue, 01 Jul 2025 04:24:54 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:458e6d543ab088026ffd0af6d1e30a99a1b66c24c8e2c17332915a32addea193`  
		Last Modified: Tue, 01 Jul 2025 04:24:54 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:369cd300c820a4929ffe4cfa83f2fa6442da2ec63e145d634d0d615c54ab9c98`  
		Last Modified: Tue, 01 Jul 2025 04:24:55 GMT  
		Size: 8.9 KB (8883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7de6aae687c2746ccaee56a39a7833f8a5e29be28af1fd3db5a32fdfcdcc9e16`  
		Last Modified: Tue, 01 Jul 2025 12:44:02 GMT  
		Size: 58.5 MB (58469265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdab3cf0009e74d9e757ea84b9e06ee803c3a573e414aa5b8b9dcbdb15fa806c`  
		Last Modified: Tue, 01 Jul 2025 12:44:00 GMT  
		Size: 1.8 MB (1789754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a214c64739b65dfbfa433c476e5dd6e1552a0f9fd738467c9f931bef4c3c1cc1`  
		Last Modified: Tue, 01 Jul 2025 12:43:59 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faf1439b7fddc5e8955718a7ad18eb66d46a01cb05046c1dc402788d3fda7440`  
		Last Modified: Tue, 01 Jul 2025 12:43:59 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f70bd722823043527ccce8d45d2e0c44b8a9e95965d9021a45d639d903486102`  
		Last Modified: Tue, 01 Jul 2025 12:44:06 GMT  
		Size: 93.2 MB (93207519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mediawiki:lts-fpm` - unknown; unknown

```console
$ docker pull mediawiki@sha256:ee14d26d7b63a0436a005a138957d3cb01cf845e29b00ac2f91eaf37556ff180
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.0 KB (34969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feb1f5004d7cd6852ee6a6817c57b59e8600dbda61cbef05af5ba40fc836e48b`

```dockerfile
```

-	Layers:
	-	`sha256:1b354c367a151e03ece3761fe2d3e614813ef419cf4c3379b070210184175a25`  
		Last Modified: Tue, 01 Jul 2025 15:17:14 GMT  
		Size: 35.0 KB (34969 bytes)  
		MIME: application/vnd.in-toto+json
