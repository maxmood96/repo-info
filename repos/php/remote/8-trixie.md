## `php:8-trixie`

```console
$ docker pull php@sha256:49a7f1e17ec846753e55c4e70ae6cc7c81227a937aaa2f65fce71fbdb8bf9481
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

### `php:8-trixie` - linux; amd64

```console
$ docker pull php@sha256:713e0e29e9c962fcccd6fa6693a6f5decbcacfd2e7dc13dfd85b8be20d677faa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.8 MB (188803053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84fe8b522f415c04007708ab414919826623d098cb9688db9f8aa9e821cd7d6d`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:05:02 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 24 Feb 2026 19:05:19 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 24 Feb 2026 19:05:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 19:05:19 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 24 Feb 2026 19:05:20 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 24 Feb 2026 19:05:20 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 24 Feb 2026 19:05:20 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 24 Feb 2026 19:05:20 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 24 Feb 2026 19:05:20 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Tue, 24 Feb 2026 19:05:20 GMT
ENV PHP_VERSION=8.5.3
# Tue, 24 Feb 2026 19:05:20 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.3.tar.xz.asc
# Tue, 24 Feb 2026 19:05:20 GMT
ENV PHP_SHA256=ce65725b8af07356b69a6046d21487040b11f2acfde786de38b2bfb712c36eb9
# Tue, 24 Feb 2026 19:05:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 24 Feb 2026 19:05:30 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:08:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 24 Feb 2026 19:08:23 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:08:24 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 24 Feb 2026 19:08:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 24 Feb 2026 19:08:24 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ebbfc22ec785db1947369fe92c6a215e23d03fd92d93a3ab0ee6ad66ece279`  
		Last Modified: Tue, 24 Feb 2026 19:08:44 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:218722ecf8c2c02b97723d8240b3f4d536a1b31a28758adbeaff3660e0544f3e`  
		Last Modified: Tue, 24 Feb 2026 19:08:48 GMT  
		Size: 117.8 MB (117842178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09ad1aa1cc2a571cd10925bd6332a15677c05f471a497cc13455dba5151e42e0`  
		Last Modified: Tue, 24 Feb 2026 19:08:44 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:749ef0438b4275e1ecd9b8b0c78dd77447644e94661c9b021d3d129166748613`  
		Last Modified: Tue, 24 Feb 2026 19:08:45 GMT  
		Size: 14.5 MB (14480791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65f0380f964d22ede567d57e7af71684a78e5fdb45233c5a1db8d1e4ef32f793`  
		Last Modified: Tue, 24 Feb 2026 19:08:46 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e45c0ea51b9500232d96eb76350cec62699283a523f10c104e439391b4db5d8f`  
		Last Modified: Tue, 24 Feb 2026 19:08:47 GMT  
		Size: 26.7 MB (26697811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75db0d6ce3955aac1f6b5b329b1c3a5a1d67e492d2f6c2084f53b79d0e12cbba`  
		Last Modified: Tue, 24 Feb 2026 19:08:47 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9e9b7a7e392ecc36be1e80bc6864024904393b0ec3ab14fa25cdd589b31deb9`  
		Last Modified: Tue, 24 Feb 2026 19:08:47 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-trixie` - unknown; unknown

```console
$ docker pull php@sha256:8dd5f1d29d50bbc8c5f89a8d4391f0c68b60c537bea281bb3275890d894299d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6728606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dfd068a725a90dad060e3e96bf2ede9c4c66b9f05ae3c807599ff2f4104e993`

```dockerfile
```

-	Layers:
	-	`sha256:47970d0574899a9b6ec220712b1b7eb7a55fccdfb54f9a317260e628591d4a9e`  
		Last Modified: Tue, 24 Feb 2026 19:08:45 GMT  
		Size: 6.7 MB (6685551 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb450ae3be10f34a7b4b62137c223de19a22f611135496cf0364bc6ed32ec3b7`  
		Last Modified: Tue, 24 Feb 2026 19:08:44 GMT  
		Size: 43.1 KB (43055 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-trixie` - linux; arm variant v5

```console
$ docker pull php@sha256:7740eb8d363ca144ed24ce2a87456b5a03f1f6bfe8d670058966de7c3fca9776
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.2 MB (160233757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78a55d8b73f59151cc30c94e5c9f13d7332d469609aa0d41fbb1041bb9c000a0`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:00:53 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 24 Feb 2026 19:01:16 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 24 Feb 2026 19:01:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 19:01:16 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 24 Feb 2026 19:01:16 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 24 Feb 2026 19:01:16 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 24 Feb 2026 19:01:16 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 24 Feb 2026 19:01:16 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 24 Feb 2026 19:01:16 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Tue, 24 Feb 2026 19:01:16 GMT
ENV PHP_VERSION=8.5.3
# Tue, 24 Feb 2026 19:01:16 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.3.tar.xz.asc
# Tue, 24 Feb 2026 19:01:16 GMT
ENV PHP_SHA256=ce65725b8af07356b69a6046d21487040b11f2acfde786de38b2bfb712c36eb9
# Tue, 24 Feb 2026 19:01:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 24 Feb 2026 19:01:30 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:04:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 24 Feb 2026 19:04:44 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:04:44 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 24 Feb 2026 19:04:44 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 24 Feb 2026 19:04:44 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:280a075cc1d2a97445b9f4430aa9774bfc38fc4217b7fc9d6a7b04e7e431cb65`  
		Last Modified: Tue, 24 Feb 2026 18:42:44 GMT  
		Size: 27.9 MB (27947608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54a4dd7516184511f985d792272c50b3225be5e5efa0acb9fc477df50027d930`  
		Last Modified: Tue, 24 Feb 2026 19:05:03 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eaacc23e894891dcfbb5b8bf1e5a5f410b2a9fb1ab22bc9c0e204715fd011af`  
		Last Modified: Tue, 24 Feb 2026 19:05:05 GMT  
		Size: 94.9 MB (94884175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aeca48b18070dc59cfda6b40e7305dd994923890c52006e313b6e2178a09072`  
		Last Modified: Tue, 24 Feb 2026 19:05:03 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d89f2967e3998198ff5adebf8c51e3d6cde34139e3d46ccd51c41764bf906047`  
		Last Modified: Tue, 24 Feb 2026 19:05:03 GMT  
		Size: 14.5 MB (14478660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16070324b689d3ac02911e2f033828881733714974bcf7aecbe81099e8e10cd3`  
		Last Modified: Tue, 24 Feb 2026 19:05:04 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ab5669c1ff96a5d7cbe3ce8983b7574241f1dffaefe455faba85045a90ce607`  
		Last Modified: Tue, 24 Feb 2026 19:05:06 GMT  
		Size: 22.9 MB (22919674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70399219a6e0932fd4b6275ec34e8bbd45e49b0ee64ec2150488cf566c79f71c`  
		Last Modified: Tue, 24 Feb 2026 19:05:05 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:534b85dece0d1a89ca86ea7996de1857d8d614c8423c705adbbd04b38a96f3c2`  
		Last Modified: Tue, 24 Feb 2026 19:05:05 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-trixie` - unknown; unknown

```console
$ docker pull php@sha256:0716357ed5e0d03cc836591fff19b501c33dd27c4fd0431d11adb04b7b774003
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6528750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a65589b3c148d73ec84d1ae8bb865abb29ba841df0ba8ed4de17a3c98708ac3`

```dockerfile
```

-	Layers:
	-	`sha256:1bcdfd7f13eedccee6b24bba3b29ba99a9bc1820153b8426aadbe2e63fc11195`  
		Last Modified: Tue, 24 Feb 2026 19:05:03 GMT  
		Size: 6.5 MB (6485461 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57385e481623e751f3680000de734b208cee34609705539ae4a33456addf3cdf`  
		Last Modified: Tue, 24 Feb 2026 19:05:03 GMT  
		Size: 43.3 KB (43289 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-trixie` - linux; arm variant v7

```console
$ docker pull php@sha256:d0f3fc0fa470adb3aeba928ef1fb391ab86eabe2082c9ffc8ea3c2a765217a2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.6 MB (148576091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a253c244532dd45bf3d3b2052ce07e58afd37b64d489099bad141066b7e6f01`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:05:51 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 24 Feb 2026 19:06:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 24 Feb 2026 19:06:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 19:06:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 24 Feb 2026 19:06:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 24 Feb 2026 19:06:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 24 Feb 2026 19:06:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 24 Feb 2026 19:06:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 24 Feb 2026 19:06:09 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Tue, 24 Feb 2026 19:06:09 GMT
ENV PHP_VERSION=8.5.3
# Tue, 24 Feb 2026 19:06:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.3.tar.xz.asc
# Tue, 24 Feb 2026 19:06:09 GMT
ENV PHP_SHA256=ce65725b8af07356b69a6046d21487040b11f2acfde786de38b2bfb712c36eb9
# Tue, 24 Feb 2026 19:06:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 24 Feb 2026 19:06:19 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:09:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 24 Feb 2026 19:09:09 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:09:09 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 24 Feb 2026 19:09:09 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 24 Feb 2026 19:09:09 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:be1f02cfc6708a9e39fcae481bc45544f342901641dd63341104a8ef3fa3cde9`  
		Last Modified: Tue, 24 Feb 2026 18:42:48 GMT  
		Size: 26.2 MB (26213745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:487a25dafc3b52cc5c7e3c7f67103b03a5efb085805918411d1973008798b9f7`  
		Last Modified: Tue, 24 Feb 2026 19:09:25 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c984d855b13c2d534a29e6cb6196b3c16c6c84526cd987256a362f563c0f4f3d`  
		Last Modified: Tue, 24 Feb 2026 19:09:27 GMT  
		Size: 86.2 MB (86246549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:592e34c85c7083d2997b553ff68cd6ad3bb3b98e20064399bd1c6d339e9935f3`  
		Last Modified: Tue, 24 Feb 2026 19:09:20 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a20fab39e319ea094bdfc1f432ce92c336edc815d032aca7b62ec17733d29193`  
		Last Modified: Tue, 24 Feb 2026 19:09:26 GMT  
		Size: 14.5 MB (14478691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dda3ed35c2a1b91dc0cc08a9b29ad491ac51f708b5303bd444ba63fe7ca017fc`  
		Last Modified: Tue, 24 Feb 2026 19:09:26 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddb4285515d3bf36b1e0cd6a649c244ccf703eae78776688abef7f826b15cba0`  
		Last Modified: Tue, 24 Feb 2026 19:09:27 GMT  
		Size: 21.6 MB (21633464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6317d773d81c7ee9560f3b673a21499d2766997980f3ed5e5e7b142e33212bb`  
		Last Modified: Tue, 24 Feb 2026 19:09:27 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:becf64c5253649fc2bb101bc526d199d4601b59c34a2e60feff085a010e0ee00`  
		Last Modified: Tue, 24 Feb 2026 19:09:27 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-trixie` - unknown; unknown

```console
$ docker pull php@sha256:7d9533cdcb30cae50ef21429a844ebfd95a83de5c0664aac2535997a193b4da8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6532716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdc50a30d1d692e6e26c411ed1bcd121ccd526990c2ec9de175a907f84626cd3`

```dockerfile
```

-	Layers:
	-	`sha256:69b89d7d4a955be8f57e5c6055da47e24dfd37716f1f66ba5037914534131015`  
		Last Modified: Tue, 24 Feb 2026 19:09:25 GMT  
		Size: 6.5 MB (6489427 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa53413d8779d1c75cba6687de59e2d731c25fe1fe3e20e4edc053b705c60ec7`  
		Last Modified: Tue, 24 Feb 2026 19:09:25 GMT  
		Size: 43.3 KB (43289 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-trixie` - linux; arm64 variant v8

```console
$ docker pull php@sha256:e90c6ba4d6793778df879ba660d4d8c9919032fff1119c41e9a29e901eb7741c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.7 MB (180726158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6302511b091c8cceee71aa6d6a9c1fd98f72420def7c63e08ed666b90669876c`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:08:40 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 24 Feb 2026 19:08:57 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 24 Feb 2026 19:08:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 19:08:57 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 24 Feb 2026 19:08:57 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 24 Feb 2026 19:08:57 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 24 Feb 2026 19:08:57 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 24 Feb 2026 19:08:57 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 24 Feb 2026 19:08:57 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Tue, 24 Feb 2026 19:08:57 GMT
ENV PHP_VERSION=8.5.3
# Tue, 24 Feb 2026 19:08:57 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.3.tar.xz.asc
# Tue, 24 Feb 2026 19:08:57 GMT
ENV PHP_SHA256=ce65725b8af07356b69a6046d21487040b11f2acfde786de38b2bfb712c36eb9
# Tue, 24 Feb 2026 19:09:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 24 Feb 2026 19:09:10 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:12:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 24 Feb 2026 19:12:18 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:12:18 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 24 Feb 2026 19:12:18 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 24 Feb 2026 19:12:18 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fc77aead35a10f4280d7e62e0c6c87d0d2fb50dbe7ab559afd6017170010d89`  
		Last Modified: Tue, 24 Feb 2026 19:11:37 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dc10a3d1d37f5fa2baaa4fe77581259b7da0ab39436f6dde3f5f8eec19fdbec`  
		Last Modified: Tue, 24 Feb 2026 19:12:42 GMT  
		Size: 110.2 MB (110163264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08425e5b72c3fce331c4a62e07570826b9eafaeccc019a69fc4a1af81923f7c5`  
		Last Modified: Tue, 24 Feb 2026 19:12:38 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb22dc8c2350b113b8b942c211f0c0019c0d72be63529105534dda8bbfedd45a`  
		Last Modified: Tue, 24 Feb 2026 19:12:39 GMT  
		Size: 14.5 MB (14480444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c188f56e6a93fee8f592a5f322e93ba572ad3ef887072debf29cb830f13cd266`  
		Last Modified: Tue, 24 Feb 2026 19:12:39 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ebd6e006843ffc883dc36914d31eb830bc73b7f870fbf46bf8fb541b45cec5d`  
		Last Modified: Tue, 24 Feb 2026 19:12:41 GMT  
		Size: 25.9 MB (25938714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc8cd2434f64caa12510c075a25e884daa12774ce8fcbf0484bc77b3699b4f1b`  
		Last Modified: Tue, 24 Feb 2026 19:12:40 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e508d819e976b802ee70836afedd87fd8bbdb5e7ca7a787b6e0e7f77eb28f057`  
		Last Modified: Tue, 24 Feb 2026 19:12:41 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-trixie` - unknown; unknown

```console
$ docker pull php@sha256:ab15e868b36fc08c83e1c2545175e10cd15543afb6dc58c1554a32eae02e8da0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6826351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb991ea9c50218b9b75a0ff95907152bb587c48bd964dd5e8ef9cc9159a969a2`

```dockerfile
```

-	Layers:
	-	`sha256:755020636e44a8cb04f711750b6f91f832b09091c122df7958298b43e4f7e6e4`  
		Last Modified: Tue, 24 Feb 2026 19:12:38 GMT  
		Size: 6.8 MB (6782974 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54237c65d0c0fc1109426772c0261af643dede5389a5875960f1cdd265f9643e`  
		Last Modified: Tue, 24 Feb 2026 19:12:38 GMT  
		Size: 43.4 KB (43377 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-trixie` - linux; 386

```console
$ docker pull php@sha256:5ce0a10ae0b21ebfcb10b8c3cc89ce44ea98c09b71d76d63249bce4bd1140ea2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.2 MB (189203124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a77b482addce66d13d03485f1f093f51aac31b1ff83305e5320597b964527a4`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 18:59:37 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 24 Feb 2026 18:59:57 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 24 Feb 2026 18:59:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 18:59:57 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 24 Feb 2026 18:59:57 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 24 Feb 2026 18:59:57 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 24 Feb 2026 18:59:57 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 24 Feb 2026 18:59:57 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 24 Feb 2026 18:59:57 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Tue, 24 Feb 2026 18:59:57 GMT
ENV PHP_VERSION=8.5.3
# Tue, 24 Feb 2026 18:59:57 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.3.tar.xz.asc
# Tue, 24 Feb 2026 18:59:57 GMT
ENV PHP_SHA256=ce65725b8af07356b69a6046d21487040b11f2acfde786de38b2bfb712c36eb9
# Tue, 24 Feb 2026 19:00:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 24 Feb 2026 19:00:08 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:03:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 24 Feb 2026 19:03:21 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:03:22 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 24 Feb 2026 19:03:22 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 24 Feb 2026 19:03:22 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:f4e0b944ee1e7e50bdfbfa77bda370b6eccee7d698a7adca78c38f5ca0767ca5`  
		Last Modified: Tue, 24 Feb 2026 18:43:18 GMT  
		Size: 31.3 MB (31293918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4918b757f22e434e55dc0a5fdacad5cf252e1bf7e2ebcb92c8c34bbfc81840cf`  
		Last Modified: Tue, 24 Feb 2026 19:03:41 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38663399a9f40e01ec0510ada0f49762fcd4ced7f6ac6dd665c88b3ac95d6c18`  
		Last Modified: Tue, 24 Feb 2026 19:03:45 GMT  
		Size: 116.1 MB (116145327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2264971e254c1de8964218e239372ad999c5a2201f15569600cb4e9b6a5dff92`  
		Last Modified: Tue, 24 Feb 2026 19:03:41 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:214203af3e259089f9ae097aa7856dea5874643310ffdf8da2724c3f11b9231f`  
		Last Modified: Tue, 24 Feb 2026 19:03:42 GMT  
		Size: 14.5 MB (14479869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34d22957ffc62447bc9c8d71342f7df0569ee25f704a8ef709ca32075ffeaf5f`  
		Last Modified: Tue, 24 Feb 2026 19:03:42 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94d1c6992dc80d80616e8898c130374929d3038ed4db524ec4ee0cc9d02b36de`  
		Last Modified: Tue, 24 Feb 2026 19:03:44 GMT  
		Size: 27.3 MB (27280375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e124e97bb67d49f649320738689dc2b1eace209bc4e271d5d7e2d5fec84d5b3e`  
		Last Modified: Tue, 24 Feb 2026 19:03:44 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58e4701db5112e374740c3bd93cc0cbbcbb7d1bd301bee8bb07a6947f883de33`  
		Last Modified: Tue, 24 Feb 2026 19:03:44 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-trixie` - unknown; unknown

```console
$ docker pull php@sha256:bb1eaed425383531cc594df313a21413dc1afd509e8764f2d0ace597db61de54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6702341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36a25910b54a8e7b3eced9dcb31fbbff7162671f05cfd5aa95974879a1d9e4c5`

```dockerfile
```

-	Layers:
	-	`sha256:3252adf676ecad6bc366a6f1544c730c800f7320d54e530af9e415488178f4a2`  
		Last Modified: Tue, 24 Feb 2026 19:03:42 GMT  
		Size: 6.7 MB (6659389 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d01e002598b6bf732bb01b4b13d9a3184ce4d030ec15842f5d9d420f7cae48f6`  
		Last Modified: Tue, 24 Feb 2026 19:03:41 GMT  
		Size: 43.0 KB (42952 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-trixie` - linux; ppc64le

```console
$ docker pull php@sha256:08ad9f385da104b8263c69e214101a5ad6d82fc95cfe2341833d665198f02d5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.5 MB (184484088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2899259b4b5cd22d98dbef7a337388d8c154d122414db6c197b47516ca126e54`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:32:43 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 24 Feb 2026 19:33:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 24 Feb 2026 19:33:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 19:33:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 24 Feb 2026 19:33:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 24 Feb 2026 19:33:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 24 Feb 2026 19:33:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 24 Feb 2026 19:33:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 24 Feb 2026 19:33:28 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Tue, 24 Feb 2026 19:33:28 GMT
ENV PHP_VERSION=8.5.3
# Tue, 24 Feb 2026 19:33:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.3.tar.xz.asc
# Tue, 24 Feb 2026 19:33:28 GMT
ENV PHP_SHA256=ce65725b8af07356b69a6046d21487040b11f2acfde786de38b2bfb712c36eb9
# Tue, 24 Feb 2026 19:34:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 24 Feb 2026 19:34:06 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:38:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 24 Feb 2026 19:38:31 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:38:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 24 Feb 2026 19:38:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 24 Feb 2026 19:38:32 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:91416f8238d93c33a42d4030b8a24944e7f5b4b808e36e206f1bf078f8543c0d`  
		Last Modified: Tue, 24 Feb 2026 18:45:10 GMT  
		Size: 33.6 MB (33600216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b7690cd9f98d511ab47bad6b0f57131948908338ab7adc991d55c865326cac8`  
		Last Modified: Tue, 24 Feb 2026 19:39:18 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ae9f58f13e9d918afe833361b4c7d9fe0b3caf579a1a946767b97fa1d9806bd`  
		Last Modified: Tue, 24 Feb 2026 19:39:22 GMT  
		Size: 109.6 MB (109598488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a71f0a668b3964403df849cfd4e69c59e0bab46a4a7ab6507b543c932233ac99`  
		Last Modified: Tue, 24 Feb 2026 19:39:18 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c95f45ee73e8518fd45ef3980267f35d28f3577d80da458b7f62451907387c75`  
		Last Modified: Tue, 24 Feb 2026 19:39:19 GMT  
		Size: 14.5 MB (14480058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b88f8c3184f1e0508078b8b7c19f08dcebc542baccd0eb2feb3f2b807ebe8042`  
		Last Modified: Tue, 24 Feb 2026 19:39:19 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bb0922fdee4ab3cbd086f32bc60597033281a3c84af3f3d8b3f53c73545ed82`  
		Last Modified: Tue, 24 Feb 2026 19:39:21 GMT  
		Size: 26.8 MB (26801686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:435cf298dcea7c784f2c57d3065b0342d9d6ce4e882c2a0de461ee2d16f6c683`  
		Last Modified: Tue, 24 Feb 2026 19:39:21 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6265909d1ef87a41466529eec3b1369ca9a0c2eed2cfc3ba5e78368b9f9d7a84`  
		Last Modified: Tue, 24 Feb 2026 19:39:21 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-trixie` - unknown; unknown

```console
$ docker pull php@sha256:c700138e5ec0d6e133c7b89b5df691396196122e5bc22e3f717558af49bc56fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6728454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4786b5c9c1f722d52a7b37e368ad311f95528c73bd1debd4e80fc4c1e5ff9976`

```dockerfile
```

-	Layers:
	-	`sha256:31e65e808dc36b9b6262f265cb3a857b92343d02d66a21f084bffffc9dc7601a`  
		Last Modified: Tue, 24 Feb 2026 19:39:19 GMT  
		Size: 6.7 MB (6685273 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbdf36e05926f3ea6c78f958c7baaa96f574ada9245ee0facf88738470c0d8ee`  
		Last Modified: Tue, 24 Feb 2026 19:39:18 GMT  
		Size: 43.2 KB (43181 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-trixie` - linux; riscv64

```console
$ docker pull php@sha256:6cf2e20cc4adac1174afb296833e7742b2db21928850462aabc43d6ee14353a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.1 MB (214081811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b53a154d8d21088872a6b8d6fa3bdb3682b02d3f2e1d0d06002f5f1772cb70a1`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

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
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 03 Feb 2026 17:10:42 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 03 Feb 2026 17:10:42 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 03 Feb 2026 17:10:42 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Tue, 03 Feb 2026 17:10:42 GMT
ENV PHP_VERSION=8.5.3
# Tue, 03 Feb 2026 17:10:42 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.3.tar.xz.asc
# Tue, 03 Feb 2026 17:10:42 GMT
ENV PHP_SHA256=ce65725b8af07356b69a6046d21487040b11f2acfde786de38b2bfb712c36eb9
# Fri, 13 Feb 2026 19:03:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 13 Feb 2026 19:03:34 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 14 Feb 2026 21:07:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 14 Feb 2026 21:07:16 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 14 Feb 2026 21:07:17 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 14 Feb 2026 21:07:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 14 Feb 2026 21:07:17 GMT
CMD ["php" "-a"]
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
	-	`sha256:51dcb612d917444aa8c7a2df33b1f02a4eb42f6c61e3d498acac19ab380ce6ec`  
		Last Modified: Fri, 13 Feb 2026 21:08:34 GMT  
		Size: 14.5 MB (14495399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc9ede79e4936d9566d1602fd71cf8b34cb5ef329508db8c5b3e9c2fc4336036`  
		Last Modified: Fri, 13 Feb 2026 21:08:29 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05a580bfd32f376ab669c718f2d010d48cea7b85ea20d8b7f9d19101a6bd7185`  
		Last Modified: Sat, 14 Feb 2026 21:10:40 GMT  
		Size: 24.7 MB (24727795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67aca8963ee79db4e22f96adee3a45b2a3c38ca709a8901be540b0358bd4f551`  
		Last Modified: Sat, 14 Feb 2026 21:10:35 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:175eca044604ca114452d548251e826ca441b4fe57109de0e1147e3a82d03e98`  
		Last Modified: Sat, 14 Feb 2026 21:10:35 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-trixie` - unknown; unknown

```console
$ docker pull php@sha256:195b182ddd77ab99ee2d10c6afb5ecdde40817f4f83c0b965490eb87b5fbf88e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6800543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:655638d7c99beccc64999e97825a2308dfefca17e71fd325a84fc5cad79d73b2`

```dockerfile
```

-	Layers:
	-	`sha256:59ae08b7d46fb4874a016a573c11c003e626d8a4d66a51ba2a1af48b217b0efa`  
		Last Modified: Sat, 14 Feb 2026 21:10:37 GMT  
		Size: 6.8 MB (6757362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:446015aee09ae11387ed0f237913915291457bed814cc15ced9295d8f27b9891`  
		Last Modified: Sat, 14 Feb 2026 21:10:35 GMT  
		Size: 43.2 KB (43181 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-trixie` - linux; s390x

```console
$ docker pull php@sha256:00669769ede47bc0bf67f4eb2e34a42d0a0d9d2c28fe4a816d5b4bfffce2a367
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.2 MB (162215997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:170dd5b6deba9715aa919ab6801857f9e56c8d667fa4ce8328e5f2aa9d179944`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:05:43 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 24 Feb 2026 19:06:42 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 24 Feb 2026 19:06:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 19:06:42 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 24 Feb 2026 19:06:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 24 Feb 2026 19:06:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 24 Feb 2026 19:06:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 24 Feb 2026 19:06:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 24 Feb 2026 19:06:43 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Tue, 24 Feb 2026 19:06:43 GMT
ENV PHP_VERSION=8.5.3
# Tue, 24 Feb 2026 19:06:43 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.3.tar.xz.asc
# Tue, 24 Feb 2026 19:06:43 GMT
ENV PHP_SHA256=ce65725b8af07356b69a6046d21487040b11f2acfde786de38b2bfb712c36eb9
# Tue, 24 Feb 2026 19:07:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 24 Feb 2026 19:07:54 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:12:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 24 Feb 2026 19:12:48 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:12:49 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 24 Feb 2026 19:12:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 24 Feb 2026 19:12:49 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:b50f587e37cdad2c774c5137974987f2b5aca2ef491f293c135b60e1e43e0135`  
		Last Modified: Tue, 24 Feb 2026 18:43:50 GMT  
		Size: 29.8 MB (29838179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3739313275215d8af3ccec1798ad7d24991d08b822a789bbe7cc6ac1166dc3`  
		Last Modified: Tue, 24 Feb 2026 19:13:24 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d70c79f342449ad2e0636a0d744541e20b01b41c213ebb68f7909c753a321398`  
		Last Modified: Tue, 24 Feb 2026 19:13:26 GMT  
		Size: 92.6 MB (92572978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de26d615071822eaa28f215073d26b5aafbb3133c7cc98a021cb18e6d33d3038`  
		Last Modified: Tue, 24 Feb 2026 19:13:24 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:645cae74c11bf13856f2c9e52b1842e940f5d46a9810a73b31ad024eb9169013`  
		Last Modified: Tue, 24 Feb 2026 19:13:25 GMT  
		Size: 14.5 MB (14479670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2d4b8b8b1e0b8a4d3d2ea1363ee5d66c6d149edfd526081fac64d0ac646e257`  
		Last Modified: Tue, 24 Feb 2026 19:13:25 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d83d6a6125dbd2cbe1c7871628cf26ed784d34409002673b9bf50ab77a8460a8`  
		Last Modified: Tue, 24 Feb 2026 19:13:26 GMT  
		Size: 25.3 MB (25321534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41ca2ef3e47b51a8555da48c930b55cd89603c34a99bb57714bc35b80adeef30`  
		Last Modified: Tue, 24 Feb 2026 19:13:26 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a13b999aaa53af8b2af43565ba2cbc34e7c9190dcae1e4291376555a357a68d5`  
		Last Modified: Tue, 24 Feb 2026 19:13:26 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-trixie` - unknown; unknown

```console
$ docker pull php@sha256:787e6b581cf9bf6ce9240aeffaf20b65ae8c0cef579c73bfe1b860127901dbf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6545872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ddaa78accdca93352e1658cb3927ef24855e21d8bf753ca969c9063b4b36b43`

```dockerfile
```

-	Layers:
	-	`sha256:f17a99d2443524316d0bfcc4e82271e8eda1c9d9ebd17c71957749c88c79217c`  
		Last Modified: Tue, 24 Feb 2026 19:13:24 GMT  
		Size: 6.5 MB (6502824 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ab32068f7fc4dbb7de6653d965a95ae0af955201d52e894b86c6c381e307209`  
		Last Modified: Tue, 24 Feb 2026 19:13:24 GMT  
		Size: 43.0 KB (43048 bytes)  
		MIME: application/vnd.in-toto+json
