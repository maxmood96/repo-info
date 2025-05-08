## `php:8-cli-bullseye`

```console
$ docker pull php@sha256:23d15b7804d5924f558a48049195988b1d679c3c34368d3dc0e6ed47a34f3177
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `php:8-cli-bullseye` - linux; amd64

```console
$ docker pull php@sha256:fae5cbabbdec2265499e5f76da31db61170a88f41bb3c87036498034ded4b0cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.1 MB (175108210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:669a99ad89e40df11c226134aa27eaeb1f0da271bf133f3e953bcbef12132199`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Thu, 10 Apr 2025 21:29:12 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1745798400'
# Thu, 10 Apr 2025 21:29:12 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 10 Apr 2025 21:29:12 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 10 Apr 2025 21:29:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Apr 2025 21:29:12 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 10 Apr 2025 21:29:12 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 10 Apr 2025 21:29:12 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 10 Apr 2025 21:29:12 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 10 Apr 2025 21:29:12 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 10 Apr 2025 21:29:12 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 10 Apr 2025 21:29:12 GMT
ENV PHP_VERSION=8.4.6
# Thu, 10 Apr 2025 21:29:12 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.6.tar.xz.asc
# Thu, 10 Apr 2025 21:29:12 GMT
ENV PHP_SHA256=089b08a5efef02313483325f3bacd8c4fe311cf1e1e56749d5cc7d059e225631
# Thu, 10 Apr 2025 21:29:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 10 Apr 2025 21:29:12 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 10 Apr 2025 21:29:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 10 Apr 2025 21:29:12 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 10 Apr 2025 21:29:12 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 10 Apr 2025 21:29:12 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 10 Apr 2025 21:29:12 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:c8e1eb8ab3b017bd9e33ddec83ebdd8292c542bbd14a8d5a6cfa2edc3ad3b8eb`  
		Last Modified: Thu, 08 May 2025 17:04:40 GMT  
		Size: 30.3 MB (30254604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc345a474126d953f08c183e46d0196b0842e6caedbb8750daceb72722866dd5`  
		Last Modified: Mon, 28 Apr 2025 21:48:30 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c1f966a1335607a6f8d871ff1308c3e9eb223749a87cb0aa35127254257b1fc`  
		Last Modified: Mon, 28 Apr 2025 21:48:32 GMT  
		Size: 91.7 MB (91654002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daabef48876f979bf9f521abb33dbede07c2c615317ce16a300b4ae51490785d`  
		Last Modified: Mon, 28 Apr 2025 21:48:30 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:002f72cbade081838125c8bf82ac46784d823b8f0e1bb06f144f39099c8cee69`  
		Last Modified: Mon, 28 Apr 2025 21:48:31 GMT  
		Size: 13.7 MB (13715220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:696f2dbe8c669b6eb558003110c19f1ec9cce1ac404365176e2c62ba5e471a42`  
		Last Modified: Mon, 28 Apr 2025 21:48:31 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4df0a0f4d5b23506937883124fbfaf34323e44b205ee06ec0fad7c8d5d405f3`  
		Last Modified: Mon, 28 Apr 2025 21:48:32 GMT  
		Size: 39.5 MB (39480754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:187bd7b29a80672f125f19db33c14a1da872a5d51153f5af80213bcf068bfce3`  
		Last Modified: Mon, 28 Apr 2025 21:48:31 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaea983c59ecf3733a9bc777579155fa12496f6e67c831cc4cd54c3661b50dd2`  
		Last Modified: Mon, 28 Apr 2025 21:48:32 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-cli-bullseye` - unknown; unknown

```console
$ docker pull php@sha256:5fd1184a738713bac01e869eaa963b70863cd55d033fdfc8a48f4c83e20cb728
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6427635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39863324c8c156de52d217d0c73336fc99d641fc9e7c5327a91b179ca4ea5cc9`

```dockerfile
```

-	Layers:
	-	`sha256:161d5021abc95a7f027e80ba9f1c28b5a1bb761ff0d201030513a51865ab474a`  
		Last Modified: Mon, 28 Apr 2025 21:48:30 GMT  
		Size: 6.4 MB (6387179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4d89519b3f7bd1f35eaf3ba684c356053ac0e28edb4486a0a2afd13b5262831`  
		Last Modified: Mon, 28 Apr 2025 21:48:30 GMT  
		Size: 40.5 KB (40456 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-cli-bullseye` - linux; arm variant v7

```console
$ docker pull php@sha256:69d3cd8ff4585db4c428c1b891fa3d9f540db0137368145c88afc4b68e995d2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.2 MB (144170344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bca9bb4017a9f52fcdfadd4100ac6d36881b6b735038cb20762254f2731b1392`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Thu, 10 Apr 2025 21:29:12 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1745798400'
# Thu, 10 Apr 2025 21:29:12 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 10 Apr 2025 21:29:12 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 10 Apr 2025 21:29:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Apr 2025 21:29:12 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 10 Apr 2025 21:29:12 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 10 Apr 2025 21:29:12 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 10 Apr 2025 21:29:12 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 10 Apr 2025 21:29:12 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 10 Apr 2025 21:29:12 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 10 Apr 2025 21:29:12 GMT
ENV PHP_VERSION=8.4.6
# Thu, 10 Apr 2025 21:29:12 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.6.tar.xz.asc
# Thu, 10 Apr 2025 21:29:12 GMT
ENV PHP_SHA256=089b08a5efef02313483325f3bacd8c4fe311cf1e1e56749d5cc7d059e225631
# Thu, 10 Apr 2025 21:29:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 10 Apr 2025 21:29:12 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 10 Apr 2025 21:29:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 10 Apr 2025 21:29:12 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 10 Apr 2025 21:29:12 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 10 Apr 2025 21:29:12 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 10 Apr 2025 21:29:12 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:93c17983cb6e26d53fe6219e705b968f8a22ae1b4cb559618bdff5ba501ae39d`  
		Last Modified: Thu, 08 May 2025 18:14:26 GMT  
		Size: 25.5 MB (25542427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc0f5fed3526aa9a655f9051583860faef7fcc89d2b8dd45cbb36330f794b823`  
		Last Modified: Mon, 28 Apr 2025 22:53:21 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:234cc059c4c04843743476aea79a8338e98813c033c7a8a6d11a05b306c529af`  
		Last Modified: Mon, 28 Apr 2025 22:53:24 GMT  
		Size: 69.3 MB (69324676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed313b30099a075eb05bf4a036c81061e7355fa5dbb96437932389a84592afc2`  
		Last Modified: Mon, 28 Apr 2025 22:53:21 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54482ce932d981a15fd606c847519f56ab36ebab2ef60f76fd2a5e8b453fee37`  
		Last Modified: Mon, 28 Apr 2025 23:22:58 GMT  
		Size: 13.7 MB (13713820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2a442c44ed14ce5e415b40acc19e3738b9e112f90aa9e5d63e2e9552c55e89a`  
		Last Modified: Mon, 28 Apr 2025 23:22:57 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87a62a5b7c8206be60f73a9a3d4b0de36111eaf2125de48dc76fcf615bc57fb1`  
		Last Modified: Mon, 28 Apr 2025 23:22:58 GMT  
		Size: 35.6 MB (35585796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5bdebda0ebc5b0203927bb235557da4f379e5f77d05794558114ed71a4b25f8`  
		Last Modified: Mon, 28 Apr 2025 23:22:57 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:542e4a9ed06b4eb380ca33cc170f87873a908767b1bf667de1334221b3fd9a68`  
		Last Modified: Mon, 28 Apr 2025 23:22:58 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-cli-bullseye` - unknown; unknown

```console
$ docker pull php@sha256:e2e3317f8eff7273d24e97a13b70d7eaa2a8e188fc8e8d5cbcd0cde43a15876c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6236654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1c31e8c546984e136b192900a25b243d3ff7d69c7a7fd1600ddaa2cb8790ca2`

```dockerfile
```

-	Layers:
	-	`sha256:1fab83918b938359f6fa0bfee4ff0110b7ab10875b480a667c893dcc7f4b7e10`  
		Last Modified: Mon, 28 Apr 2025 23:22:57 GMT  
		Size: 6.2 MB (6196026 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d12d9fd577aed08bda7a5fcd3b37efaa13b94f13895d8fb6a82b011fb68866c6`  
		Last Modified: Mon, 28 Apr 2025 23:22:57 GMT  
		Size: 40.6 KB (40628 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-cli-bullseye` - linux; arm64 variant v8

```console
$ docker pull php@sha256:57b1469d23baf68ee01e72489f1e5be4e9f0c3a663e05bad12302ab94a788f89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.4 MB (168410770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c1ad02fe6ccaab45bf2dbc0b3821ac5363d2263b4d8c3e9e180bbbbf3fbfa58`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Thu, 10 Apr 2025 21:29:12 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1745798400'
# Thu, 10 Apr 2025 21:29:12 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 10 Apr 2025 21:29:12 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 10 Apr 2025 21:29:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Apr 2025 21:29:12 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 10 Apr 2025 21:29:12 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 10 Apr 2025 21:29:12 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 10 Apr 2025 21:29:12 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 10 Apr 2025 21:29:12 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 10 Apr 2025 21:29:12 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 10 Apr 2025 21:29:12 GMT
ENV PHP_VERSION=8.4.6
# Thu, 10 Apr 2025 21:29:12 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.6.tar.xz.asc
# Thu, 10 Apr 2025 21:29:12 GMT
ENV PHP_SHA256=089b08a5efef02313483325f3bacd8c4fe311cf1e1e56749d5cc7d059e225631
# Thu, 10 Apr 2025 21:29:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 10 Apr 2025 21:29:12 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 10 Apr 2025 21:29:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 10 Apr 2025 21:29:12 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 10 Apr 2025 21:29:12 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 10 Apr 2025 21:29:12 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 10 Apr 2025 21:29:12 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:5d3a81360c5bb9281a4f735a1468429a1898f1a4fc24a2581dde4cf28ace4488`  
		Last Modified: Thu, 08 May 2025 17:04:53 GMT  
		Size: 28.7 MB (28744645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e399040856549dc4a226a08faad5fb428e9430859d56acfe05462ca8444750a`  
		Last Modified: Thu, 08 May 2025 17:04:47 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f72cf290eaa9cbf7926f0fecd941a3049b3b2eb55cee9a84dc7759b3868b4647`  
		Last Modified: Thu, 08 May 2025 17:08:52 GMT  
		Size: 86.9 MB (86940643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d8132c544db419467815cf232bcf11c55005c5a76d14b74d0946ee2deb8fc75`  
		Last Modified: Thu, 08 May 2025 17:04:48 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c18ffbcb589299eebdb423bdaac27e6b03de4a764af29a765316584072826db4`  
		Last Modified: Mon, 28 Apr 2025 23:22:40 GMT  
		Size: 13.7 MB (13714637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaccea43932988c145ce7679a0848cd000d917b2f80e67cf54a94642e496576d`  
		Last Modified: Mon, 28 Apr 2025 23:22:39 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a48b25de9b7810a0d3595bbd41aa225e4109efb0a8127bf481f5e9f06c8c5c`  
		Last Modified: Mon, 28 Apr 2025 23:22:41 GMT  
		Size: 39.0 MB (39007215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c133741e214e0f9d0a672dfcd2f6e966019634caec33d32271c70e968bce4a9`  
		Last Modified: Mon, 28 Apr 2025 23:22:39 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f88dcc459a915226668077d35ab12668caaaeb21a8062ebc966e6f6902f8103`  
		Last Modified: Mon, 28 Apr 2025 23:22:41 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-cli-bullseye` - unknown; unknown

```console
$ docker pull php@sha256:3f38c49b27549f694f1a92bbb5440a7183dbe57a41fbadf49a728fed09dec55c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6430679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ddbd7490e20e30a5ec6acf331fb2f4c0dc88b495aea139ad36d9b12e5925445`

```dockerfile
```

-	Layers:
	-	`sha256:216362669a18673dc3bb138e0f5dda7ee9bcd6b59010e90a7587a8ead6c27fbc`  
		Last Modified: Mon, 28 Apr 2025 23:22:40 GMT  
		Size: 6.4 MB (6389996 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:828d42ad688c93103ea746875c0225449908536c307a23607241340b6047646c`  
		Last Modified: Mon, 28 Apr 2025 23:22:39 GMT  
		Size: 40.7 KB (40683 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-cli-bullseye` - linux; 386

```console
$ docker pull php@sha256:786ded23e15ad2033ac3fbd866fb86d9d2c097b1f48f2343d0e1aa85a36282fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.8 MB (177825602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2811196475a842158119c8ebc0d732c556e511db60cfb9d1689dfccbc5d6f3f`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Thu, 10 Apr 2025 21:29:12 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1745798400'
# Thu, 10 Apr 2025 21:29:12 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 10 Apr 2025 21:29:12 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 10 Apr 2025 21:29:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Apr 2025 21:29:12 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 10 Apr 2025 21:29:12 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 10 Apr 2025 21:29:12 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 10 Apr 2025 21:29:12 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 10 Apr 2025 21:29:12 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 10 Apr 2025 21:29:12 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 10 Apr 2025 21:29:12 GMT
ENV PHP_VERSION=8.4.6
# Thu, 10 Apr 2025 21:29:12 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.6.tar.xz.asc
# Thu, 10 Apr 2025 21:29:12 GMT
ENV PHP_SHA256=089b08a5efef02313483325f3bacd8c4fe311cf1e1e56749d5cc7d059e225631
# Thu, 10 Apr 2025 21:29:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 10 Apr 2025 21:29:12 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 10 Apr 2025 21:29:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 10 Apr 2025 21:29:12 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 10 Apr 2025 21:29:12 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 10 Apr 2025 21:29:12 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 10 Apr 2025 21:29:12 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:73bb1b80ecf1f8784ad6f92a35120b6e2306657fc7e8cbaedca1f45900f3d746`  
		Last Modified: Thu, 08 May 2025 17:35:43 GMT  
		Size: 31.2 MB (31187893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6003fec73b08086b51430a6de83dc65f281e5e0c0f6ebc7d60cf710a07ca77c2`  
		Last Modified: Mon, 28 Apr 2025 21:48:18 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67f2d33432949481aa0e0da055efad274864f04cf6dc8bdde3d374b2cf3114bf`  
		Last Modified: Mon, 28 Apr 2025 21:48:22 GMT  
		Size: 92.7 MB (92724537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92564d719deaca7601d14985bf20285fa2f97baa7056af93f2d0eee93f9930a2`  
		Last Modified: Mon, 28 Apr 2025 21:48:18 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a6c11c72f95678fdb45f4c369b76c37b73bc6cf0e4d94633ccb1b25a1d5e518`  
		Last Modified: Mon, 28 Apr 2025 21:48:19 GMT  
		Size: 13.7 MB (13714545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b6070a5ecda746956ac24b59740cd81b918124b1ffab6a4d5c3bb04f88811a2`  
		Last Modified: Mon, 28 Apr 2025 21:48:19 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3db662974effc10d5bbdd4c3c92c85d2aae7ae5c90644708f5cb8be31db05dd`  
		Last Modified: Mon, 28 Apr 2025 21:48:21 GMT  
		Size: 40.2 MB (40194995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:021489543d7ce8f114d2380131cc12ed740bb97a6b1a5936a21496560099875d`  
		Last Modified: Mon, 28 Apr 2025 21:48:20 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b71dc78198f4abd78de57f1362938c6949e2c8d8508ff979a5b910c17ad7775`  
		Last Modified: Mon, 28 Apr 2025 21:48:21 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-cli-bullseye` - unknown; unknown

```console
$ docker pull php@sha256:79ff68c2899dcba7869d36bf1d7b52e3794a2257cddbbcbc435f58a3982564a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6418225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49840a9ca7016ba997a0fac962965d1d4ff4ef54437d8a1b4372a07b639eaa4b`

```dockerfile
```

-	Layers:
	-	`sha256:c0071ac2d1655726687529f26292a69cad39b1c4da6edfa86584e66ff2ac296c`  
		Last Modified: Mon, 28 Apr 2025 21:48:21 GMT  
		Size: 6.4 MB (6377831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fcac877696019d9ffb04e841e058ffed6d283bdf4a256a3a54c324b344a0c8b`  
		Last Modified: Mon, 28 Apr 2025 21:48:18 GMT  
		Size: 40.4 KB (40394 bytes)  
		MIME: application/vnd.in-toto+json
