## `php:zts`

```console
$ docker pull php@sha256:2eb7cf55ed14918b0bdae96b0b96a4c3efc1a8dd4d21f5fece0966b0f77b34f4
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

### `php:zts` - linux; amd64

```console
$ docker pull php@sha256:280ded05f02cb48991c2437ee45dff954fe130d15b86fdd1af8c69053f7d6dc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.2 MB (187245140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d9691848c3a5d8661392b83d7f19c46cfd2a497098867a9ec5adfb35be6a9ba`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Thu, 13 Feb 2025 21:31:38 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Thu, 13 Feb 2025 21:31:38 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 13 Feb 2025 21:31:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 13 Feb 2025 21:31:38 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 13 Feb 2025 21:31:38 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_VERSION=8.4.4
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.4.tar.xz.asc
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_SHA256=05a6c9a2cc894dd8be719ecab221b311886d5e0c02cb6fac648dd9b3459681ac
# Thu, 13 Feb 2025 21:31:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 13 Feb 2025 21:31:38 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:7cf63256a31a4cc44f6defe8e1af95363aee5fa75f30a248d95cae684f87c53c`  
		Last Modified: Tue, 25 Feb 2025 01:29:30 GMT  
		Size: 28.2 MB (28219301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8546d3971dc8d0ff9380d230de57d8a4b0bc49119d4c82473bc969e8701e29`  
		Last Modified: Tue, 25 Feb 2025 02:22:56 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cd5cdacb3c1effe6fb1ea6805fefa06302add9e25fd970ef28cba20691ae338`  
		Last Modified: Tue, 25 Feb 2025 02:22:57 GMT  
		Size: 104.3 MB (104345657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba2bf011bbe715b94bb7a0d56d6a30ae7ae458c4de08fbb0073e6966bd5e10b2`  
		Last Modified: Tue, 25 Feb 2025 02:22:56 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daeef261a2a459f7f1c47da61c21e62d2f03f03bb1ceb8950c39a44c6d93eb35`  
		Last Modified: Tue, 25 Feb 2025 02:22:56 GMT  
		Size: 13.7 MB (13698392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9927a5059ad6b3df4f5f039e0376bc55c9ac03fe35dbcd36e531088f847cc5eb`  
		Last Modified: Tue, 25 Feb 2025 02:22:57 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9a11eaacbe24f59a59c9a3779cd61eef3fb97ebccf291b3eed4c01fabb13e36`  
		Last Modified: Tue, 25 Feb 2025 02:22:57 GMT  
		Size: 41.0 MB (40978158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a69157327c63f91f6ec0a63aca51b33439b73048ce4f56f9990aa1e960331964`  
		Last Modified: Tue, 25 Feb 2025 02:22:57 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9347db04701ead1b2659ccd1201e0ec851f8198dca2796438f7eddfd7c9c26f9`  
		Last Modified: Tue, 25 Feb 2025 02:22:57 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:zts` - unknown; unknown

```console
$ docker pull php@sha256:757a36e4c9c6fb0b99051b4c3e99967f48a1c3c06f7f64b24e72cf9ed4f526dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6265975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afc2f95793f27fce1bd635aa5618f3e869d11d36b4aca5cd8dabc93ec20947ac`

```dockerfile
```

-	Layers:
	-	`sha256:9a646c212bc3a3981ac18fa542409173b88a1fe7dc7347827aa057d32c919755`  
		Last Modified: Tue, 25 Feb 2025 02:22:56 GMT  
		Size: 6.2 MB (6225220 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:090e0c555183912b3ff98acbdbc67c38076ad903eb9e9d971b2cdd3b62c39abe`  
		Last Modified: Tue, 25 Feb 2025 02:22:56 GMT  
		Size: 40.8 KB (40755 bytes)  
		MIME: application/vnd.in-toto+json

### `php:zts` - linux; arm variant v5

```console
$ docker pull php@sha256:26b84c377cc96b1ec828567dca5dbaf9ecaa9c8bb4ef1329de12fb119e5314ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.2 MB (160238671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64204d0496b91472a9278101698a56209f9128fde5a12061fa1aa8e64bfc64b8`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1740355200'
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 13 Mar 2025 17:27:40 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_VERSION=8.4.5
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.5.tar.xz.asc
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_SHA256=0d3270bbce4d9ec617befce52458b763fd461d475f1fe2ed878bb8573faed327
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 13 Mar 2025 17:27:40 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:d8a77b84d73cc90f2bbd622ec970d928c4f14e4be51927c88b7c15b7b6772382`  
		Last Modified: Tue, 25 Feb 2025 01:30:58 GMT  
		Size: 25.7 MB (25740630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3014e21b6e4396df02c7cc3c5f126fa29d531fa5a1ad0b40b80de6794ae2694`  
		Last Modified: Tue, 25 Feb 2025 02:51:17 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:858e0a56f6198eb0af5102ce28eda7b5a34384f5b54701b7346487229bff9e9c`  
		Last Modified: Tue, 25 Feb 2025 02:51:20 GMT  
		Size: 82.0 MB (81993202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c24b0f2499da71327f565769347ea1f63e9070dfa8385025f0465d80e603c361`  
		Last Modified: Tue, 25 Feb 2025 02:51:17 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e150f96764dd58539846c6e7b5484721cacd9608e5e49da3ef779e041dae899`  
		Last Modified: Fri, 14 Mar 2025 00:12:26 GMT  
		Size: 13.7 MB (13712529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b1018ab699293a1333b27006b19ea33496d0a6740983e2627d53ef7f2ec718a`  
		Last Modified: Fri, 14 Mar 2025 00:12:25 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbba4b2a2968db3223aff3042e48394324f19449f7efc5cfddf2237c4c04e851`  
		Last Modified: Fri, 14 Mar 2025 00:41:05 GMT  
		Size: 38.8 MB (38788670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6660b1072abf111ed82c2780d5b0d1f1c5631ab7799af3ba764473c2df2eb86b`  
		Last Modified: Fri, 14 Mar 2025 00:41:03 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b461c3a0a14f3d022135e2ef0ef2e1a3077fc3a6c19e731e81e79bf07211e2de`  
		Last Modified: Fri, 14 Mar 2025 00:41:04 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:zts` - unknown; unknown

```console
$ docker pull php@sha256:211ebcc99339a1e3a16ed991afe783d0cf3229d75825034e21a244e87c7b726c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6077135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f43b7ce62f00ca30101dfc5124a1c6d1d097973254db05d6c7073e583d78f1e8`

```dockerfile
```

-	Layers:
	-	`sha256:11e76c792f059ece8097b871162c601118cc7643baf95ea51d9d5f547116a812`  
		Last Modified: Fri, 14 Mar 2025 00:41:02 GMT  
		Size: 6.0 MB (6036214 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54249ebe82cb5082d47d65aff9b1a34228ca1fd56da84f00563da0021b3161c1`  
		Last Modified: Fri, 14 Mar 2025 00:41:02 GMT  
		Size: 40.9 KB (40921 bytes)  
		MIME: application/vnd.in-toto+json

### `php:zts` - linux; arm variant v7

```console
$ docker pull php@sha256:674317042dc0774080a98a56ed416c9842a73ae4c0ce00cd9e4028872a292dba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.9 MB (150909745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73b158c1b7e7fe1496df5daff7146c1517be08c7864781c2051de9bc5c8fb395`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Thu, 13 Feb 2025 21:31:38 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1740355200'
# Thu, 13 Feb 2025 21:31:38 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 13 Feb 2025 21:31:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 13 Feb 2025 21:31:38 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 13 Feb 2025 21:31:38 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_VERSION=8.4.4
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.4.tar.xz.asc
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_SHA256=05a6c9a2cc894dd8be719ecab221b311886d5e0c02cb6fac648dd9b3459681ac
# Thu, 13 Feb 2025 21:31:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 13 Feb 2025 21:31:38 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:b47565bb13c54d9e609fa36aeddfc2e70b47de981bac54a6d090c2148f2f4fc4`  
		Last Modified: Tue, 25 Feb 2025 01:30:40 GMT  
		Size: 23.9 MB (23919734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81d7e09b1d1dfb9227526dbb14ab0477c0b3e235584b36c16282a130f9eb0f3c`  
		Last Modified: Tue, 25 Feb 2025 02:45:28 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:195d4e13a8d04cec48669402c294b437f110e69a04f231bf7f4fb038ce009feb`  
		Last Modified: Tue, 25 Feb 2025 02:45:31 GMT  
		Size: 76.2 MB (76162862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f86b4b4427af4c394c935ad45142cba4e205bc21eb933d83f2d2432a5bb3cb64`  
		Last Modified: Tue, 25 Feb 2025 02:45:28 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18044719a3c0708896871c9b84c8956489062467fb3ee8565d99f0444b6e72bf`  
		Last Modified: Tue, 25 Feb 2025 02:45:29 GMT  
		Size: 13.7 MB (13696518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d73b08d9b04d37e3a4465335a563f1a3e95fb9cbcc80b2a50f9f4c1e4124727`  
		Last Modified: Tue, 25 Feb 2025 02:45:29 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606633b5a966cca742c4c68efe046969444fd768b6fc739aba8c243896ea5d8e`  
		Last Modified: Tue, 25 Feb 2025 02:56:47 GMT  
		Size: 37.1 MB (37127002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26b6c2e28866230df6189188867137ed5d65b8f6d4eeef02fb4e4a635f9b9bb1`  
		Last Modified: Tue, 25 Feb 2025 02:56:45 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e12089a8c5e2be45a9c4901196a8fe21083c76760320c8a50dd2fa1f2a170e52`  
		Last Modified: Tue, 25 Feb 2025 02:56:45 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:zts` - unknown; unknown

```console
$ docker pull php@sha256:baad14ef52fa618fb185c5b8f0214656928f21f1b5a8f23a474e275e5c901bda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6081076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79f11d7e17a7d9698717d6358e4f0feec72e974c37dbe0e5499c54cced35a3c3`

```dockerfile
```

-	Layers:
	-	`sha256:f7189052c8352b91c2260d57f220d582f1cf4ad0dd84e4cd70fcdee3d55da770`  
		Last Modified: Tue, 25 Feb 2025 02:56:46 GMT  
		Size: 6.0 MB (6040156 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61befbf92dabb6a6303212763eb3ee9bfa9a450f5f4e1b3f223e139973dd818a`  
		Last Modified: Tue, 25 Feb 2025 02:56:45 GMT  
		Size: 40.9 KB (40920 bytes)  
		MIME: application/vnd.in-toto+json

### `php:zts` - linux; arm64 variant v8

```console
$ docker pull php@sha256:9251a52fe85f8f4e7732812b05549fe32e48c69800076d0e8004dee7a2071306
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.3 MB (180327329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b8b968c1a40443f8ac333c9eac486e646866633eccaab5ce6961a92d02e8709`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Thu, 13 Feb 2025 21:31:38 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Thu, 13 Feb 2025 21:31:38 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 13 Feb 2025 21:31:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 13 Feb 2025 21:31:38 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 13 Feb 2025 21:31:38 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_VERSION=8.4.4
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.4.tar.xz.asc
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_SHA256=05a6c9a2cc894dd8be719ecab221b311886d5e0c02cb6fac648dd9b3459681ac
# Thu, 13 Feb 2025 21:31:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 13 Feb 2025 21:31:38 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31676cd976ed7c1a1f79275ef2602fefb67765b353e429d88aab3fd76863e399`  
		Last Modified: Tue, 25 Feb 2025 03:03:46 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e6e69341e71d07089c45827b72bbbf8ca0698042a25ca2375d9c71797edd77e`  
		Last Modified: Tue, 25 Feb 2025 03:03:49 GMT  
		Size: 98.1 MB (98130460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5ee28dda6888ebc4fc51f7f52c135986c07171dad8ce5a8fafed9d2f65d62ec`  
		Last Modified: Tue, 25 Feb 2025 03:03:47 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f749205b2879ea09b2ef4bd000f0925816fb68f04a32f610ed56628901dfe5d1`  
		Last Modified: Tue, 25 Feb 2025 03:03:47 GMT  
		Size: 13.7 MB (13698282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4de543bbdee30c62ad737cfb7180fb0e3bcd2d20fd66e7ca635a7b49f012e65c`  
		Last Modified: Tue, 25 Feb 2025 03:03:47 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2a42d7979f29f786aeca2b3c9f2fb6483ecec19ce146cacb9ab64541499823d`  
		Last Modified: Tue, 25 Feb 2025 03:14:13 GMT  
		Size: 40.4 MB (40446529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76553f00377daad9b372106ae0d137e63fd0fc877fc136ec551154c5bee3fae7`  
		Last Modified: Tue, 25 Feb 2025 03:14:11 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d640ac0a960cb953081f801c9ae177f76bee1409de0360e516ab6d4de7969a0b`  
		Last Modified: Tue, 25 Feb 2025 03:14:11 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:zts` - unknown; unknown

```console
$ docker pull php@sha256:df596efdb93b529369769f7e734c7ecc07ae081975b1f5131b60cc7018aa9410
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6294633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b4b35d24f5863dafab2e4bf546078b1ec15b0739ce730b49ac01469f97d534f`

```dockerfile
```

-	Layers:
	-	`sha256:c9b27c70094c3cf207484bee615ecdbc95bc6f2971c7ec465f298cc5405a7117`  
		Last Modified: Tue, 25 Feb 2025 03:14:11 GMT  
		Size: 6.3 MB (6253658 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebf9e9560a524e9111e684f0387a2b650db031d29e0c6573059148d437d2ee13`  
		Last Modified: Tue, 25 Feb 2025 03:14:11 GMT  
		Size: 41.0 KB (40975 bytes)  
		MIME: application/vnd.in-toto+json

### `php:zts` - linux; 386

```console
$ docker pull php@sha256:f91c34c366a198d6b69607da29a43d2010468020f26afde498b2e5ce8016be5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.2 MB (186221193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:017ce5f8d6c1d5d82a5198da957a1ee5ee3511ac76eaa187e481c7142e55b65c`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1740355200'
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 13 Mar 2025 17:27:40 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_VERSION=8.4.5
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.5.tar.xz.asc
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_SHA256=0d3270bbce4d9ec617befce52458b763fd461d475f1fe2ed878bb8573faed327
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 13 Mar 2025 17:27:40 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:a424c1d96f8a4c2d56031254051a822634b1b977ca2bc56e7fd2adc3e742703a`  
		Last Modified: Tue, 25 Feb 2025 01:29:49 GMT  
		Size: 29.2 MB (29194590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83498aac653c6f3fd1f510c84af8967dbbbf5265a21a13f2d21b71d12013a34b`  
		Last Modified: Fri, 14 Mar 2025 00:13:16 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a86254289413b52d7581f4b747f038e8990b3a7f70130450ef48d526aad7128e`  
		Last Modified: Fri, 14 Mar 2025 00:13:39 GMT  
		Size: 101.5 MB (101513175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5ae944fad43526214c5a496f5b2c7d6b8ded38e9ab67fe1f7d5ad6cfe101e75`  
		Last Modified: Fri, 14 Mar 2025 00:13:36 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55bfe11b49da2ca48810e1b11413cefefb7f8225c0e1f5ab8a523585489ba7fb`  
		Last Modified: Fri, 14 Mar 2025 00:13:37 GMT  
		Size: 13.7 MB (13713696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdb1d22cd584cdc3ed58da69f36ab7ccc885a95c42b85c97212457621488262e`  
		Last Modified: Fri, 14 Mar 2025 00:13:36 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ce7af038fee7bdfa4412a57f44a9b34a6c2c37a4eca1a9cf00395bfcc0bc893`  
		Last Modified: Fri, 14 Mar 2025 00:13:38 GMT  
		Size: 41.8 MB (41796094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7d646b0bd082d900a856093ec97491d261b2213c8c48bf9037c6e1cc9de31cd`  
		Last Modified: Fri, 14 Mar 2025 00:13:37 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d9b632529def3f76c7a7c1c65af762526a25d3ff2af5fb3f29f55661534320`  
		Last Modified: Fri, 14 Mar 2025 00:13:38 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:zts` - unknown; unknown

```console
$ docker pull php@sha256:82a060b1a99a76274cd4de052e2f1ea7adfbb8acccfbe927d78f7a22dc4d20c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6246220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46bcd65c6576a9c6516ee73ff73d4468ca22433bf0ccd054bbc65db6a8948d9f`

```dockerfile
```

-	Layers:
	-	`sha256:b6b5bf2f1bad18a2b7b06b0033957509732b7c5f3a0a3dd67b3a8f935315b8de`  
		Last Modified: Fri, 14 Mar 2025 00:13:36 GMT  
		Size: 6.2 MB (6205529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:631759a140790314b31b6b216a8b14601366ca4cac5b6c96f4f10942b58064e5`  
		Last Modified: Fri, 14 Mar 2025 00:13:36 GMT  
		Size: 40.7 KB (40691 bytes)  
		MIME: application/vnd.in-toto+json

### `php:zts` - linux; mips64le

```console
$ docker pull php@sha256:c097d5899b66edd80a1e78f9f03c863e03c41d5ed4a4ecd0dedef02ca2d8ae9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.3 MB (162316013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3719439d0641d63a701b95af929a0f447c3a9dc48075c5aee8c30e552d847850`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1740355200'
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 13 Mar 2025 17:27:40 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_VERSION=8.4.5
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.5.tar.xz.asc
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_SHA256=0d3270bbce4d9ec617befce52458b763fd461d475f1fe2ed878bb8573faed327
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 13 Mar 2025 17:27:40 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:1851efe37d59b19d5c7092778464657e31dbfae35874c19fb94fb95542e2fba7`  
		Last Modified: Tue, 25 Feb 2025 01:30:49 GMT  
		Size: 28.5 MB (28493681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80d36a7b1e0c4904256c3222f554e2f9053a6ce6cb06dac686a36004c2968943`  
		Last Modified: Tue, 25 Feb 2025 04:23:17 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:878fe44e60469208a4e6a6cc56a06ba4bd6418ae0d09468c66a29bce7fc35e03`  
		Last Modified: Tue, 25 Feb 2025 04:23:25 GMT  
		Size: 80.7 MB (80668722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03653780888887368ef36859920d833d269d38c1e54ffb86bae392b6bfcfde65`  
		Last Modified: Tue, 25 Feb 2025 04:23:17 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:407c23b34911bcd4afa36c2b9b4114bb104dab3c977961b56c5e01584a1bffc5`  
		Last Modified: Fri, 14 Mar 2025 00:26:18 GMT  
		Size: 13.7 MB (13712081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a81cac3ab1de9a0c5678d6b4762c946c5f75a2ed19c02698dd008112ad53d6f7`  
		Last Modified: Fri, 14 Mar 2025 00:26:16 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5acb1acff3c6f9876d65c48921b8c2f2efd7dbbf0b4cdacbaa77615f835a8a02`  
		Last Modified: Fri, 14 Mar 2025 04:45:06 GMT  
		Size: 39.4 MB (39437885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9be877148c0f07ead89d91e7d043088cecb0e4de817d852c372f313eba874299`  
		Last Modified: Fri, 14 Mar 2025 04:45:02 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c8f137b9d5f4624896a9c4766c357ff1e130120e001f0e2ac3e7fa30513add4`  
		Last Modified: Fri, 14 Mar 2025 04:45:02 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:zts` - unknown; unknown

```console
$ docker pull php@sha256:27d7a57f886d663042fc0dcfeaab0f88d982bd6d0359295fad4a0fd7200dd52a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.6 KB (40650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3f7399e84d343337c082c3b4fceec423ce77272b9ce687322bca5857954ff91`

```dockerfile
```

-	Layers:
	-	`sha256:d89e30180ff1756daea3b6ccd36fb0be0be67187349e8eb7274b2458c7ea5187`  
		Last Modified: Fri, 14 Mar 2025 04:45:02 GMT  
		Size: 40.6 KB (40650 bytes)  
		MIME: application/vnd.in-toto+json

### `php:zts` - linux; ppc64le

```console
$ docker pull php@sha256:2274b534364895e3a7f733ca7b50b8adca4817b4091469868ac798879e38106f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.1 MB (192073560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:178218ab4d86fc4a1b6fef88386f764a6675b01f691e9350dc03bd3be8e8ce52`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1740355200'
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 13 Mar 2025 17:27:40 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_VERSION=8.4.5
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.5.tar.xz.asc
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_SHA256=0d3270bbce4d9ec617befce52458b763fd461d475f1fe2ed878bb8573faed327
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 13 Mar 2025 17:27:40 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:4713de4e13d024eec0b1cb2d083909104c2a36ed3ffba92c5cf710577a33ad45`  
		Last Modified: Tue, 25 Feb 2025 01:30:47 GMT  
		Size: 32.1 MB (32052314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35bbbae4d2dc0350f7df1634e33daf64fe78cb672182650c700a26750b33b64c`  
		Last Modified: Tue, 25 Feb 2025 02:59:24 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e7f7bed916e76b3a3b176b4e6a5bcfe6e10e39a6c423be8fc3575115d7b1e06`  
		Last Modified: Tue, 25 Feb 2025 02:59:28 GMT  
		Size: 103.3 MB (103323545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21d9943a0d5cef1bf22e1a6d5df4b38af8052474c28fe7d9188d33c9e0190742`  
		Last Modified: Tue, 25 Feb 2025 02:59:24 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:822a546051d9f3e473b577fd15172b155853bd8cb79c8cf44ae4d42f28665e87`  
		Last Modified: Fri, 14 Mar 2025 00:11:53 GMT  
		Size: 13.7 MB (13713974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9ad382d3f0721f948b359d31966302852b44cdc6fedd5ac796ec04c007ad5d8`  
		Last Modified: Fri, 14 Mar 2025 00:11:51 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39e2f47d59ae42fb7bda02b37896899d928432a819fe0f1a0d6e470948b7fa09`  
		Last Modified: Fri, 14 Mar 2025 01:46:13 GMT  
		Size: 43.0 MB (42980096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb0ac492c7f83a55882527b51fc38597a5a99bf036354dc89dbdf81565e6bf59`  
		Last Modified: Fri, 14 Mar 2025 01:46:11 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78731cfc6d6bf183df95828b9cf6a2b70769ce4ad668de49233394b01d5df19d`  
		Last Modified: Fri, 14 Mar 2025 01:46:11 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:zts` - unknown; unknown

```console
$ docker pull php@sha256:7597bd0f475785fcaa891459d8e50aabfb7a2b12fed7033006c6a913dcb6519e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6242953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0de5e66a15789027a771fdb8c3d92a727e08209a12d74b1319d55613759eeb6a`

```dockerfile
```

-	Layers:
	-	`sha256:a68fdcc9f260d548ac00ebfd0f1a9f7053af51e2d325c704f62521f9f533c045`  
		Last Modified: Fri, 14 Mar 2025 01:46:12 GMT  
		Size: 6.2 MB (6202120 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd2db7bc99ba5fc12f571bd9e3f357361208504a8a8df3e670c266eb70b1a221`  
		Last Modified: Fri, 14 Mar 2025 01:46:11 GMT  
		Size: 40.8 KB (40833 bytes)  
		MIME: application/vnd.in-toto+json

### `php:zts` - linux; s390x

```console
$ docker pull php@sha256:e90d391e3f3efcc76a11371d6c7a3a79900cc57c2411fd3acf301b8db6226050
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.7 MB (161669161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39cb737be83b55357468201e25ac3301414c68a72b7298537038e2a55818eb8b`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1740355200'
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 13 Mar 2025 17:27:40 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_VERSION=8.4.5
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.5.tar.xz.asc
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_SHA256=0d3270bbce4d9ec617befce52458b763fd461d475f1fe2ed878bb8573faed327
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 13 Mar 2025 17:27:40 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:6d4d169c55c2ee02478b6705c4ba9e6795bffbbb872a22adfd95fb2484f2e85c`  
		Last Modified: Tue, 25 Feb 2025 01:30:03 GMT  
		Size: 26.9 MB (26864838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f83dfaf87e0f897b620f8faafcd35d93785d305460fb8a1f24f178152dc8ef4`  
		Last Modified: Tue, 25 Feb 2025 02:47:05 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:382c1a79d42d9a6f73ff6106cec8445a8fb8bc6a78380c02024ff5e71c740938`  
		Last Modified: Tue, 25 Feb 2025 02:47:06 GMT  
		Size: 80.8 MB (80817122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dd5ce3ea58656e03c29355d087376523130702c7a182e93a6e6c775d2e795dd`  
		Last Modified: Tue, 25 Feb 2025 02:47:05 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccf49b173ac460e94e4d31e84f970fab2bd0b9ae2601212e2d48c6e9a3481f4d`  
		Last Modified: Fri, 14 Mar 2025 00:15:55 GMT  
		Size: 13.7 MB (13713005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd948647d1bfbcd5b7f08c3eb73c506a148215db1c2eec707df8a79bc30a58af`  
		Last Modified: Fri, 14 Mar 2025 00:15:55 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:878a2106927307632fe422899efe6000eda25a24192a2e0b52156c7ce3b95701`  
		Last Modified: Fri, 14 Mar 2025 00:51:22 GMT  
		Size: 40.3 MB (40270556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adabb92d228c34e1862a58be7b22b3ee91632055220da8a9b350fa69baac325b`  
		Last Modified: Fri, 14 Mar 2025 00:51:21 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc418552fe4650f12e7718706ba02c0712fb438100b7fd018e224dbd98329a17`  
		Last Modified: Fri, 14 Mar 2025 00:51:21 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:zts` - unknown; unknown

```console
$ docker pull php@sha256:5b95f5dc36f9fefeda8da6b64a4b7d2551e4d9d6992dfee8847276b1e6047fc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6107414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3bf59180677068e575d2598b513526ffef29d5caabfce283f3529765e547baf`

```dockerfile
```

-	Layers:
	-	`sha256:02d771cca0d8b349e1f6413ba99f39ab53b9180496286d766ab8fda654096b19`  
		Last Modified: Fri, 14 Mar 2025 00:51:21 GMT  
		Size: 6.1 MB (6066666 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37aa8856e8a8863ce26d644afb88291d6464357714f38eb28cdaa5afdd4f2fd6`  
		Last Modified: Fri, 14 Mar 2025 00:51:21 GMT  
		Size: 40.7 KB (40748 bytes)  
		MIME: application/vnd.in-toto+json
