## `php:8-cli-bullseye`

```console
$ docker pull php@sha256:d026a3efa3cd0b0996211bef12cc4c46ceb552631efc93a964e89d231bcb4cd2
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
$ docker pull php@sha256:b361d41afaceb6c435e2e5b4a4fe2d05c4ff18638bf00c53527c88c248b70355
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.8 MB (174821356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21561f17cc6bbb43dd23d631a8a94bae38aa01efc0a085c35ed23e11090bcfed`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1736726400'
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 17 Jan 2025 01:46:40 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_VERSION=8.4.3
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 17 Jan 2025 01:46:40 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:89320e7119e225692d79aaeb4989a18d7f97daafdb2b3782f84a0a8de31a09de`  
		Last Modified: Tue, 14 Jan 2025 01:33:29 GMT  
		Size: 30.3 MB (30252665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc676fa2c632766b8c4a22ca782413fb99cf7d0508619b51916f3c22ef30e142`  
		Last Modified: Fri, 17 Jan 2025 17:33:09 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2462b88ec88014151b5ec3f713c0e7478122dcd33680c8e08ee7011088c50532`  
		Last Modified: Fri, 17 Jan 2025 17:33:10 GMT  
		Size: 91.4 MB (91448006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c846b73b6377d92766368bea10ba5dd71e6b5f24abd4a50d2c6d4703ce69f1ee`  
		Last Modified: Fri, 17 Jan 2025 17:33:08 GMT  
		Size: 229.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8bf1fe3d0d9f1fb692930d089b1756fbf2787f15c9bfc93b1dac5f70334fbd6`  
		Last Modified: Fri, 17 Jan 2025 17:33:09 GMT  
		Size: 13.7 MB (13674110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c7a9fc2c20d68be06dcedb7f3d378a0d95bd5535533a078db78d8a8bff97c2b`  
		Last Modified: Fri, 17 Jan 2025 17:33:09 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b740b54be10aed584c68d741f5b87c36f893ab9745f2eec295bfb6513436b1d1`  
		Last Modified: Fri, 17 Jan 2025 17:33:10 GMT  
		Size: 39.4 MB (39442935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83dc0e2da8ef857785f4ce00aae0b200e21915ce553e98e08dc9721e1e2dcc11`  
		Last Modified: Fri, 17 Jan 2025 17:33:10 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8afd8da09c0dc15299dfc4f69db14b6828fdeec040db560026ae3737d66be17d`  
		Last Modified: Fri, 17 Jan 2025 17:33:10 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-cli-bullseye` - unknown; unknown

```console
$ docker pull php@sha256:f2815327c0c5d9e70175b47d80ef8dca56374e27586cbd292dcd0465730b565f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6425653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7688c8f12c14ce923652f8ec44f69059f9cc7d03375694764007e9dfa3a11579`

```dockerfile
```

-	Layers:
	-	`sha256:3b3b114778dab8ca3c51e0b878a22aa85b2ab8325c00d2e729103a7c2c848330`  
		Last Modified: Fri, 17 Jan 2025 17:33:09 GMT  
		Size: 6.4 MB (6385197 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fc80975003de09a1f014c797e64c49b6442faad0b4a9657997ce72aee6d3ede`  
		Last Modified: Fri, 17 Jan 2025 17:33:09 GMT  
		Size: 40.5 KB (40456 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-cli-bullseye` - linux; arm variant v7

```console
$ docker pull php@sha256:b87a4d241967388560760e9e44bad81eccf0d8c54e23bfa07def8bf08e5a5286
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.9 MB (143906011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6836cbacc8c26ebea6aeecb28379913c3ca43e7fc79bd7f34ab48c811b60fbc1`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1736726400'
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 17 Jan 2025 01:46:40 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_VERSION=8.4.3
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 17 Jan 2025 01:46:40 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:61fe776d618d9b70bea09742b3fce817da0393e8911c90f01094c0a407e1f7bf`  
		Last Modified: Tue, 14 Jan 2025 01:35:53 GMT  
		Size: 25.5 MB (25533960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d93b737d9d37bd60c8605bf5c054750994a7d9bf9fcc44b376fd7249244abcf`  
		Last Modified: Tue, 14 Jan 2025 03:05:15 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69002742768de244d879a330315c30a076fb9fcc3e1b1e78748310f0f812a011`  
		Last Modified: Tue, 14 Jan 2025 03:05:18 GMT  
		Size: 69.1 MB (69119271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b30d38aa9fbc72534a04c8660b325338232f5eb41922619c41d2da02e32be09f`  
		Last Modified: Tue, 14 Jan 2025 03:05:14 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fc9330843c0d12fec597ddcea844c67e21e0ece1528ea5cbe61a322daae7626`  
		Last Modified: Fri, 17 Jan 2025 17:59:04 GMT  
		Size: 13.7 MB (13672668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c6240e3eaa77c73babdb7f05d586fd81583b9bb8f4032bc0de6b3bc72d59b37`  
		Last Modified: Fri, 17 Jan 2025 17:59:03 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f3fba11d90e09d69af7caacc3a03a0da5ef124a55c1b5c943531aa2caa39d17`  
		Last Modified: Fri, 17 Jan 2025 17:59:04 GMT  
		Size: 35.6 MB (35576478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aea6cc90cc6083f3a62bb96a40cc3e43d1d94154a43d07c1f0992ce7cb92ce62`  
		Last Modified: Fri, 17 Jan 2025 17:59:03 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a059c95c7bedf1b992311168edc6d3b6cc6024972f3880162cc812e71d129e8`  
		Last Modified: Fri, 17 Jan 2025 17:59:04 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-cli-bullseye` - unknown; unknown

```console
$ docker pull php@sha256:90f9d21b59a9f7e6259a81d82f9d52b51e28ee3e32fd7dd788b35c7495c4ff20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6234673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26e99786b4e129ed5cbf4ea72c30af84cb0fc0305a24ce256b9f559f79f92934`

```dockerfile
```

-	Layers:
	-	`sha256:f62cc12468645eac94eb0bfa6ed6b1f8d5c9f5e08b73ce0fa1a86c9b1def17e2`  
		Last Modified: Fri, 17 Jan 2025 17:59:03 GMT  
		Size: 6.2 MB (6194044 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:112303831c9758f5db87f3b1a4af7b6c8be6c49fdf49cf88df4fdbf67a3cacb3`  
		Last Modified: Fri, 17 Jan 2025 17:59:03 GMT  
		Size: 40.6 KB (40629 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-cli-bullseye` - linux; arm64 variant v8

```console
$ docker pull php@sha256:a6f18dcd6c6ce679407ef294d1348f851c3a8ea84d4e17c9aeeb1d046a7aff5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.1 MB (168106412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9eb92fb3afceac9534b5fbdb6120ca675b4ddeb34e2ecb7a4781cf0128c2524`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 17 Jan 2025 01:46:40 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_VERSION=8.4.3
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 17 Jan 2025 01:46:40 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:6a43d3167ec1fb9f3b40bf3e095c86abebf31d406e2de1d196433c26d262f72c`  
		Last Modified: Tue, 14 Jan 2025 01:36:26 GMT  
		Size: 28.7 MB (28744913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:798f4885259ede04563f6f2c30252c470e94aaf9a95576060866ba0ca177a1b8`  
		Last Modified: Tue, 14 Jan 2025 03:28:41 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f91a0cfe9d2540e4d05e8198913405c46a9a624800b104db09fb49ea98a3d13e`  
		Last Modified: Tue, 14 Jan 2025 03:28:44 GMT  
		Size: 86.7 MB (86734429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3b3d3d9ba2fe6d1d3be940377c1fbbc1ab8489811531766e34900760d284128`  
		Last Modified: Tue, 14 Jan 2025 03:28:41 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffbce83e3a463fbe56b62579fe576cb636548a454db8f478baa5257d7f8f5b32`  
		Last Modified: Fri, 17 Jan 2025 17:44:58 GMT  
		Size: 13.7 MB (13673444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36cef290a986b57366f166852fb0e5138be69723557ef721e396651b844e1a8e`  
		Last Modified: Fri, 17 Jan 2025 17:44:57 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7f2337ef5288bddc554d205307d28d7c0d7e494a59edc2481174d6eacda8c22`  
		Last Modified: Fri, 17 Jan 2025 17:44:58 GMT  
		Size: 38.9 MB (38949991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:637b18b0469b765305c1a92bac0c3d6a21be895b607f46887bdd42398b55c908`  
		Last Modified: Fri, 17 Jan 2025 17:44:57 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1799d1325cac3c1c89e36983daaba16c6f7ebbe2084305c3b5c511e9716b675f`  
		Last Modified: Fri, 17 Jan 2025 17:44:58 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-cli-bullseye` - unknown; unknown

```console
$ docker pull php@sha256:1c7021226d2c1799af64f1a327c67f03a410074f121718cc8a34744d6afcf641
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6428697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32e2dac3a7dbd51a3d8fb0c1139689dd1b62b288d486f6425331424dfe492ba2`

```dockerfile
```

-	Layers:
	-	`sha256:04e58715a2f62f979a310efa425be829f2f6e43cfdff2e929ca3db856fa6d297`  
		Last Modified: Fri, 17 Jan 2025 17:44:57 GMT  
		Size: 6.4 MB (6388014 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d89976dc4e779074c22760f12db23c6db93d83c6e23405b5fc2b5b42b2746df`  
		Last Modified: Fri, 17 Jan 2025 17:44:56 GMT  
		Size: 40.7 KB (40683 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-cli-bullseye` - linux; 386

```console
$ docker pull php@sha256:1d851d172bc67ba6f1f08fcfdd080e6eada891792aef84762302d5be46cc3c99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.5 MB (177530376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3369a075aa09b160dc6c2d597fa5604d4a804d4d81f07644ee16237154e3518`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Fri, 17 Jan 2025 01:46:40 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1738540800'
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 17 Jan 2025 01:46:40 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_VERSION=8.4.3
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 17 Jan 2025 01:46:40 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:af24a588b358e10d8284ac042756542ed964075987788d3d4a5fdbb6809e4de5`  
		Last Modified: Tue, 04 Feb 2025 01:36:34 GMT  
		Size: 31.2 MB (31178875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d0f568910f1eb5f0381f7317b418e4a0c85b7843d861d5d8c0df61036296936`  
		Last Modified: Tue, 04 Feb 2025 04:31:39 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13e13de310548ce32c71487e3730c381d505db79afd0f2310b6ad59afb246af8`  
		Last Modified: Tue, 04 Feb 2025 04:31:41 GMT  
		Size: 92.5 MB (92521524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7d56c160288e0c6cdaefd7461a6e215b489c2195eac499f99d292554d213a81`  
		Last Modified: Tue, 04 Feb 2025 04:31:39 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae213f7a28e43aa73bb1f3a2ee3dac79765dd3c2fc085d294bb1e0a17c431a7b`  
		Last Modified: Tue, 04 Feb 2025 04:31:40 GMT  
		Size: 13.7 MB (13673392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3beace4834b9be18df808cc0acbbbd515ae10dfe873e9af4ae692d4f5e9f1243`  
		Last Modified: Tue, 04 Feb 2025 04:31:40 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b5b95ed6cb8547990a012e9a782c7a6cc489de33d28f9068eaf3291295ddecf`  
		Last Modified: Tue, 04 Feb 2025 04:31:41 GMT  
		Size: 40.2 MB (40152963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acedf488e7e2630e7b24969573d4ab78e25ff8901e082cb3623869705a8f0bf0`  
		Last Modified: Tue, 04 Feb 2025 04:31:40 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:058ffe6335bdc430842321e009fba681f57e2b66d0a395528416113483618c10`  
		Last Modified: Tue, 04 Feb 2025 04:31:40 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-cli-bullseye` - unknown; unknown

```console
$ docker pull php@sha256:0d3c8e791d986466b3faa2d76ff1d3d58a9e78fcadaa3f229d25acb091f696cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6416243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3e4193a0dc32dbec80df0ced4402857201fbc56ccaf061520cb1b7ddf45f6a4`

```dockerfile
```

-	Layers:
	-	`sha256:b4550e5f3873ab121977bcb1fc27d98b6ad3072fd072f0baf67e2d3b2e17618e`  
		Last Modified: Tue, 04 Feb 2025 04:31:39 GMT  
		Size: 6.4 MB (6375849 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c1a4c095140c9a8e1e04ee376f7055ab140abb71bcd328884ddb8ec267dbb80`  
		Last Modified: Tue, 04 Feb 2025 04:31:39 GMT  
		Size: 40.4 KB (40394 bytes)  
		MIME: application/vnd.in-toto+json
