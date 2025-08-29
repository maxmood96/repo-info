## `php:8-trixie`

```console
$ docker pull php@sha256:24a6d741b50242e8a9bd8eb14345790e5266eb8314c528a254ce8c014e961e9d
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
$ docker pull php@sha256:9af82245aa65f174765441067c01f8d5ed0b6caf0f06b59b9426e04e9d19a0cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.3 MB (186292742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:797fe7681a3e268f80414fc2fe7149a29c6c89fa1acf11a9fd5217626e4b7bd6`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
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
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
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
	-	`sha256:396b1da7636e2dcd10565cb4f2f952cbb4a8a38b58d3b86a2cacb172fb70117c`  
		Last Modified: Tue, 12 Aug 2025 20:45:08 GMT  
		Size: 29.8 MB (29773285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:331172d464fdd00eb58e7d97d1ba28aa3a139db9d1a70713b05c96b920ebd8f4`  
		Last Modified: Thu, 28 Aug 2025 18:18:34 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f889f3c8e6d06d85de567e34f4134f754a69a971313b5f7c3784555e5e35bd70`  
		Last Modified: Thu, 28 Aug 2025 18:18:47 GMT  
		Size: 117.8 MB (117833912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a04401585b760bf7305221ceb5905ef3155c9986cc123e6a2f8f7d80663de395`  
		Last Modified: Thu, 28 Aug 2025 18:18:34 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d30f5ecc1fd38debdedea58da1d86bfcca8fd1a34c676be4a1f7d2fb8bb7cb8`  
		Last Modified: Thu, 28 Aug 2025 18:18:38 GMT  
		Size: 13.8 MB (13783904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbe9520fe18b45d490bf9c2844012c83370fd717f3624a73e06c2c026e0615fc`  
		Last Modified: Thu, 28 Aug 2025 18:18:34 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc6f0bd01def78192343d06653f9cb50b4bfb3eb92be8395963a49c00a3ef4c5`  
		Last Modified: Thu, 28 Aug 2025 18:18:39 GMT  
		Size: 24.9 MB (24897749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0873ad17a6f3705391f10157f69d6e9c435194e6fa54008cc00349be1a17f713`  
		Last Modified: Thu, 28 Aug 2025 18:18:34 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3a8df84e2a9a2b9f27649e5a9653da134cc7716cbfefd0a41b17c2cc73876c1`  
		Last Modified: Thu, 28 Aug 2025 18:18:35 GMT  
		Size: 253.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:702fe5e289a3458164fcf5dd94771e37d2e721dd1e379f0d52880cc6c54aebdb`  
		Last Modified: Thu, 28 Aug 2025 18:18:35 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-trixie` - unknown; unknown

```console
$ docker pull php@sha256:c856a9559744955493527bac7376ade4e8f6f54e8bbb5977c4f4e97df691c1f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6731496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e131502dd503dad9ba67af0425c590f7de253181d9011c82d5988ed74d829c3`

```dockerfile
```

-	Layers:
	-	`sha256:1a86ab727385f911903d5e058f3a7c36b774a6c82f90506d55e851041a6f542d`  
		Last Modified: Thu, 28 Aug 2025 19:54:42 GMT  
		Size: 6.7 MB (6685698 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:834f307a20f6c992954b93dda87b3f0c042d694da53111dea543fe529d48a060`  
		Last Modified: Thu, 28 Aug 2025 19:54:43 GMT  
		Size: 45.8 KB (45798 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-trixie` - linux; arm variant v5

```console
$ docker pull php@sha256:26ac3f516eb937f036fb3738d745902f6e0c094c534293edbe704963b3639632
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.3 MB (159278561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:458ee9b45953a3786d2ec06e4b63dd77cb3f66c2bd1d5eaffade4c76fbb3398b`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1754870400'
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
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
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
	-	`sha256:498399880872f14c562c46bd2a1ef4cfcf3c2a1453514ff0d0f6b7d89f8010dd`  
		Last Modified: Tue, 12 Aug 2025 22:02:01 GMT  
		Size: 27.9 MB (27941706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b826fc1a1d535eacc028e3d956ad4684d2277457bc010244dfb267e133817510`  
		Last Modified: Wed, 13 Aug 2025 02:04:17 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e5554cad66c2c0be3db0dee9e2828bb1216178113d28498a470e272f7c87a2e`  
		Last Modified: Wed, 13 Aug 2025 04:31:51 GMT  
		Size: 94.9 MB (94871877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bad6001493531fd836717f5de4d6b19cb18c7fe4e2c9d0cbbcb80e66609bd4b`  
		Last Modified: Wed, 13 Aug 2025 02:04:23 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b33dd804fa5154b93369fb189d40a92e59aff890da1834393a2979a3e841797`  
		Last Modified: Thu, 28 Aug 2025 18:57:27 GMT  
		Size: 13.8 MB (13794465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfa48cdf26a8f14cbc1099d813fdd248f290edcec023ce9542a7b515f1f01ff7`  
		Last Modified: Thu, 28 Aug 2025 18:41:53 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebc9c450db4471189bc8ba70e9b45271b5ba391133dae685185e0d69dde5b33a`  
		Last Modified: Thu, 28 Aug 2025 18:57:36 GMT  
		Size: 22.7 MB (22666619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f3c1841c6f3063f837d29f078d60c317f26944fafdae36fc013bfecd6edca3e`  
		Last Modified: Thu, 28 Aug 2025 18:57:38 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5056d00d7382d225da8561c9dfa7d1dfa6a0c58b9ca561223cebb91b0aa34f9d`  
		Last Modified: Thu, 28 Aug 2025 18:57:40 GMT  
		Size: 253.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23e7f6c331a8dc3ab660b4dbe4d07deaea4acc064d9a10967b41900206f2601a`  
		Last Modified: Thu, 28 Aug 2025 18:57:41 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-trixie` - unknown; unknown

```console
$ docker pull php@sha256:14e0edd55049d20f8a378593195895da78fe7c2651d0b3b3762dd111dd28a492
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6531648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:507c52a886d59fe6dd32a6c22ac518324d0fab1f8364c2ec42cd531bb7ca0a65`

```dockerfile
```

-	Layers:
	-	`sha256:d6da06c58bd5dcf2d1662b57a5937219d8984f342e951d9b087e34e81ee11bf7`  
		Last Modified: Thu, 28 Aug 2025 19:54:49 GMT  
		Size: 6.5 MB (6485608 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e75b6b8c6b48239e34b36880013d99f6d8d49016e88176414e0a89727d8561d8`  
		Last Modified: Thu, 28 Aug 2025 19:54:50 GMT  
		Size: 46.0 KB (46040 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-trixie` - linux; arm variant v7

```console
$ docker pull php@sha256:12aa77cf712e621ee5a91a142bd6cd60c6fd3f37311af4e5060e3053bed7274c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.7 MB (147695383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86bd434c8ffcf95ac6522eb91af4041a05a3131fe9d7e1b5d293030bc4bee87b`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1754870400'
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
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
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
	-	`sha256:d480d07cd33d2a61cb24d871a17254661d250ae887a2db15a7e99cb67383a74e`  
		Last Modified: Tue, 12 Aug 2025 20:52:10 GMT  
		Size: 26.2 MB (26207488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f783066fe233d49b725a424d9e4e2edf03ec368e8008a7100235b31d55c72428`  
		Last Modified: Wed, 13 Aug 2025 03:03:11 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:def7928390388cc2020246549215f695478752f6ae67568af1344eee2f6088ce`  
		Last Modified: Wed, 13 Aug 2025 03:03:28 GMT  
		Size: 86.2 MB (86243176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5decd14e90655d8988225e174f3bef3fbd8abee342388203104f64e9516432f7`  
		Last Modified: Wed, 13 Aug 2025 03:03:11 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01239ee2eb348cf2a3bf163f4e891f10c1e70b345cb14dc2af423bef3867870b`  
		Last Modified: Thu, 28 Aug 2025 19:22:21 GMT  
		Size: 13.8 MB (13794579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a90905884b94473ddab24a444ac06045a6590622499b7e1ec6455b4016cbffcc`  
		Last Modified: Thu, 28 Aug 2025 18:41:56 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cde4325869759a47a39d539ca5a5223a3da8fe36ae0e09cb639d99a4024908d`  
		Last Modified: Thu, 28 Aug 2025 19:22:25 GMT  
		Size: 21.4 MB (21446252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37e23eda0825630a57f097040f20a46bee50070129454b8f39abcbd5a896d4f1`  
		Last Modified: Thu, 28 Aug 2025 19:11:42 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f1151d8246605ca9bf3fb7f690dc536a609cb4a6adf2ecdafbe2693160ce3ad`  
		Last Modified: Thu, 28 Aug 2025 19:11:43 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ecc62f24de8bd8a387e38fc4a91b2252e0b3d2304228909dd99466c508bf66a`  
		Last Modified: Thu, 28 Aug 2025 19:11:43 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-trixie` - unknown; unknown

```console
$ docker pull php@sha256:2931a7fb0e53e80c8c4a0f2dde3dbd3dc96ce9c5f20215afc51be71e634115e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6535614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95337302def2aa3f26e2211d8631b1860317aa4244208360239774e70d0c24ad`

```dockerfile
```

-	Layers:
	-	`sha256:e4dc2de7e9aace4c38f20cbf816e074e6ae200505c176d3144097e9b3ccc5a45`  
		Last Modified: Thu, 28 Aug 2025 19:54:56 GMT  
		Size: 6.5 MB (6489574 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4468347ec68337c0f0ef32b87e472d608ac983e4af5abbcb933edb72fbbd4577`  
		Last Modified: Thu, 28 Aug 2025 19:54:57 GMT  
		Size: 46.0 KB (46040 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-trixie` - linux; arm64 variant v8

```console
$ docker pull php@sha256:a8bbae7649947566d187c5433fb3295f85945e13656b2f55b612f17d513e7f54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.5 MB (178469274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1b97924939abd1d54b2f56f95b55f8437e0c8fe500cccafd7df692f364bca06`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
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
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
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
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef1ee6d029e615fa2b873890f1011a42f1c5f78b2d100eaed3bc1df5bb73d212`  
		Last Modified: Thu, 14 Aug 2025 22:21:29 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a472e922e809f2164e7de33f1a04d157980da1614d66407be60d248980ca8453`  
		Last Modified: Thu, 14 Aug 2025 22:21:38 GMT  
		Size: 110.2 MB (110160334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48fe053e93cb40a6c44acd9d0ab0ee960880abe08bd106a21947710df1e0399e`  
		Last Modified: Thu, 14 Aug 2025 22:21:29 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55a0aec95b02c2860affeb48595cb4d8edb2a68b61013471982c96f17358203b`  
		Last Modified: Thu, 28 Aug 2025 18:20:07 GMT  
		Size: 13.8 MB (13796582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1692beccd566aa61a5176dbbd571323bb8bef44c4d5a5461a3e2e653040e40b0`  
		Last Modified: Thu, 28 Aug 2025 18:20:06 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eeef96374d2d762aadb364484ce968941ec1b093df55f11e385c6e975bb5a28`  
		Last Modified: Thu, 28 Aug 2025 18:20:09 GMT  
		Size: 24.4 MB (24372422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e9ec3bcc39e03c7569b83841353d061d8a853966b255c5d502692b182d85ae7`  
		Last Modified: Thu, 28 Aug 2025 18:20:06 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4763a6ec64b8866060e49a8670d4fa4c9ee99bd507bc705b218e44fbb382c979`  
		Last Modified: Thu, 28 Aug 2025 18:20:07 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fda10b7ed762b5ec6baacd14315ce126b79f7aff1203960bf43cb7038bcb4c8b`  
		Last Modified: Thu, 28 Aug 2025 18:20:07 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-trixie` - unknown; unknown

```console
$ docker pull php@sha256:aaf724a7d293e4c792df797ff396fb3021ff2da4ee8de30a39b18ad3cc4beccc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6829257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2e4cffd7a7f0e96e9818f905e411968fea33eba1dc17210a113e5d637e254af`

```dockerfile
```

-	Layers:
	-	`sha256:558c3ae520d6d02d921c904932f4109255884e4be142dc91076175c2f1c1016c`  
		Last Modified: Thu, 28 Aug 2025 19:55:04 GMT  
		Size: 6.8 MB (6783121 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a59787e77b4febc7fd623037115d613398acf9914d23e0503614616112f1c1e4`  
		Last Modified: Thu, 28 Aug 2025 19:55:05 GMT  
		Size: 46.1 KB (46136 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-trixie` - linux; 386

```console
$ docker pull php@sha256:d080eeb2a0ed39fa5aee27c9cb0d537c5d6b12f33a30f11fb71c2802e7dbdcb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.6 MB (186590515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5906e287bc26992dc718285e65f2612da4c02c327c76828bc8a86da31c80350b`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1754870400'
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
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
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
	-	`sha256:346d0c953bdbc38917a27a6f30726e5b46419d98ecaf4d2d8f201bc3b7025e57`  
		Last Modified: Tue, 12 Aug 2025 20:45:00 GMT  
		Size: 31.3 MB (31289378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:699565c0b7e200a16cc5af39fcb8c0eeb57f3076a393f16c32fe946c763a205a`  
		Last Modified: Thu, 28 Aug 2025 19:08:17 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:838fe8e85d07f9a2b6e09eb16b0ed745afefa974288b4cb7d39c345a458ceff6`  
		Last Modified: Thu, 28 Aug 2025 20:32:00 GMT  
		Size: 116.1 MB (116134644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a04401585b760bf7305221ceb5905ef3155c9986cc123e6a2f8f7d80663de395`  
		Last Modified: Thu, 28 Aug 2025 18:18:34 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93b0f63f10fef513b160cad852e089858bb2fa1e587e38fa5010a3fc3ab1a977`  
		Last Modified: Thu, 28 Aug 2025 20:32:20 GMT  
		Size: 13.8 MB (13782905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a5fad352d3c53577c2410470f64ae834e31ad36274e99f4ecbb6beb5f230b7f`  
		Last Modified: Thu, 28 Aug 2025 19:08:24 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:344b79e9dc243bf816ec4765acee7896700c7fda9f98fc750a53e7d837507e60`  
		Last Modified: Thu, 28 Aug 2025 20:32:31 GMT  
		Size: 25.4 MB (25379695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e168a555ad249d9f24de86f59cc989a72b74c96082bbc6f27a58ef66639b4a76`  
		Last Modified: Thu, 28 Aug 2025 19:08:29 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4649cbe874b166743120892cac09bc53f3bbebd9089592c7ed31bb3fbd70c548`  
		Last Modified: Thu, 28 Aug 2025 19:08:32 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca3de0b5713d0a6da33f396d05649db84d1f5c1be32db343c545773bfbf83bf`  
		Last Modified: Thu, 28 Aug 2025 19:08:35 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-trixie` - unknown; unknown

```console
$ docker pull php@sha256:0bab83d3013b9ad0a4ed5b84e3a2d4e2859a19e12250b54d6945142cc0331edd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6705229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f38bee2a8671e144bbf89aae543920f6ab487fb894c3aa57dfb7db8971dfc28d`

```dockerfile
```

-	Layers:
	-	`sha256:39ddf2e2477dd1d6b804e0cfa6b2c8e289a6870edc7422ec850ecdab9415ff03`  
		Last Modified: Thu, 28 Aug 2025 19:55:12 GMT  
		Size: 6.7 MB (6659536 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f40bcd45f7da80247776b0ba5f06b241060c35115752d4c8538581823d5cd8fd`  
		Last Modified: Thu, 28 Aug 2025 19:55:12 GMT  
		Size: 45.7 KB (45693 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-trixie` - linux; ppc64le

```console
$ docker pull php@sha256:6c8c88e53844e3c8ef718594aa9e6b6b8dc74a1294a75343e259041b823e2aba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.3 MB (183262043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e40ec7f03796ece08d2d7e5bbef06dc8b8097ec1f00fa675ec2ef9a2d73e393`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1754870400'
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
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
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
	-	`sha256:52a4daa8724e9e1632306e15fe478aa26ff0ebcb7ba924cb168e9b6738c239d5`  
		Last Modified: Wed, 13 Aug 2025 01:42:36 GMT  
		Size: 33.6 MB (33594213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebe95aaa1875d4c50c764ba29c6f95cc470f62d9ac88ad9109e0cd4505d319b5`  
		Last Modified: Wed, 13 Aug 2025 05:31:58 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e0ffef807c2273a22858b85bf52a5cbb82101766a6dfce24ba2f8e3ca25f228`  
		Last Modified: Wed, 13 Aug 2025 08:03:15 GMT  
		Size: 109.6 MB (109595127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b5e8a64ac10b73fd871320ade0ad956a6b2aeb6e2c3151d32095cad855bbccb`  
		Last Modified: Wed, 13 Aug 2025 05:32:01 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03afb458e7def5cd6bc09cbac6e138c0d5dea54f31ce8278e16fdfea67a263e5`  
		Last Modified: Thu, 28 Aug 2025 18:17:53 GMT  
		Size: 13.8 MB (13796031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cda77c7d92fefb7a8a2237a9df8a1e245fe8466b833ae549695035495fa3033`  
		Last Modified: Thu, 28 Aug 2025 18:17:42 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dfdca24522d2bc5d9529b072eee42e6c4597dee3d3a2828d39a0d3dcc5d342e`  
		Last Modified: Thu, 28 Aug 2025 18:17:44 GMT  
		Size: 26.3 MB (26272781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7110178f14ee5d475f197cd511d06bdfd6aa6e9f41aa672bca2329f585ad2d2`  
		Last Modified: Thu, 28 Aug 2025 18:17:42 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45ff3c3a6500628c068dc336cb915bcba43526042f442a24c9be10a242074013`  
		Last Modified: Thu, 28 Aug 2025 18:17:43 GMT  
		Size: 253.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cfe0f6b48887aaeb9199b78ba5c65011f6d927674e57555dbbfc4f230b2bda1`  
		Last Modified: Thu, 28 Aug 2025 18:17:43 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-trixie` - unknown; unknown

```console
$ docker pull php@sha256:38c5f2c220d9ae719c28c9b93da2f0b2eb56d8f0c20d60f0e4b9d78f03c954b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6731346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a784994a458ca42b0840e2ea6e51e89eaab941c534dd5b0920e6b4f12cf4f6b0`

```dockerfile
```

-	Layers:
	-	`sha256:827d0309253e53a13e6763c7067bde379ff5787daf3edae812ecf3b8b6af4e25`  
		Last Modified: Thu, 28 Aug 2025 19:55:19 GMT  
		Size: 6.7 MB (6685420 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cb59539d5ac54ebcc046c605f743ba951e95a8259c369765cd06f1d5e7cb95f`  
		Last Modified: Thu, 28 Aug 2025 19:55:20 GMT  
		Size: 45.9 KB (45926 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-trixie` - linux; riscv64

```console
$ docker pull php@sha256:d43a3dc655dab72d701a653ff46921e067fb138c0d9bb5a5fc0840d3e06b8c26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.0 MB (213015834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d14341d674ee04df213f8e463e7a7eb772c47671802b2aa3c1448c730a5883e4`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1754870400'
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
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
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
	-	`sha256:a37386b9234ad75f65b5aa72f3d919ff0eb3bb18978566fa959d6e357480594c`  
		Last Modified: Wed, 13 Aug 2025 04:01:43 GMT  
		Size: 28.3 MB (28271623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40e74ecc2368ed7bf14f15784d294255a507b61c121584b8889b54497f586460`  
		Last Modified: Wed, 13 Aug 2025 11:14:45 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44ba9332bf4f75d23eae5411f58fe1a55971f98de6873eba08746a8a1042d175`  
		Last Modified: Wed, 13 Aug 2025 11:43:11 GMT  
		Size: 146.6 MB (146577824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05acfa088a6e9eb3845fc5011b31ba6a62983f44944e2347f32361bf21d8f85`  
		Last Modified: Wed, 13 Aug 2025 11:14:48 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13b6f12b0240e0dbf97c8e4e7dcd68de87e0574ef0a3f23092d507469bd287a7`  
		Last Modified: Thu, 28 Aug 2025 20:15:17 GMT  
		Size: 13.8 MB (13795967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04c460ecb1c90c1e778236105aed7163700500a98352ef0a0fc0ca5883f519ff`  
		Last Modified: Thu, 28 Aug 2025 20:14:18 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a36ce695637343d1c6085adbb4af9f3c06d13ddeebb1497a38ea26b1ee85ec23`  
		Last Modified: Thu, 28 Aug 2025 20:15:21 GMT  
		Size: 24.4 MB (24366524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a97b17cac0fde926945802056b1c85eeb3dd8ca847e118ea8fb4ff2baa18fc7`  
		Last Modified: Thu, 28 Aug 2025 20:14:21 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c747c7682987ab7a250a6cc784332b791fa15afd6d3cf9419ae5d2402095b09`  
		Last Modified: Thu, 28 Aug 2025 20:14:25 GMT  
		Size: 254.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fe58409bb77170b1e2c053dfddefc299e7dd77356cdd7c649aee7542d0313d4`  
		Last Modified: Thu, 28 Aug 2025 20:14:28 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-trixie` - unknown; unknown

```console
$ docker pull php@sha256:a03a42df320535094fa4a408782178849afbd083727478eb0ed3c0ff1982f7bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6803435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4a67721eafb792dac8f4b0d6ca18c289e86a2534e0eb6efab6b1ebcfe65bfc4`

```dockerfile
```

-	Layers:
	-	`sha256:d56230e97101f026eec04a9196f58f2edf916f5306f26f9bfe089cae1c370427`  
		Last Modified: Thu, 28 Aug 2025 20:09:16 GMT  
		Size: 6.8 MB (6757509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:166d786869e935b999d597092fd986ae95a0452d4bfc6d21313dcd8c459358e7`  
		Last Modified: Thu, 28 Aug 2025 20:09:17 GMT  
		Size: 45.9 KB (45926 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-trixie` - linux; s390x

```console
$ docker pull php@sha256:8b3040abab854ab4aea0c7a5442c9db55d933b39e4a4f84ce35b5e8219c421d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.7 MB (161717477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7b2cf4aab9dc16fe418555a9846908fa1ed605b5f4bc1acb28f7b3b681f7242`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1754870400'
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
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
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
	-	`sha256:bfe4d60a27c9392ab729f16b50a763cda36622d744066c3cf029a072133f2907`  
		Last Modified: Tue, 12 Aug 2025 20:59:52 GMT  
		Size: 29.8 MB (29833057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2d672c8320b5c626e155e165336b2569c5c22cfbda44788e2e9dd0b175c8a1e`  
		Last Modified: Tue, 12 Aug 2025 23:44:44 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b06790e9e58c7a87421168e1b912411e592f3adbcdce2412a5541e72fa8de3f1`  
		Last Modified: Tue, 12 Aug 2025 23:44:49 GMT  
		Size: 92.6 MB (92562072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:019838dc72213baa0c7fefd5773b69a921a755553c45ef473aea40f478c95cb3`  
		Last Modified: Tue, 12 Aug 2025 23:44:45 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0315b0bbaf3f0a13ecfdbc8198ee4184822abe3736eeae59551c67ca01981bae`  
		Last Modified: Thu, 28 Aug 2025 18:40:00 GMT  
		Size: 13.8 MB (13795360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0d236682bdc44aa14a14c0c16c2ddffd676cdfada4136f07ec5aa43ea30d132`  
		Last Modified: Thu, 28 Aug 2025 18:39:59 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60d105528a7d1ad6367115f3df4925791e0bbb984a44faf83716e2cef4de4802`  
		Last Modified: Thu, 28 Aug 2025 18:40:01 GMT  
		Size: 25.5 MB (25523097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5aad2b1a3660270a82a1f0e4d19f40439f97d3c7cb929fb034e053bba973f81`  
		Last Modified: Thu, 28 Aug 2025 18:40:00 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5580d9a43e605060adad112939e9b13d69dbb9fa51a70a7fdce4ff259518d5dd`  
		Last Modified: Thu, 28 Aug 2025 18:39:59 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da507f0d145ad63d42d60230438e72f377eebbe6ed21ee0cb9ee8fa2f66210f7`  
		Last Modified: Thu, 28 Aug 2025 18:40:00 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-trixie` - unknown; unknown

```console
$ docker pull php@sha256:cc04dcbd6f24f0a38c0a924afa8636bebb9701f8eda19eaff3c482d6be15c8a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6548761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bd1c4bb1f3b51e03c22e6ef2a23ad8389f6012ce365e19a73e5a75d482ee56c`

```dockerfile
```

-	Layers:
	-	`sha256:f32cbc19858d2ca01744c00f34470a31dea798f2806a90b1a20e5a47286bd27f`  
		Last Modified: Thu, 28 Aug 2025 19:55:30 GMT  
		Size: 6.5 MB (6502971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e37607c05a5457ea3f17ea131a5e153e5ce381dd82530809aed853b183aedc8b`  
		Last Modified: Thu, 28 Aug 2025 19:55:31 GMT  
		Size: 45.8 KB (45790 bytes)  
		MIME: application/vnd.in-toto+json
