## `php:8-bullseye`

```console
$ docker pull php@sha256:8f82f00c19ddac8eb1ef3dab33a52fe5f2b1ce5d392fbf28ae9490e51ccb1843
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `php:8-bullseye` - linux; amd64

```console
$ docker pull php@sha256:29f53e4478a976bbc9377ff89bcc653f69aeb9566a0f75cf04daea708f2161a9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.0 MB (169990962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19c2c8fba62f596c431732c3bd0bfb92832cbfec223c16d998382cb0ced9e684`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Thu, 07 Sep 2023 00:21:13 GMT
ADD file:cb5fcc80c057b356a31492a20c6e3a75b70ed70a663506c8e97ad730ae32a02d in / 
# Thu, 07 Sep 2023 00:21:13 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 05:40:33 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 07 Sep 2023 05:40:33 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 07 Sep 2023 05:40:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 05:40:54 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 07 Sep 2023 05:40:54 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 07 Sep 2023 05:40:54 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 07 Sep 2023 05:40:54 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 07 Sep 2023 05:40:54 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 07 Sep 2023 06:09:43 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 07 Sep 2023 06:09:43 GMT
ENV PHP_VERSION=8.2.10
# Thu, 07 Sep 2023 06:09:43 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.10.tar.xz.asc
# Thu, 07 Sep 2023 06:09:43 GMT
ENV PHP_SHA256=561dc4acd5386e47f25be76f2c8df6ae854756469159248313bcf276e282fbb3
# Thu, 07 Sep 2023 06:09:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 07 Sep 2023 06:09:55 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 07 Sep 2023 06:12:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--enable-embed 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 07 Sep 2023 06:12:57 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Thu, 07 Sep 2023 06:12:58 GMT
RUN docker-php-ext-enable sodium
# Thu, 07 Sep 2023 06:12:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 07 Sep 2023 06:12:58 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:7d97e254a0461b0a30b3f443f1daa0d620a3cc6ff4e2714cc1cfd96ace5b7a7e`  
		Last Modified: Thu, 07 Sep 2023 00:26:03 GMT  
		Size: 31.4 MB (31417503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c922bf9f92d13038a122a2bbf23132b5031bc16c2f89201710690573d5f13b9`  
		Last Modified: Thu, 07 Sep 2023 07:21:41 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f00ab166ae05f0957fbd191f2796558c3a7882f2fd27c4748452468c9230a8bc`  
		Last Modified: Thu, 07 Sep 2023 07:21:53 GMT  
		Size: 91.6 MB (91632347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77443d03e1f5d38e50de1907169309b71b0bce1263628c8d1c8c39cf6e8b0de2`  
		Last Modified: Thu, 07 Sep 2023 07:21:41 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:655055ebca634cdea18ec0af79ba45dd8d55a7bb080796cae88ef4eab3cc22fb`  
		Last Modified: Thu, 07 Sep 2023 07:24:59 GMT  
		Size: 12.4 MB (12360395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d253c6756066f75027673d085dbb7a848d2da50a6f3389b039af62407cc2ec83`  
		Last Modified: Thu, 07 Sep 2023 07:24:58 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68edde91d2520137ff41a65d3a54db6bf714a5a964fc86b179123e451032d65b`  
		Last Modified: Thu, 07 Sep 2023 07:25:03 GMT  
		Size: 34.6 MB (34577037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ea98acadbbca8b2371dd910bb8ec215ac3fb057e6e5854aa0c08605601bfaa`  
		Last Modified: Thu, 07 Sep 2023 07:24:58 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ae2d2e5ff8f394fe40e90d6f1689a35a91a7c0d4f4080ba073ece664ddd63ab`  
		Last Modified: Thu, 07 Sep 2023 07:24:58 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `php:8-bullseye` - linux; arm variant v5

```console
$ docker pull php@sha256:1d83ee5b93923c2a815ddf967d07090ffee18aef73e1b8b9b8348947c02cdc67
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.5 MB (147521561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:119e11c79fba9004a35ef6cb21a432d64be220dec7435e1089f5e5f890070632`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Thu, 07 Sep 2023 00:48:46 GMT
ADD file:fb0679e6b5c5114176b186c73a97748a7712d856da24ce6f6aad2cd210825755 in / 
# Thu, 07 Sep 2023 00:48:47 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 01:24:29 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 07 Sep 2023 01:24:29 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 07 Sep 2023 01:24:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 01:25:00 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 07 Sep 2023 01:25:00 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 07 Sep 2023 01:25:00 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 07 Sep 2023 01:25:00 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 07 Sep 2023 01:25:00 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 07 Sep 2023 01:49:03 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 07 Sep 2023 01:49:03 GMT
ENV PHP_VERSION=8.2.10
# Thu, 07 Sep 2023 01:49:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.10.tar.xz.asc
# Thu, 07 Sep 2023 01:49:03 GMT
ENV PHP_SHA256=561dc4acd5386e47f25be76f2c8df6ae854756469159248313bcf276e282fbb3
# Thu, 07 Sep 2023 01:49:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 07 Sep 2023 01:49:17 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 07 Sep 2023 01:52:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--enable-embed 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 07 Sep 2023 01:52:05 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Thu, 07 Sep 2023 01:52:05 GMT
RUN docker-php-ext-enable sodium
# Thu, 07 Sep 2023 01:52:05 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 07 Sep 2023 01:52:05 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:3c087ebb90b5f9b89ab4e03487d68bd9805afd41a68507381ba597291c3083d6`  
		Last Modified: Thu, 07 Sep 2023 00:52:19 GMT  
		Size: 28.9 MB (28919010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e05524833dd688f94528580fd5563e1acfa42c76f89354b56984caaa45904ba7`  
		Last Modified: Thu, 07 Sep 2023 02:44:14 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99e2b5e18e2238dbfb414718ccd9f3646f942fe02b64e8cc8d0e7737daf8fdb0`  
		Last Modified: Thu, 07 Sep 2023 02:44:30 GMT  
		Size: 73.7 MB (73689756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d27784d71da02f2c8d0112ace96ff509efdb2e63cb671aa413a404857ff37462`  
		Last Modified: Thu, 07 Sep 2023 02:44:14 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28b656fa74e3d219bd0f23226322ea05ba74791ab69cc11d49063cc34401cd45`  
		Last Modified: Thu, 07 Sep 2023 02:47:34 GMT  
		Size: 12.4 MB (12358725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d6ab4f412b968ac57721ef7b607a771360fb8bf35aecc98b1f7ea10dd76a92d`  
		Last Modified: Thu, 07 Sep 2023 02:47:33 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be3c8b750c102509f54220ff130af04219ecdf96d56534ae089cd770f9d1cc37`  
		Last Modified: Thu, 07 Sep 2023 02:47:39 GMT  
		Size: 32.6 MB (32550384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b49a03d8f75bb9b7fa6867e1ec72b433d8755fb52d06e2bae6a7468d9dfd77d6`  
		Last Modified: Thu, 07 Sep 2023 02:47:33 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ac7430a65c6e3a55038a2440936b9400f6a815a18ed541ef04a77e55b17203a`  
		Last Modified: Thu, 07 Sep 2023 02:47:33 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `php:8-bullseye` - linux; arm variant v7

```console
$ docker pull php@sha256:ff4a51d8ef473f0ca8e92bf3749427d9d6ad201d80d0e475aca2b369df7d4300
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.4 MB (139422939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8233d37fffc10cb436b7d7fc63a6fda96c8f5e9be45f7691ce72bb9e8bd3e6e`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Thu, 07 Sep 2023 00:58:09 GMT
ADD file:d714939aacc810de397a02461ce4b9dd85e92783aff066bd3da685e3d2d97439 in / 
# Thu, 07 Sep 2023 00:58:10 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 16:56:57 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 07 Sep 2023 16:56:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 07 Sep 2023 16:57:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 16:57:19 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 07 Sep 2023 16:57:20 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 07 Sep 2023 16:57:20 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 07 Sep 2023 16:57:20 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 07 Sep 2023 16:57:20 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 07 Sep 2023 17:37:33 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 07 Sep 2023 17:37:33 GMT
ENV PHP_VERSION=8.2.10
# Thu, 07 Sep 2023 17:37:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.10.tar.xz.asc
# Thu, 07 Sep 2023 17:37:33 GMT
ENV PHP_SHA256=561dc4acd5386e47f25be76f2c8df6ae854756469159248313bcf276e282fbb3
# Thu, 07 Sep 2023 17:37:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 07 Sep 2023 17:37:46 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 07 Sep 2023 17:40:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--enable-embed 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 07 Sep 2023 17:40:45 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Thu, 07 Sep 2023 17:40:46 GMT
RUN docker-php-ext-enable sodium
# Thu, 07 Sep 2023 17:40:46 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 07 Sep 2023 17:40:46 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:323242406c24248128abc25e113055d272350b4ac4ecd985dbabfb7061c48d49`  
		Last Modified: Thu, 07 Sep 2023 01:03:12 GMT  
		Size: 26.6 MB (26578710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33fffdcc4a13d4ceeac1d887048976e0c8e0b963234bccf4ed8739d6872fbc26`  
		Last Modified: Thu, 07 Sep 2023 18:56:39 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a6105f80283b18102b11ca11ecba091883063b2de1d8804053ee3aa0611ed7d`  
		Last Modified: Thu, 07 Sep 2023 18:56:54 GMT  
		Size: 69.3 MB (69319958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25dd2c6641bdb1d55d8161263c0be6676cde0edec82068834386a0395ba00a85`  
		Last Modified: Thu, 07 Sep 2023 18:56:39 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3db1783686fee846abaab972b360d035a80427868a3bbe8f385460c5ccef36f6`  
		Last Modified: Thu, 07 Sep 2023 19:00:26 GMT  
		Size: 12.4 MB (12358657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c8866b43d425c2236858b43150b8f13cbb6c9c52b01e7b0e70ca830fc706f67`  
		Last Modified: Thu, 07 Sep 2023 19:00:25 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9944b170a7a9f112f5a089d620464530affdf188dad897654eec6291816803dd`  
		Last Modified: Thu, 07 Sep 2023 19:00:30 GMT  
		Size: 31.2 MB (31161931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32bb8e0ec8c5a823939c86d2ad3decffc36234441b4f665612ab7d5da8d2b944`  
		Last Modified: Thu, 07 Sep 2023 19:00:25 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8f82b2ff4898e86a667fa80c77133219f7925556ed312e30ca81969dac7a597`  
		Last Modified: Thu, 07 Sep 2023 19:00:25 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `php:8-bullseye` - linux; arm64 variant v8

```console
$ docker pull php@sha256:41aaa3d265840187eb67bdc0096765f4a9a63cae9ec73e9784de96507c441fb9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.9 MB (163850977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a10e294576acf95179aac3ece9ce710bd15dbbc9ce7f9a58b1d08337dbc3b1b6`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Thu, 07 Sep 2023 00:39:53 GMT
ADD file:abd1ad48ae3ebec7a6ecc8ce3016c25be2afcbaedfcb904bc89b1ce59400aef0 in / 
# Thu, 07 Sep 2023 00:39:54 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 07:27:11 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 07 Sep 2023 07:27:11 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 07 Sep 2023 07:27:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 07:27:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 07 Sep 2023 07:27:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 07 Sep 2023 07:27:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 07 Sep 2023 07:27:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 07 Sep 2023 07:27:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 07 Sep 2023 07:54:38 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 07 Sep 2023 07:54:38 GMT
ENV PHP_VERSION=8.2.10
# Thu, 07 Sep 2023 07:54:38 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.10.tar.xz.asc
# Thu, 07 Sep 2023 07:54:38 GMT
ENV PHP_SHA256=561dc4acd5386e47f25be76f2c8df6ae854756469159248313bcf276e282fbb3
# Thu, 07 Sep 2023 07:54:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 07 Sep 2023 07:54:50 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 07 Sep 2023 07:57:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--enable-embed 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 07 Sep 2023 07:57:35 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Thu, 07 Sep 2023 07:57:36 GMT
RUN docker-php-ext-enable sodium
# Thu, 07 Sep 2023 07:57:36 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 07 Sep 2023 07:57:36 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:f96ab15157043879c2ff23e0556e798eba6a6ff3d7fd5d1384de223bb9f66f1d`  
		Last Modified: Thu, 07 Sep 2023 00:43:41 GMT  
		Size: 30.1 MB (30062903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01ae993f76603852b5b3f1f8e84cea45d6ff3486fa77a24acfc0704c3952ddbd`  
		Last Modified: Thu, 07 Sep 2023 08:54:34 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a21e699f30d36a7a9059a931d9f7fd200c37c81002424635c3700f8701afdc44`  
		Last Modified: Thu, 07 Sep 2023 08:54:43 GMT  
		Size: 86.9 MB (86929166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38930988baf2370e157f8e45e1109b4a021060016029a10560cb214b454e0f6b`  
		Last Modified: Thu, 07 Sep 2023 08:54:33 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3968261e2e85a36103822711f9b09b6e0eca2e25566c7670134b4de3299a5cf`  
		Last Modified: Thu, 07 Sep 2023 08:57:37 GMT  
		Size: 12.4 MB (12359554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:089277259f086962e30b739013f67a4b5409ad3ad0e0859517c813e6f35c1b2b`  
		Last Modified: Thu, 07 Sep 2023 08:57:36 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01464ee16c22013a5b39b9dd384c2dfa7c16e309956b2dfdf8cc44560d8c8cc8`  
		Last Modified: Thu, 07 Sep 2023 08:57:40 GMT  
		Size: 34.5 MB (34495667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbcc439e958c20a85ea26716fadb191a5afeb3d5e85cf951e8eae3761402dfc5`  
		Last Modified: Thu, 07 Sep 2023 08:57:36 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5af89dd277fe3a2834ff3c28c2ed450c034aa30531cf4b6cd6a498c72e7acf8`  
		Last Modified: Thu, 07 Sep 2023 08:57:36 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `php:8-bullseye` - linux; 386

```console
$ docker pull php@sha256:abc7247a6f5035631bedbb7e24bf9b0aeb95c3a1ab231c9719adf1bde65e0b83
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.7 MB (172722642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cd910176bcaef3861c706713abd359157ebdbc9bba8ac1d7f12cf190efbbca4`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Thu, 07 Sep 2023 00:39:23 GMT
ADD file:7da3a32fda5f1208b9e4a0151bc02b156c151608c0a2c17b70ca382b4446d87f in / 
# Thu, 07 Sep 2023 00:39:24 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 06:11:25 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 07 Sep 2023 06:11:26 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 07 Sep 2023 06:11:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 06:11:52 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 07 Sep 2023 06:11:53 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 07 Sep 2023 06:11:53 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 07 Sep 2023 06:11:53 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 07 Sep 2023 06:11:53 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 07 Sep 2023 07:00:25 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 07 Sep 2023 07:00:25 GMT
ENV PHP_VERSION=8.2.10
# Thu, 07 Sep 2023 07:00:25 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.10.tar.xz.asc
# Thu, 07 Sep 2023 07:00:26 GMT
ENV PHP_SHA256=561dc4acd5386e47f25be76f2c8df6ae854756469159248313bcf276e282fbb3
# Thu, 07 Sep 2023 07:00:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 07 Sep 2023 07:00:39 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 07 Sep 2023 07:05:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--enable-embed 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 07 Sep 2023 07:05:59 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Thu, 07 Sep 2023 07:05:59 GMT
RUN docker-php-ext-enable sodium
# Thu, 07 Sep 2023 07:05:59 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 07 Sep 2023 07:05:59 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:2508d8884943a2a8ff1cc6a8264b3085b7d7637e9de43269faf016019de5c311`  
		Last Modified: Thu, 07 Sep 2023 00:44:37 GMT  
		Size: 32.4 MB (32397335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:990a959d10715871683ef763a240cea3e87181fc7f72930652983037a2f189ce`  
		Last Modified: Thu, 07 Sep 2023 08:56:32 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9e960ca8230371a52cca0550a8695a681794b3f1f7d27658a154a18ba153a9a`  
		Last Modified: Thu, 07 Sep 2023 08:56:52 GMT  
		Size: 92.7 MB (92723693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0b781f99389bc416de44a189e67239bf120bf5984622103dd66027463356d05`  
		Last Modified: Thu, 07 Sep 2023 08:56:32 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d25cde75056a2ed31a9b4bc098be6878e26d47c987a5457013e87039b8daded1`  
		Last Modified: Thu, 07 Sep 2023 09:00:11 GMT  
		Size: 12.4 MB (12359546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f5cf294a5b9bcde70bed92917d02a613489b7d3f9c16dc7a5fc09059cb186be`  
		Last Modified: Thu, 07 Sep 2023 09:00:10 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eafcf35ddad3e04d16821aea25d0b2782d0792dca31254c81408f66f60c403c`  
		Last Modified: Thu, 07 Sep 2023 09:00:18 GMT  
		Size: 35.2 MB (35238385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bda34e7d576798ae6b835ce8c6ea911d1f0f0666ae348b02180e86e042b501df`  
		Last Modified: Thu, 07 Sep 2023 09:00:10 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:540401e2f44004cc0e5cff0d395689471f3f4bc0fb5c8d24e98afeac4c61a2f4`  
		Last Modified: Thu, 07 Sep 2023 09:00:10 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `php:8-bullseye` - linux; mips64le

```console
$ docker pull php@sha256:ac4e9fe1972a384695730d2aac67f97ee8e83d33bb3d8c05d64b7479c1f7e4a4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.7 MB (146726894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:107607630f1e7da7b7347071cbaeeb235d80d5ac3a9cf925641bac23c44522f7`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Thu, 07 Sep 2023 01:10:26 GMT
ADD file:d38d449a8bdd452a8b7527e92adb18283eee35701f577c61deb4ab93f1b88721 in / 
# Thu, 07 Sep 2023 01:10:31 GMT
CMD ["bash"]
# Fri, 08 Sep 2023 09:23:57 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Fri, 08 Sep 2023 09:23:59 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 08 Sep 2023 09:25:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 08 Sep 2023 09:25:43 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 08 Sep 2023 09:25:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Fri, 08 Sep 2023 09:25:52 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 Sep 2023 09:25:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 Sep 2023 09:25:58 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 08 Sep 2023 11:29:03 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Fri, 08 Sep 2023 11:29:06 GMT
ENV PHP_VERSION=8.2.10
# Fri, 08 Sep 2023 11:29:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.10.tar.xz.asc
# Fri, 08 Sep 2023 11:29:13 GMT
ENV PHP_SHA256=561dc4acd5386e47f25be76f2c8df6ae854756469159248313bcf276e282fbb3
# Fri, 08 Sep 2023 11:30:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 08 Sep 2023 11:30:09 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 08 Sep 2023 11:43:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--enable-embed 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 08 Sep 2023 11:43:10 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Fri, 08 Sep 2023 11:43:16 GMT
RUN docker-php-ext-enable sodium
# Fri, 08 Sep 2023 11:43:20 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 Sep 2023 11:43:23 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:daedb7bf89cfe84a87bcfe1ba162d42f6ff21c2cb822f6199737968dee1ec769`  
		Last Modified: Thu, 07 Sep 2023 01:21:41 GMT  
		Size: 29.6 MB (29634539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bbe4718f2da8c6ce0266badbab21443bed91e354ee8fa91de370deb0677ec8f`  
		Last Modified: Fri, 08 Sep 2023 15:29:48 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f1fd3a403ecc8d0754f4914b820365ca52842496e4ce92af5742937016975b8`  
		Last Modified: Fri, 08 Sep 2023 15:30:41 GMT  
		Size: 71.8 MB (71811362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10487028beeff3cd8f78aa8972781834a0d3f644670243ebafa9199fe6fec80f`  
		Last Modified: Fri, 08 Sep 2023 15:29:48 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:834f254e1e19793891e0298df54429c98f56888d2ee048b8dfcfd19fedaa973b`  
		Last Modified: Fri, 08 Sep 2023 15:35:30 GMT  
		Size: 12.1 MB (12142612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f878c342d3843c0b6a2279f22298150ec4e744f6803666ad4788b6bec7ce617`  
		Last Modified: Fri, 08 Sep 2023 15:35:27 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4af2cfb12dc6630c39b2417000a9f0494dfa71e171a2d3a445800c9387d8ae4e`  
		Last Modified: Fri, 08 Sep 2023 15:35:48 GMT  
		Size: 33.1 MB (33134736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3619b36cb4f46f6dcbfa9ed5d7ad234e919b187eaf71583b1b39abc2629a0519`  
		Last Modified: Fri, 08 Sep 2023 15:35:27 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be037dc9a509ce2b7a80e676eb1ddf92488e485b31482de97cff79a89602d7d0`  
		Last Modified: Fri, 08 Sep 2023 15:35:27 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `php:8-bullseye` - linux; ppc64le

```console
$ docker pull php@sha256:2e1d091d856fb96648d8eac4aecff37f62ad494d0db9270b13452702aef4bc70
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.7 MB (170714775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0e9f73c848c3fa3e5d455197d011d3c576720fe71d93ecfdb6e009bd155af28`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Thu, 07 Sep 2023 00:18:05 GMT
ADD file:bf50998bef8a71b4723f6c17cc5c3e929d9c3b7a71b56060fea91ea0cd3502c4 in / 
# Thu, 07 Sep 2023 00:18:08 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 01:44:04 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 07 Sep 2023 01:44:04 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 07 Sep 2023 01:45:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 01:45:52 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 07 Sep 2023 01:45:53 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 07 Sep 2023 01:45:53 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 07 Sep 2023 01:45:54 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 07 Sep 2023 01:45:56 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 07 Sep 2023 02:29:19 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 07 Sep 2023 02:29:20 GMT
ENV PHP_VERSION=8.2.10
# Thu, 07 Sep 2023 02:29:20 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.10.tar.xz.asc
# Thu, 07 Sep 2023 02:29:21 GMT
ENV PHP_SHA256=561dc4acd5386e47f25be76f2c8df6ae854756469159248313bcf276e282fbb3
# Thu, 07 Sep 2023 02:29:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 07 Sep 2023 02:29:57 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 07 Sep 2023 02:34:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--enable-embed 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 07 Sep 2023 02:34:16 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Thu, 07 Sep 2023 02:34:18 GMT
RUN docker-php-ext-enable sodium
# Thu, 07 Sep 2023 02:34:18 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 07 Sep 2023 02:34:19 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:2365f3cb8bc5e18258159454852d941d92577738f79c1b5594afaec8481b47f3`  
		Last Modified: Thu, 07 Sep 2023 00:24:24 GMT  
		Size: 35.3 MB (35291070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbdd0d4f5d1c80d7e58b6bf6c8a8e61f6e8f83b9589c70c86c2a8ce1bc83fef1`  
		Last Modified: Thu, 07 Sep 2023 03:53:04 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96477cf5c43bf3803b132e85674b6222f82c3a41794a64c61d31603e7a3e1893`  
		Last Modified: Thu, 07 Sep 2023 03:53:28 GMT  
		Size: 86.6 MB (86637040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74fbe1f4f17c48c20dc1d18c3b700c2c7ae43fe9b825437ca6429153a16b849e`  
		Last Modified: Thu, 07 Sep 2023 03:53:04 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b492cefa0b2090ce73f20339908b98e023967264bee115f0ff2d8b901d5e4932`  
		Last Modified: Thu, 07 Sep 2023 03:57:08 GMT  
		Size: 12.4 MB (12360456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1282e5e356011e71bc48cf77129d2b8ba0e7872f99d130b39c19a44de70f4bdb`  
		Last Modified: Thu, 07 Sep 2023 03:57:06 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:755ec10889beae3a015e56686162d7c654f5d5e44c6c5696f48a17827e022063`  
		Last Modified: Thu, 07 Sep 2023 03:57:15 GMT  
		Size: 36.4 MB (36422525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c80d2edd3ba99936d68fcff5d9af43aab2e39c2b58076677644efad71a6da038`  
		Last Modified: Thu, 07 Sep 2023 03:57:06 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6263bc3c7ef964734140c603aa339d01876de13b665f7efc0841e7bdef8addf`  
		Last Modified: Thu, 07 Sep 2023 03:57:06 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `php:8-bullseye` - linux; s390x

```console
$ docker pull php@sha256:a7fcacadb5327b0ae41f26a0a497f724e9298806ad16e6df826bc096584c3c28
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.8 MB (146757819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:028a29fca77a60fa2e17306ac6f3cefb81b038fb57f34043e3dbf3be0e0f29a8`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Thu, 07 Sep 2023 00:44:33 GMT
ADD file:fb2f216acd6d0ecaf48e8d5dd7e3cdb5d1f51d414f2011ed318cb494f96d89ca in / 
# Thu, 07 Sep 2023 00:44:37 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 04:40:28 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 07 Sep 2023 04:40:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 07 Sep 2023 04:40:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 04:40:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 07 Sep 2023 04:40:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 07 Sep 2023 04:40:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 07 Sep 2023 04:40:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 07 Sep 2023 04:40:56 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 07 Sep 2023 05:02:59 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 07 Sep 2023 05:02:59 GMT
ENV PHP_VERSION=8.2.10
# Thu, 07 Sep 2023 05:03:00 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.10.tar.xz.asc
# Thu, 07 Sep 2023 05:03:00 GMT
ENV PHP_SHA256=561dc4acd5386e47f25be76f2c8df6ae854756469159248313bcf276e282fbb3
# Thu, 07 Sep 2023 05:03:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 07 Sep 2023 05:03:09 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 07 Sep 2023 05:05:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--enable-embed 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 07 Sep 2023 05:05:18 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Thu, 07 Sep 2023 05:05:18 GMT
RUN docker-php-ext-enable sodium
# Thu, 07 Sep 2023 05:05:18 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 07 Sep 2023 05:05:18 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:c9501ad9402d64e6c612fa1bb94f16df51188e681dc1f28c603a6109f06f22d7`  
		Last Modified: Thu, 07 Sep 2023 00:50:10 GMT  
		Size: 29.7 MB (29652801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f04459c51697fd10780b933d2fb07481994ed404f08591d0c2f2eef3f5f8bb28`  
		Last Modified: Thu, 07 Sep 2023 05:49:00 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd9615be3dc8fcd9a13fb7d453a3f43e0ad9b6f69cc442c78745cdb0a13db9ee`  
		Last Modified: Thu, 07 Sep 2023 05:49:10 GMT  
		Size: 71.6 MB (71631546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:098b6b11340bcfa589d63c880e02fa48f5657cc2f31fe3881fb5f3efc3011cf1`  
		Last Modified: Thu, 07 Sep 2023 05:49:00 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08a4327f41c38baff4b77d6175f6a8a37f753a34808292ebadd969b00511f509`  
		Last Modified: Thu, 07 Sep 2023 05:51:25 GMT  
		Size: 12.4 MB (12359127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc04b62bb4881e63ea0bdae4d3fd0f8336bd63f15b41d78d8c4c16d2df44e76`  
		Last Modified: Thu, 07 Sep 2023 05:51:25 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea8f7ec89a116dd5ae71c99bd72e4322f8d11f57f577d5721f3d2bc090c71de6`  
		Last Modified: Thu, 07 Sep 2023 05:51:30 GMT  
		Size: 33.1 MB (33110664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab9a41836f82fcd45334f31d1a776c5c2032040f0e6d08a72dd3f06b1e2e1c8c`  
		Last Modified: Thu, 07 Sep 2023 05:51:25 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48bdee7344506cb632719f4b5bba5f077916b6ebc993f26f80520969be871c0d`  
		Last Modified: Thu, 07 Sep 2023 05:51:26 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
