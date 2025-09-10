## `php:zts-trixie`

```console
$ docker pull php@sha256:374fdd9ffbbdf990894258a8db9bfaac9d6137d1bcb3886d5029b96fb60ec3be
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

### `php:zts-trixie` - linux; amd64

```console
$ docker pull php@sha256:2679ca9a77d8174516865135ab20be4005a54ff0abe012e54c095deea5d85e56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.5 MB (186474649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94ab96f2e99d84ef3941e45eb260aa9e15256bb99465b516da973dfa5fe4951c`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Thu, 28 Aug 2025 12:46:41 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 28 Aug 2025 12:46:41 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_VERSION=8.4.12
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.12.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.12.tar.xz.asc
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_SHA256=c1b7978cbb5054eed6c749bde4444afc16a3f2268101fb70a7d5d9b1083b12ad
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 28 Aug 2025 12:46:41 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:ce1261c6d567efa8e3b457673eeeb474a0a8066df6bb95ca9a6a94a31e219dd3`  
		Last Modified: Mon, 08 Sep 2025 21:12:35 GMT  
		Size: 29.8 MB (29773495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:828c51cca8367720460da1412fca1a50c43d789f57c1892d22a96b3d222a1d72`  
		Last Modified: Mon, 08 Sep 2025 22:14:27 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18cc80e40b8115a89dc591a2c1203737757f37106a22e7d2bf01b584f66b1845`  
		Last Modified: Mon, 08 Sep 2025 23:15:08 GMT  
		Size: 117.8 MB (117835872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:857dfe12e2d6ac1d9d375269a62047e02428bd594e2e59732f958ba623df9648`  
		Last Modified: Mon, 08 Sep 2025 22:14:27 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:623bd02b940bea29158ee0e3e627ef476d113a59a5c2c3f5e58811dfa297ec7a`  
		Last Modified: Mon, 08 Sep 2025 23:15:06 GMT  
		Size: 13.8 MB (13783995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34cf83ddce174df1173ca030c0fa22502aa771564e5337ac3e5428f98c3eb756`  
		Last Modified: Mon, 08 Sep 2025 22:14:28 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5428d469ade3f8974814fc36ead02ddf893e32d99c02d66b492e91b06d110821`  
		Last Modified: Mon, 08 Sep 2025 23:15:07 GMT  
		Size: 25.1 MB (25077406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f757b44f9930614defa95212432b0d92046d7e6c14ba92657c76a6e9f55b499`  
		Last Modified: Mon, 08 Sep 2025 22:14:28 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b957fd45b1f9a9b65e48d4cfb0eb942c094759c38250c14e6bd717a9cc5d1832`  
		Last Modified: Mon, 08 Sep 2025 22:14:27 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a28356c9eb80493f1ef9c493c29ebfacff617ba51531320bf7d1a3b0d1799aa`  
		Last Modified: Mon, 08 Sep 2025 22:14:28 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:zts-trixie` - unknown; unknown

```console
$ docker pull php@sha256:6cf35538758df04e19ca7f853cdda03566dcfca3042464b1980899bbb9504e42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6727993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d425882ab6bcb4c732ec341006a66dc328dbfd0fec910a2f713239b64499bb49`

```dockerfile
```

-	Layers:
	-	`sha256:01776662f4b7ad6387b3f7dab86fb1f88bf9f0986a0ec5802ea22f8b876d347a`  
		Last Modified: Mon, 08 Sep 2025 22:57:47 GMT  
		Size: 6.7 MB (6684210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35f2ee4ba1e9e57aa0e55af532c6935c1023d2db4f76885e78421054a670b821`  
		Last Modified: Mon, 08 Sep 2025 22:57:48 GMT  
		Size: 43.8 KB (43783 bytes)  
		MIME: application/vnd.in-toto+json

### `php:zts-trixie` - linux; arm variant v5

```console
$ docker pull php@sha256:4626d8cf86031464590860a04c8d6925e67e09a7c51d38b6ce993f40c75a5c95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.7 MB (159702259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f19183d8da4086d1405eac5b041d1fd052b6f81f99dabb48ffeb25f074ab29e1`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Thu, 28 Aug 2025 12:46:41 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1757289600'
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 28 Aug 2025 12:46:41 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_VERSION=8.4.12
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.12.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.12.tar.xz.asc
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_SHA256=c1b7978cbb5054eed6c749bde4444afc16a3f2268101fb70a7d5d9b1083b12ad
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 28 Aug 2025 12:46:41 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:5d61fc20e756831552727f89a087e2b45b07dace604ad2cda0a2afa80ace388d`  
		Last Modified: Mon, 08 Sep 2025 21:13:29 GMT  
		Size: 27.9 MB (27941760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cea5e9196f0a36714a48fcc1c959870b004b3e1c190b2745826302ad278016e3`  
		Last Modified: Mon, 08 Sep 2025 21:47:09 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12bb200c14744da480ad058b36c9398e6f3960e87404b051bbfc64dd96d0105c`  
		Last Modified: Tue, 09 Sep 2025 01:27:40 GMT  
		Size: 94.9 MB (94873314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:428a2042ac681c544b163051dcfe0104b3da0313f13c85a5e34911ccbffd8494`  
		Last Modified: Mon, 08 Sep 2025 21:47:13 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d77f24e9dc2451ca301bd0f21493c00e5638b2bbcc6cf4d3341e01877d50b0bf`  
		Last Modified: Tue, 09 Sep 2025 21:14:20 GMT  
		Size: 13.8 MB (13781562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a5e1b06c15511e06b486498213e694956e2548edec4bf5216fea6606530ed63`  
		Last Modified: Mon, 08 Sep 2025 22:14:29 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24875987ccbc2e0a9a35c7973ef91575004de8bf47a159319bbd046f82541c98`  
		Last Modified: Tue, 09 Sep 2025 14:19:30 GMT  
		Size: 23.1 MB (23101733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:259bfb499da0d75ba27de4437e9907d741574831f6728e6b14dee1843ff410e8`  
		Last Modified: Mon, 08 Sep 2025 22:14:30 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:913f48bf20b0c40c42a1123dbf219cf965feb7e33f3699359a6815b4f60cf1ff`  
		Last Modified: Mon, 08 Sep 2025 22:14:30 GMT  
		Size: 254.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ba12de2c363a5c69deb19608ad851825a88017fd83e45bb476c58f8ce208f1e`  
		Last Modified: Mon, 08 Sep 2025 22:14:30 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:zts-trixie` - unknown; unknown

```console
$ docker pull php@sha256:f3755b3e6e563d4b967a608fa6158dd3c7bc1a12174aa7a31fd3a9bdb87d33dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6528021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08b9e501316c2c6211fad342154b1610fb7e188ed487a8c7e294b8862c3998f4`

```dockerfile
```

-	Layers:
	-	`sha256:05e654234669de6a9dad96b93a8db85ffd3faa262067ab4dc145faad45e6ce9a`  
		Last Modified: Mon, 08 Sep 2025 22:57:55 GMT  
		Size: 6.5 MB (6484056 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a550a24bbd28f18a56a9b8dcc064770032e9aff686696f7fbb7cfaba5b4fd32a`  
		Last Modified: Mon, 08 Sep 2025 22:57:56 GMT  
		Size: 44.0 KB (43965 bytes)  
		MIME: application/vnd.in-toto+json

### `php:zts-trixie` - linux; arm variant v7

```console
$ docker pull php@sha256:0e55301e73a162eec72cf78231f6e59f17b1e0a67c516dc73cc776faba0aaeb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.0 MB (148028146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9beeca78e2371f8fd1ea981a26a1d970a2c17831496774c7344c3eb73eac5a4`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Thu, 28 Aug 2025 12:46:41 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1757289600'
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 28 Aug 2025 12:46:41 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_VERSION=8.4.12
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.12.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.12.tar.xz.asc
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_SHA256=c1b7978cbb5054eed6c749bde4444afc16a3f2268101fb70a7d5d9b1083b12ad
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 28 Aug 2025 12:46:41 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:c01338083e94735040ac705e73d3207fecb1a829de94334396239199538796bd`  
		Last Modified: Mon, 08 Sep 2025 21:13:56 GMT  
		Size: 26.2 MB (26207847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88e892a932f4a337f455f41dc5cd24c20faeae5638ab3292acf119483f3692ea`  
		Last Modified: Mon, 08 Sep 2025 22:08:58 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fadba986d704cfe25456bc4e1adde83e842cb6d7cc55dcd907cc3aae170c38f`  
		Last Modified: Tue, 09 Sep 2025 01:37:12 GMT  
		Size: 86.2 MB (86244467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20bbf8052997e9ecbe0ab93ab9f331056866c53acf46d9276f348f72d56c587b`  
		Last Modified: Mon, 08 Sep 2025 22:08:59 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3309efcfb82c3cdb419e346ea8064b6aef4b606cc41dc6df4638c4b85c46efe8`  
		Last Modified: Tue, 09 Sep 2025 12:27:58 GMT  
		Size: 13.8 MB (13781634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f04ce5148808b95d72782e191cea90f9726f507c9a504bfef115e1a70e9c05e2`  
		Last Modified: Mon, 08 Sep 2025 22:23:51 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1637bbcd0045a7923800a58764ce81d87c590eb8853bce185bd4a55f63b82e3e`  
		Last Modified: Tue, 09 Sep 2025 12:27:59 GMT  
		Size: 21.8 MB (21790314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d464761cdc5830f58c11ab97b8333f6983677e6806013d249898a02b23afcfe5`  
		Last Modified: Mon, 08 Sep 2025 22:23:51 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e647eee6ac2c51d61c9d6acb39f6a8b4a8bff0e67b8d2e015fddf55ce88ed52`  
		Last Modified: Mon, 08 Sep 2025 22:23:53 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1acd320dcdc1bfd7fb39b587ef26560aa4208fad3abd27a35ab3f321a030951`  
		Last Modified: Mon, 08 Sep 2025 22:23:51 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:zts-trixie` - unknown; unknown

```console
$ docker pull php@sha256:7f8794af6618aa42b1cff14bc46149ae6fb3b1b7f749973de56eae2a795d22ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6531988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccb722816a95dfacd3b5450d2e6cfa0e6270f77fa6eeab2b876fadd8522c6851`

```dockerfile
```

-	Layers:
	-	`sha256:956d1defcf2b2ae8a68ed4ff53e262f9d76214708a3c1581387853d085c8550c`  
		Last Modified: Mon, 08 Sep 2025 22:58:02 GMT  
		Size: 6.5 MB (6488022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:377cbced8497250045ef043092f4a3fcc6bf17c3ef02b44038b340095e613613`  
		Last Modified: Mon, 08 Sep 2025 22:58:03 GMT  
		Size: 44.0 KB (43966 bytes)  
		MIME: application/vnd.in-toto+json

### `php:zts-trixie` - linux; arm64 variant v8

```console
$ docker pull php@sha256:8703363f4436322a48ac7929f79d40c9790981b014bd8fbd6c39c47eee5f0b66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.8 MB (178766834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bcc49925ebbe439a2fead5999fa075d88389e451286a7ab3c0ce89fab26ee62`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Thu, 28 Aug 2025 12:46:41 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 28 Aug 2025 12:46:41 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_VERSION=8.4.12
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.12.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.12.tar.xz.asc
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_SHA256=c1b7978cbb5054eed6c749bde4444afc16a3f2268101fb70a7d5d9b1083b12ad
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 28 Aug 2025 12:46:41 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:b2feff975e6dd2ebaf182772fb9ee26274648387b061e821e0bb5026735dd094`  
		Last Modified: Mon, 08 Sep 2025 21:13:54 GMT  
		Size: 30.1 MB (30136631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4291e826285da1f1af405bb202cada87663a0ffaf560e289d7720d89130cf33`  
		Last Modified: Mon, 08 Sep 2025 22:06:44 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82cbb101701d421f00d87d13632eb797281d889123c411357d14387e7ac8a4fd`  
		Last Modified: Tue, 09 Sep 2025 00:45:31 GMT  
		Size: 110.2 MB (110161600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bbbdec43bcc5a2e52829085d8fce7a7481e0615b21e67f46b3170052ee334c1`  
		Last Modified: Mon, 08 Sep 2025 21:35:07 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c87b2cd2dc9615794e2c756fecefcf28651cccb6ec005315818381a09bb3463`  
		Last Modified: Tue, 09 Sep 2025 00:45:31 GMT  
		Size: 13.8 MB (13783607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3479f9d7b6b57eb15fb17fa8f2b1c4e6a77b24d73fbd0205ce45c3ba63b04ee`  
		Last Modified: Mon, 08 Sep 2025 22:09:05 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6dc5b8bd937b005ba67aca56a7ee2f7f08f501f41a2d41809f9b353761af617`  
		Last Modified: Tue, 09 Sep 2025 00:45:29 GMT  
		Size: 24.7 MB (24681109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ba7fec40725f757aee6936b91e947c7655741c606d0908728b35b59f76ad989`  
		Last Modified: Mon, 08 Sep 2025 22:09:06 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44586258b0fcc8d3031df7498c704f5a3be6ce12ed401561fc2595cf854a46f4`  
		Last Modified: Mon, 08 Sep 2025 22:09:07 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fa6c9340b8a069c0a20bd9a89504c7cafd7bae10fd0c79d55cc9cbf39f3d570`  
		Last Modified: Mon, 08 Sep 2025 22:09:05 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:zts-trixie` - unknown; unknown

```console
$ docker pull php@sha256:bfbaf5725a6f8b5687dfa0ad1939e34fde7a6c7ff1405f1fecbcfc3b856d9bb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6825563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d1573f83451bdf56f157b65cb9ff7f363820e7b60b586fd0bead1057a81b54b`

```dockerfile
```

-	Layers:
	-	`sha256:bc12cb61631dbe728560523c7c15f4498f36c7f9b1f05891c78d1a03e77ecdb3`  
		Last Modified: Mon, 08 Sep 2025 22:58:16 GMT  
		Size: 6.8 MB (6781537 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bbf92e45ecfbdeae32401fa6ae04404b1e530634ec8f269f2e7e1ddf51ccee5`  
		Last Modified: Mon, 08 Sep 2025 22:58:18 GMT  
		Size: 44.0 KB (44026 bytes)  
		MIME: application/vnd.in-toto+json

### `php:zts-trixie` - linux; 386

```console
$ docker pull php@sha256:4ac4b1e7bc1dc8ab72a1b7f0f6f2ede05b54d9c6fc66349df5d41f9853ce5ad0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.8 MB (186797751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72b764f45faab0c413e5b2411d65438efe32049793a35a44795d55e58c4d8e4d`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Thu, 28 Aug 2025 12:46:41 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1757289600'
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 28 Aug 2025 12:46:41 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_VERSION=8.4.12
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.12.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.12.tar.xz.asc
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_SHA256=c1b7978cbb5054eed6c749bde4444afc16a3f2268101fb70a7d5d9b1083b12ad
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 28 Aug 2025 12:46:41 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:d6e01c57fc6d674eef68e6bfe57a080b0a70c1c25810b7d6e769151bad3645bf`  
		Last Modified: Mon, 08 Sep 2025 21:12:32 GMT  
		Size: 31.3 MB (31289784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b0536a2d4d94901beb40c3ced04f50bc237b4925659ceabf716834ac6ca1101`  
		Last Modified: Mon, 08 Sep 2025 22:03:35 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc27efc25c3d3403cdb3a98d66313b4674a792bb7e845039ce835ad7a0abd605`  
		Last Modified: Tue, 09 Sep 2025 12:49:23 GMT  
		Size: 116.1 MB (116136855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9193f06b445fe74131814fde6d3c7cb5a52eab17f173a9c9f20eb63b4a359e34`  
		Last Modified: Mon, 08 Sep 2025 21:45:55 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e641bcf94b8d8b1a9a9ef22f87364728d531bbaeacab9e5a2da3fde3630743a`  
		Last Modified: Tue, 09 Sep 2025 12:49:14 GMT  
		Size: 13.8 MB (13782920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc4681c344f98dd70b4d31f3ecbab1ae3cd4e0e76a3d0ab0693f4d6ce2b026d1`  
		Last Modified: Mon, 08 Sep 2025 22:03:35 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3922a60bea15e4eb98b97a5c00c667eff0259e707c4173cb4ed8cd2b57814e0`  
		Last Modified: Tue, 09 Sep 2025 12:49:14 GMT  
		Size: 25.6 MB (25584309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b824882dc3212f50774ff44b24bead52d1ef685162071e1eeb395c7fd549e127`  
		Last Modified: Mon, 08 Sep 2025 22:03:35 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e53147e4fd12c2c62972236eb2437dcceda921342672b45fde04c2a5d4cef11`  
		Last Modified: Mon, 08 Sep 2025 22:03:35 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7330abf02c9fe16aed5f8cb4f396b822afab4896d2d760d0522e6dd5691a2e0f`  
		Last Modified: Mon, 08 Sep 2025 22:03:35 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:zts-trixie` - unknown; unknown

```console
$ docker pull php@sha256:4f2813baf433d4c583651a6cb43ea30f0f5001f933fde5bc6a6c86f6ad0b92c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6701808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60f3f45ae63b2c55f497c6c3c5c7e412459e732e44b2dfdc00f418a391418158`

```dockerfile
```

-	Layers:
	-	`sha256:bb9dfa012e86d8f9c3e3ebf64cc429d74c42323bea3b0b7bb6c8ad84c9ebafcf`  
		Last Modified: Mon, 08 Sep 2025 22:58:25 GMT  
		Size: 6.7 MB (6658088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03081bc5d498cfd9b8e034c2e3b6cd1886ff32a01276e9f488f88e90fa8fa298`  
		Last Modified: Mon, 08 Sep 2025 22:58:26 GMT  
		Size: 43.7 KB (43720 bytes)  
		MIME: application/vnd.in-toto+json

### `php:zts-trixie` - linux; ppc64le

```console
$ docker pull php@sha256:bb841acf6ad7217dc8e22e8a5099272c90ad0ac8e03d5b5dc3cae1ab77580296
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.5 MB (183488548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:530c8c8cdc533c7b453baa5323f1ceee01267e4f78c1ee4b9a8c29ac64997cbd`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Thu, 28 Aug 2025 12:46:41 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1757289600'
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 28 Aug 2025 12:46:41 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_VERSION=8.4.12
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.12.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.12.tar.xz.asc
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_SHA256=c1b7978cbb5054eed6c749bde4444afc16a3f2268101fb70a7d5d9b1083b12ad
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 28 Aug 2025 12:46:41 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:d11c44105444ef722eccd8c92c6b2fce9986e3274ba9b346e044a458c0425852`  
		Last Modified: Mon, 08 Sep 2025 22:03:02 GMT  
		Size: 33.6 MB (33594351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b92c5533102d377092f90a64ce96643efc2f90c8132806309f689ef1a0ff55f1`  
		Last Modified: Mon, 08 Sep 2025 22:47:15 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f75c51011b81d61508b6739213b2956df239d3867fbd1b77eade087e74d53486`  
		Last Modified: Mon, 08 Sep 2025 23:13:00 GMT  
		Size: 109.6 MB (109596656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:169d6bf5057cf9cbf3d82654ad276e19db98dfaca1501852995c56026182bd5a`  
		Last Modified: Mon, 08 Sep 2025 22:47:18 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6e4d5f8e44780ac25bebfa34d6191af197331f818be8ccd214b1b8164a3e93a`  
		Last Modified: Mon, 08 Sep 2025 23:35:09 GMT  
		Size: 13.8 MB (13783166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2508ca69d57915724e6d4016caa3a804666f309d53979798065874f5ad6414ff`  
		Last Modified: Mon, 08 Sep 2025 23:17:06 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01db8c6429fe3ac4b54da86f95013efc83290ad94e378868af62b75b151fdda9`  
		Last Modified: Tue, 09 Sep 2025 09:51:52 GMT  
		Size: 26.5 MB (26510490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:308dde7dea4d030ab6b6503ec9146472c6e59322c7fd3107b6e55aadc0952c5c`  
		Last Modified: Mon, 08 Sep 2025 23:17:16 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4b4ac1e456e0fa5f5608d72e205f2be927bf021251719baf8cb34ba510300bb`  
		Last Modified: Mon, 08 Sep 2025 23:17:20 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff68c31d9833aab6d9b7fdeb0ad83621b321cd720b4ac077de61224c6be1a5ba`  
		Last Modified: Mon, 08 Sep 2025 23:17:23 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:zts-trixie` - unknown; unknown

```console
$ docker pull php@sha256:c8afe5da5ae3ceca93c34eddc01057b6086814b4f9f6ecb880c45adcdc68a0ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6727748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c4f5ccf3495efbe553c0f570f94fded013a0ace40131184ad42aa75338768eb`

```dockerfile
```

-	Layers:
	-	`sha256:557e57d10a642e0239eb8c6103e61380d6c8bb7da7b9823b0da7a13e239e4dca`  
		Last Modified: Mon, 08 Sep 2025 23:14:36 GMT  
		Size: 6.7 MB (6683884 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6780da2cf47393a08ae1f16fdcb9affc169ca89fc73844717c5511b11a29ec68`  
		Last Modified: Mon, 08 Sep 2025 23:14:37 GMT  
		Size: 43.9 KB (43864 bytes)  
		MIME: application/vnd.in-toto+json

### `php:zts-trixie` - linux; riscv64

```console
$ docker pull php@sha256:5871fee9cbdb8ff2fe966a0ac25f1797bec293bd122fbb37e13f925b6949773c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.2 MB (213236645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d45e007a9c0a9be86c5a5a13ecf68d10ecb029cf0825dc2ddb442db37d72d032`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Thu, 28 Aug 2025 12:46:41 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1757289600'
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 28 Aug 2025 12:46:41 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_VERSION=8.4.12
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.12.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.12.tar.xz.asc
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_SHA256=c1b7978cbb5054eed6c749bde4444afc16a3f2268101fb70a7d5d9b1083b12ad
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 28 Aug 2025 12:46:41 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:dd4e3fb8766f676c414c0c55be0f5d9f6e6359dc2628caa804016b0f2ba461f2`  
		Last Modified: Tue, 09 Sep 2025 01:07:45 GMT  
		Size: 28.3 MB (28271372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faae3e77da310b8f6abd1c47c2c908b688364ff453788dffc1ea3755bda9a618`  
		Last Modified: Tue, 09 Sep 2025 18:54:07 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d25a2ea3673eda57f8891f3fdc7a2b5bd7baa28ce076ff3427218ba02258d5f`  
		Last Modified: Tue, 09 Sep 2025 20:58:30 GMT  
		Size: 146.6 MB (146579169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5fd9eb164bef808ab9cc8b8afd7d2a60572baa81f3ff4c56c34d90a36945fb1`  
		Last Modified: Tue, 09 Sep 2025 18:54:07 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b3c6ca0ae3c8b3d355932f52d0923973a557861b1dad79e5444f5645aedeb75`  
		Last Modified: Tue, 09 Sep 2025 23:03:28 GMT  
		Size: 13.8 MB (13789419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5de439b5587d1ab6b531acfd230e58194c76c8a59d0e8b10c9923eeb8fa94aa`  
		Last Modified: Tue, 09 Sep 2025 23:03:27 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58af678444b1a5917da7cb5596ec3d0393b7564f789405beccd271faf166c571`  
		Last Modified: Wed, 10 Sep 2025 02:03:49 GMT  
		Size: 24.6 MB (24592795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac09d6722f58cfbdcf95001f69689efd13551997acdba07ca02aaa24600bb6d`  
		Last Modified: Wed, 10 Sep 2025 02:03:47 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:159a2033879a0caea93ff5b274a7d321d06b42f981fea2d6f025a10b74685f81`  
		Last Modified: Wed, 10 Sep 2025 02:03:48 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:def14fbb68e63f14f94c2d9a8333b1632395ef8f92ca75c33db2a431423b2fc9`  
		Last Modified: Wed, 10 Sep 2025 02:03:48 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:zts-trixie` - unknown; unknown

```console
$ docker pull php@sha256:9bb85ce8bef3a15a1c634448f7d1a3572bb639fd7a7cf890acd4b5d9571f3dc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6799837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92237e0720ec4396608d4e4bb9ed0ef1a081b2f9bc4efd169754390531ae49fc`

```dockerfile
```

-	Layers:
	-	`sha256:886e334d623a07ce2f390871da86052d585e31cff7437088bc7a29b7b8717732`  
		Last Modified: Wed, 10 Sep 2025 04:55:12 GMT  
		Size: 6.8 MB (6755973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83ac54fc558298d330be41400b21639df0008df93ec83adead03e200ccfb92fc`  
		Last Modified: Wed, 10 Sep 2025 04:55:13 GMT  
		Size: 43.9 KB (43864 bytes)  
		MIME: application/vnd.in-toto+json

### `php:zts-trixie` - linux; s390x

```console
$ docker pull php@sha256:8e2c90b5e7b11baa4a6cb137a6efcc1f0c7bdca6354c6e5855fc2e6573aa327d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.1 MB (162132109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09af004ae99367a21e3faf97234870fc49681cd0d946bf657a9a770eb6881cc3`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Thu, 28 Aug 2025 12:46:41 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1757289600'
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 28 Aug 2025 12:46:41 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_VERSION=8.4.12
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.12.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.12.tar.xz.asc
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_SHA256=c1b7978cbb5054eed6c749bde4444afc16a3f2268101fb70a7d5d9b1083b12ad
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 28 Aug 2025 12:46:41 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:8af003c0cb712f415b555d33f1c4a9cc3fad82782766d388f3426c4d807a5ab2`  
		Last Modified: Mon, 08 Sep 2025 21:53:51 GMT  
		Size: 29.8 MB (29832904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b232e52aa98f49ca19e377e7da8d1acab05ee220da9d68dd81f728babf0c517`  
		Last Modified: Mon, 08 Sep 2025 21:55:17 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6478857e6e1b537f952dd40041dacfe05d27f69962e33a4c06fb4ff6381f540`  
		Last Modified: Mon, 08 Sep 2025 23:24:43 GMT  
		Size: 92.6 MB (92562517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa056e798e1e4f9bfdcf75b3f6f5791a4f0e696861934a12a910a510c2ac018d`  
		Last Modified: Mon, 08 Sep 2025 21:55:20 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6791b8b7b534a67db4c8aa2e1e8be2537fb2b5aa0e027b8fed33f973699b57e`  
		Last Modified: Mon, 08 Sep 2025 23:24:35 GMT  
		Size: 13.8 MB (13782379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:521ee8649b9b758d7d86588c9947141c2a79a9b036270f3aa1d15a6fa44f6762`  
		Last Modified: Mon, 08 Sep 2025 22:38:33 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca6f2660ddf4cee6789794dec208e961f669b1d4c8f50e661830aef7368fb43`  
		Last Modified: Tue, 09 Sep 2025 00:45:30 GMT  
		Size: 26.0 MB (25950422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03d89dbd6448884f783bb089775f33ba98d7df2d2981de358b07abea17ceef69`  
		Last Modified: Mon, 08 Sep 2025 23:11:50 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4918d63e7b997b24c90b6573899e4ee3120f9e2c29e61befa040cd16d2d6c2ef`  
		Last Modified: Mon, 08 Sep 2025 23:11:50 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:117444bc1a84093e305bc2dc7f79bdbe651595c615ce1d4fcfd714e82391afe6`  
		Last Modified: Mon, 08 Sep 2025 23:11:50 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:zts-trixie` - unknown; unknown

```console
$ docker pull php@sha256:85782fee34c8924ab1a115c6917739b4d3f831ace90148f71a7d601f9d33667f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6545259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:891ee852c3e5f31adbcaf5c3fe10163f9381672d61d52755b39e422bf611c874`

```dockerfile
```

-	Layers:
	-	`sha256:76fb0d3a5a97eff2f04b2b9c72424d19f9e165da1e5f3b824e6aa36bf98e570d`  
		Last Modified: Mon, 08 Sep 2025 22:58:43 GMT  
		Size: 6.5 MB (6501483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cda6542a52d60ac2112089c2406473c7514bef15c16034ee905326ef3b06839f`  
		Last Modified: Mon, 08 Sep 2025 22:58:44 GMT  
		Size: 43.8 KB (43776 bytes)  
		MIME: application/vnd.in-toto+json
