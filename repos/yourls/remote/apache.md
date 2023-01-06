## `yourls:apache`

```console
$ docker pull yourls@sha256:18f324fcef3690eb60f29be374a57021f02e3ef0c70d4e08d120ac93ebed77bc
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

### `yourls:apache` - linux; amd64

```console
$ docker pull yourls@sha256:38d3bafe23f5ce7a6dbaeffd0ceebd252bfbbfa5d45219cc77ade7a392a080a6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.8 MB (169847150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:546638d2e90ab5b4b8398691104db16621afe14e610d507a4f56302a28e8d721`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:32 GMT
ADD file:73e68ae6852c9afbb2989dc9c5b7c6668843f454b1bdcfb48658bfbc6c4af69e in / 
# Wed, 21 Dec 2022 01:20:33 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 05:06:31 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 21 Dec 2022 05:06:31 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 21 Dec 2022 05:06:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 05:06:50 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 21 Dec 2022 05:06:51 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 21 Dec 2022 05:10:24 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 21 Dec 2022 05:10:24 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 21 Dec 2022 05:10:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 21 Dec 2022 05:10:35 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 21 Dec 2022 05:10:35 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 21 Dec 2022 05:10:35 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 21 Dec 2022 05:10:35 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 21 Dec 2022 05:10:35 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 21 Dec 2022 06:04:27 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 06 Jan 2023 00:16:27 GMT
ENV PHP_VERSION=8.1.14
# Fri, 06 Jan 2023 00:16:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.14.tar.xz.asc
# Fri, 06 Jan 2023 00:16:27 GMT
ENV PHP_SHA256=e16e47a872d58685913ac848ce92ec49f42c1828110c98c65fb6265a08724a1a
# Fri, 06 Jan 2023 00:16:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 06 Jan 2023 00:16:39 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 06 Jan 2023 00:19:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 06 Jan 2023 00:19:38 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Fri, 06 Jan 2023 00:19:39 GMT
RUN docker-php-ext-enable sodium
# Fri, 06 Jan 2023 00:19:39 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 06 Jan 2023 00:19:39 GMT
STOPSIGNAL SIGWINCH
# Fri, 06 Jan 2023 00:19:39 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 06 Jan 2023 00:19:39 GMT
WORKDIR /var/www/html
# Fri, 06 Jan 2023 00:19:39 GMT
EXPOSE 80
# Fri, 06 Jan 2023 00:19:39 GMT
CMD ["apache2-foreground"]
# Fri, 06 Jan 2023 05:26:59 GMT
LABEL org.opencontainers.image.title=YOURLS
# Fri, 06 Jan 2023 05:26:59 GMT
LABEL org.opencontainers.image.description=Your Own URL Shortener
# Fri, 06 Jan 2023 05:26:59 GMT
LABEL org.opencontainers.image.url=https://yourls.org/
# Fri, 06 Jan 2023 05:27:00 GMT
LABEL org.opencontainers.image.documentation=https://yourls.org/
# Fri, 06 Jan 2023 05:27:00 GMT
LABEL org.opencontainers.image.vendor=YOURLS Org
# Fri, 06 Jan 2023 05:27:00 GMT
LABEL org.opencontainers.image.authors=YOURLS
# Fri, 06 Jan 2023 05:27:00 GMT
LABEL org.opencontainers.image.licenses=MIT
# Fri, 06 Jan 2023 05:27:00 GMT
LABEL io.artifacthub.package.readme-url=https://raw.githubusercontent.com/YOURLS/YOURLS/master/README.md
# Fri, 06 Jan 2023 05:27:42 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli
# Fri, 06 Jan 2023 05:27:42 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 06 Jan 2023 05:27:43 GMT
RUN a2enmod rewrite expires
# Fri, 06 Jan 2023 05:27:43 GMT
ARG YOURLS_VERSION=1.9.1
# Fri, 06 Jan 2023 05:27:43 GMT
ARG YOURLS_SHA256=0bf53290e8f86ea2e0121aac70f7c64d70d3dfb54823acb9dcc343dd7c5f455a
# Fri, 06 Jan 2023 05:27:43 GMT
LABEL org.opencontainers.image.version=1.9.1
# Fri, 06 Jan 2023 05:27:43 GMT
ENV YOURLS_VERSION=1.9.1
# Fri, 06 Jan 2023 05:27:43 GMT
ENV YOURLS_SHA256=0bf53290e8f86ea2e0121aac70f7c64d70d3dfb54823acb9dcc343dd7c5f455a
# Fri, 06 Jan 2023 05:27:45 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Fri, 06 Jan 2023 05:27:45 GMT
COPY --chown=www-data:www-datafile:f5584b9849b80034920f4de5f1297cb1be461f765f3437b87ddf6c86daa6499d in /usr/src/yourls/user/ 
# Fri, 06 Jan 2023 05:27:46 GMT
COPY file:975ababf859e7cabd8184ab0b2b317a5d8d3ccb6f4922be7f2a5d28c20d075a2 in /usr/local/bin/ 
# Fri, 06 Jan 2023 05:27:46 GMT
COPY file:5b7ff05d0c98ad759c4bec0ef8a7ce74cae42e95b42564b55f43b341c2c3e3f5 in /usr/src/yourls/ 
# Fri, 06 Jan 2023 05:27:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Jan 2023 05:27:46 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:3f4ca61aafcd4fc07267a105067db35c0f0ac630e1970f3cd0c7bf552780e985`  
		Last Modified: Wed, 21 Dec 2022 01:24:36 GMT  
		Size: 31.4 MB (31396943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:460703cf6140962e339a7c3f30256a39b69e89993380fb3c15ad2b939ae0859d`  
		Last Modified: Wed, 21 Dec 2022 07:24:59 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eba06349db8787dc6357728498b0da33035875a4d3fa2113c40809c3ba14a2f5`  
		Last Modified: Wed, 21 Dec 2022 07:25:13 GMT  
		Size: 91.6 MB (91634656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9130a4183abd1de004c2a4f7a86e4d4e2344614fbd43930c3e97830d7c26b4e7`  
		Last Modified: Wed, 21 Dec 2022 07:24:59 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd60536a08336b41945e7667d501c28c5ea1616423e0ad8dbeb58c6d2013fcaa`  
		Last Modified: Wed, 21 Dec 2022 07:25:40 GMT  
		Size: 19.2 MB (19244681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52e54498bf197269e593073f1b94750016135dcba55424358c496c8741ce09d7`  
		Last Modified: Wed, 21 Dec 2022 07:25:37 GMT  
		Size: 473.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9812d18c874fda64d6dafda204537681dbdbf44229ad4b0249f1bbb33e51ca50`  
		Last Modified: Wed, 21 Dec 2022 07:25:37 GMT  
		Size: 511.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cf3dd9bf3cdcfe6f2048df8fa27822bd7bab3c9c4c3361d2770ae6ac5089d2c`  
		Last Modified: Fri, 06 Jan 2023 01:51:04 GMT  
		Size: 12.1 MB (12093584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec04c06055d55cab5b9f2687eee58adadaaf5274d609cee1d25c87b0b4e0c1df`  
		Last Modified: Fri, 06 Jan 2023 01:51:01 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:143d2c3a0ec9975dd1046242c1a9d326c6a5be1a2d2eef6c247088bc7adc8ddb`  
		Last Modified: Fri, 06 Jan 2023 01:51:03 GMT  
		Size: 11.0 MB (11048910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ce6abbe3000d9d5e8f97da514ea5dd91b1c33b43c1b08a5fee4cb3bed022057`  
		Last Modified: Fri, 06 Jan 2023 01:51:01 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a71219d962f80c22951d5a04c893c682d124cc28027fd80e772eb4de737afbc5`  
		Last Modified: Fri, 06 Jan 2023 01:51:01 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e49fe66ca9a6920f22f6e49faed1580ce20862502a9aded850dd00f6118e9331`  
		Last Modified: Fri, 06 Jan 2023 01:51:01 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc417879665815786a496c6a4ac72f34991e004597301bc418afb759115df6a7`  
		Last Modified: Fri, 06 Jan 2023 05:30:19 GMT  
		Size: 514.6 KB (514649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a38f9d84db3c8dd70d0fae57ef751331720f46e3924c20588be915f3007de59`  
		Last Modified: Fri, 06 Jan 2023 05:30:18 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c72a6abbee14da3bcf4bab46c56726b8ea5b4a49b534b760954ee96d63c4f461`  
		Last Modified: Fri, 06 Jan 2023 05:30:16 GMT  
		Size: 345.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aa62a077286ec5af2552a625d9c2a5166c010141e200880bf36dffe4a47fced`  
		Last Modified: Fri, 06 Jan 2023 05:30:17 GMT  
		Size: 3.9 MB (3903535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20ac6f8a3db0524b5038a17923de4d433ce3267f9d6a1bcabed34872f2834d4d`  
		Last Modified: Fri, 06 Jan 2023 05:30:16 GMT  
		Size: 2.1 KB (2052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06128153e481ef4b3ab9b5b1ce1864a9a0ac175ab16c5066da6a651e9fae766c`  
		Last Modified: Fri, 06 Jan 2023 05:30:16 GMT  
		Size: 1.6 KB (1557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a100e5aa3f779fcde9d03e2f4bb6f43b77d049f3711a8194d793271bf3097ea7`  
		Last Modified: Fri, 06 Jan 2023 05:30:16 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:apache` - linux; arm variant v5

```console
$ docker pull yourls@sha256:94f4610714eacfdbc34612c4efc3b6323eee066f3aa93f608232a4bb3b50285b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.4 MB (147361508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29f59f2d248739a726fd1a94d5921e3730f3b9b5fe5b95a6a76ea42a3a3f9cec`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 21 Dec 2022 01:49:08 GMT
ADD file:89f7788ae38bc6c172614b734ff10cba90c89ee09ca0f1acccc185c1bec630a1 in / 
# Wed, 21 Dec 2022 01:49:09 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 03:12:23 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 21 Dec 2022 03:12:23 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 21 Dec 2022 03:12:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 03:12:44 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 21 Dec 2022 03:12:44 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 21 Dec 2022 03:16:06 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 21 Dec 2022 03:16:06 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 21 Dec 2022 03:16:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 21 Dec 2022 03:16:20 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 21 Dec 2022 03:16:20 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 21 Dec 2022 03:16:20 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 21 Dec 2022 03:16:20 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 21 Dec 2022 03:16:20 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 21 Dec 2022 03:45:36 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 06 Jan 2023 00:16:37 GMT
ENV PHP_VERSION=8.1.14
# Fri, 06 Jan 2023 00:16:37 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.14.tar.xz.asc
# Fri, 06 Jan 2023 00:16:38 GMT
ENV PHP_SHA256=e16e47a872d58685913ac848ce92ec49f42c1828110c98c65fb6265a08724a1a
# Fri, 06 Jan 2023 00:16:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 06 Jan 2023 00:16:54 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 06 Jan 2023 00:21:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 06 Jan 2023 00:21:56 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Fri, 06 Jan 2023 00:21:57 GMT
RUN docker-php-ext-enable sodium
# Fri, 06 Jan 2023 00:21:57 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 06 Jan 2023 00:21:57 GMT
STOPSIGNAL SIGWINCH
# Fri, 06 Jan 2023 00:21:57 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 06 Jan 2023 00:21:58 GMT
WORKDIR /var/www/html
# Fri, 06 Jan 2023 00:21:58 GMT
EXPOSE 80
# Fri, 06 Jan 2023 00:21:58 GMT
CMD ["apache2-foreground"]
# Fri, 06 Jan 2023 02:59:59 GMT
LABEL org.opencontainers.image.title=YOURLS
# Fri, 06 Jan 2023 02:59:59 GMT
LABEL org.opencontainers.image.description=Your Own URL Shortener
# Fri, 06 Jan 2023 02:59:59 GMT
LABEL org.opencontainers.image.url=https://yourls.org/
# Fri, 06 Jan 2023 02:59:59 GMT
LABEL org.opencontainers.image.documentation=https://yourls.org/
# Fri, 06 Jan 2023 03:00:00 GMT
LABEL org.opencontainers.image.vendor=YOURLS Org
# Fri, 06 Jan 2023 03:00:00 GMT
LABEL org.opencontainers.image.authors=YOURLS
# Fri, 06 Jan 2023 03:00:00 GMT
LABEL org.opencontainers.image.licenses=MIT
# Fri, 06 Jan 2023 03:00:00 GMT
LABEL io.artifacthub.package.readme-url=https://raw.githubusercontent.com/YOURLS/YOURLS/master/README.md
# Fri, 06 Jan 2023 03:00:21 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli
# Fri, 06 Jan 2023 03:00:22 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 06 Jan 2023 03:00:22 GMT
RUN a2enmod rewrite expires
# Fri, 06 Jan 2023 03:00:22 GMT
ARG YOURLS_VERSION=1.9.1
# Fri, 06 Jan 2023 03:00:22 GMT
ARG YOURLS_SHA256=0bf53290e8f86ea2e0121aac70f7c64d70d3dfb54823acb9dcc343dd7c5f455a
# Fri, 06 Jan 2023 03:00:23 GMT
LABEL org.opencontainers.image.version=1.9.1
# Fri, 06 Jan 2023 03:00:23 GMT
ENV YOURLS_VERSION=1.9.1
# Fri, 06 Jan 2023 03:00:23 GMT
ENV YOURLS_SHA256=0bf53290e8f86ea2e0121aac70f7c64d70d3dfb54823acb9dcc343dd7c5f455a
# Fri, 06 Jan 2023 03:00:25 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Fri, 06 Jan 2023 03:00:25 GMT
COPY --chown=www-data:www-datafile:f5584b9849b80034920f4de5f1297cb1be461f765f3437b87ddf6c86daa6499d in /usr/src/yourls/user/ 
# Fri, 06 Jan 2023 03:00:25 GMT
COPY file:975ababf859e7cabd8184ab0b2b317a5d8d3ccb6f4922be7f2a5d28c20d075a2 in /usr/local/bin/ 
# Fri, 06 Jan 2023 03:00:25 GMT
COPY file:5b7ff05d0c98ad759c4bec0ef8a7ce74cae42e95b42564b55f43b341c2c3e3f5 in /usr/src/yourls/ 
# Fri, 06 Jan 2023 03:00:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Jan 2023 03:00:26 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:6addfee759f2774f92392906ab5b50ba2f4a14314858c502e856f7d7de2a7e07`  
		Last Modified: Wed, 21 Dec 2022 01:54:03 GMT  
		Size: 28.9 MB (28898607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a9d6b0a4c348f2acc126a26d45600c97234dc9c1280bc45aa1273e17e6a84c1`  
		Last Modified: Wed, 21 Dec 2022 04:29:00 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c501678603c45e97e3a59b6d68da5b1b8c2c7d722e08be9317819c4261c14897`  
		Last Modified: Wed, 21 Dec 2022 04:29:16 GMT  
		Size: 73.7 MB (73686551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a59e0b6e2b0a7211798fe853414b53d3c41263af6fa379898febb3b275ef4856`  
		Last Modified: Wed, 21 Dec 2022 04:29:00 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd289d1f09762f0ba56809e8fbf54703e29c0c807ce1d8381fffcb382a5e17d6`  
		Last Modified: Wed, 21 Dec 2022 04:29:53 GMT  
		Size: 18.6 MB (18554253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db60116a1fbc1e7697014d2d18759adb437b9cc2027efe4d9080f5b685854011`  
		Last Modified: Wed, 21 Dec 2022 04:29:49 GMT  
		Size: 436.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e2fac801028417e08d2e48a6042a9776aec5ce2ee903650ebbe57ce26be34c4`  
		Last Modified: Wed, 21 Dec 2022 04:29:49 GMT  
		Size: 485.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87d9af284de219d973e15faf3c9d82c49641d6517778e0967e8e692656ee74b9`  
		Last Modified: Fri, 06 Jan 2023 01:05:52 GMT  
		Size: 12.1 MB (12091975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75b9f8404f10f8042f90d61402f3bc49c1199b0eacfd0a4f994a9b64924ee3c7`  
		Last Modified: Fri, 06 Jan 2023 01:05:48 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b3ae9f8f75fa04d3bc901cc5132dc83c933368dddb4c99b016849b2620905de`  
		Last Modified: Fri, 06 Jan 2023 01:05:51 GMT  
		Size: 10.1 MB (10065796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fe3e87a512884794a00e725fdccd3fb3bf4cfd985b21a398b55142753d1ebe0`  
		Last Modified: Fri, 06 Jan 2023 01:05:48 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01c18e7b010b99715c0c658b1a283fa5dba7de7b7fb076272359eda2700ac2a1`  
		Last Modified: Fri, 06 Jan 2023 01:05:48 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a13a9fb45772abe1e79bfcbe308312e979e42e3f1636a2fd0c6a1bdd5ba9198`  
		Last Modified: Fri, 06 Jan 2023 01:05:48 GMT  
		Size: 895.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f9e7e0aa0ac20d94c348d4ec38b0e13a5bcf7dfbac294c4e39bab1f115c8836`  
		Last Modified: Fri, 06 Jan 2023 03:01:37 GMT  
		Size: 150.7 KB (150715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f8782620d4d6a70612692ce1cebb2296c5f6a0512872889770b9cf57ffae885`  
		Last Modified: Fri, 06 Jan 2023 03:01:37 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f1513e745847f007c70de6060f24365bf304fcf77f496bd5440cd5fedcd34d1`  
		Last Modified: Fri, 06 Jan 2023 03:01:35 GMT  
		Size: 345.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f7e858d67261fd71535711ba9e5d73bfac5ddc9242dcd618c196f5da968fce5`  
		Last Modified: Fri, 06 Jan 2023 03:01:36 GMT  
		Size: 3.9 MB (3903531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49eccec046442fc03a953c6ed761a3cf86c027dd7269c5c8a3807fa7d4ee4d6d`  
		Last Modified: Fri, 06 Jan 2023 03:01:35 GMT  
		Size: 2.1 KB (2054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afbdf83c4436df07e5336d161bfaf2b52b469647f3a9bb5e6e379c858c2eb8bd`  
		Last Modified: Fri, 06 Jan 2023 03:01:35 GMT  
		Size: 1.6 KB (1557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93e917184623b5ca848a45757d358565a0f3939164384ffd2b55daea02a95cc8`  
		Last Modified: Fri, 06 Jan 2023 03:01:35 GMT  
		Size: 333.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:apache` - linux; arm variant v7

```console
$ docker pull yourls@sha256:a39f74c5b09c550042640f002fa1eb97ee1bbad38b357a52e8218342c9ed8309
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.6 MB (139560279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7960853c1aeb31fbd500a208bdfec11970a22a6dfbfb52dad7b8cb82c13ed8a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 21 Dec 2022 01:58:25 GMT
ADD file:d62015d4eb206b606ae0bc76253de55403ede851d6fae0277e76bdaed196a848 in / 
# Wed, 21 Dec 2022 01:58:26 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 19:49:58 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 21 Dec 2022 19:49:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 21 Dec 2022 19:50:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 19:50:16 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 21 Dec 2022 19:50:17 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 21 Dec 2022 19:52:55 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 21 Dec 2022 19:52:55 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 21 Dec 2022 19:53:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 21 Dec 2022 19:53:06 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 21 Dec 2022 19:53:06 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 21 Dec 2022 19:53:06 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 21 Dec 2022 19:53:06 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 21 Dec 2022 19:53:06 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 21 Dec 2022 20:37:58 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Thu, 05 Jan 2023 23:42:57 GMT
ENV PHP_VERSION=8.1.14
# Thu, 05 Jan 2023 23:42:57 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.14.tar.xz.asc
# Thu, 05 Jan 2023 23:42:57 GMT
ENV PHP_SHA256=e16e47a872d58685913ac848ce92ec49f42c1828110c98c65fb6265a08724a1a
# Thu, 05 Jan 2023 23:43:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 05 Jan 2023 23:43:09 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 05 Jan 2023 23:45:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 05 Jan 2023 23:45:31 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Thu, 05 Jan 2023 23:45:32 GMT
RUN docker-php-ext-enable sodium
# Thu, 05 Jan 2023 23:45:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 05 Jan 2023 23:45:32 GMT
STOPSIGNAL SIGWINCH
# Thu, 05 Jan 2023 23:45:32 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 05 Jan 2023 23:45:32 GMT
WORKDIR /var/www/html
# Thu, 05 Jan 2023 23:45:32 GMT
EXPOSE 80
# Thu, 05 Jan 2023 23:45:32 GMT
CMD ["apache2-foreground"]
# Fri, 06 Jan 2023 06:04:36 GMT
LABEL org.opencontainers.image.title=YOURLS
# Fri, 06 Jan 2023 06:04:36 GMT
LABEL org.opencontainers.image.description=Your Own URL Shortener
# Fri, 06 Jan 2023 06:04:37 GMT
LABEL org.opencontainers.image.url=https://yourls.org/
# Fri, 06 Jan 2023 06:04:37 GMT
LABEL org.opencontainers.image.documentation=https://yourls.org/
# Fri, 06 Jan 2023 06:04:37 GMT
LABEL org.opencontainers.image.vendor=YOURLS Org
# Fri, 06 Jan 2023 06:04:37 GMT
LABEL org.opencontainers.image.authors=YOURLS
# Fri, 06 Jan 2023 06:04:37 GMT
LABEL org.opencontainers.image.licenses=MIT
# Fri, 06 Jan 2023 06:04:37 GMT
LABEL io.artifacthub.package.readme-url=https://raw.githubusercontent.com/YOURLS/YOURLS/master/README.md
# Fri, 06 Jan 2023 06:04:56 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli
# Fri, 06 Jan 2023 06:04:57 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 06 Jan 2023 06:04:58 GMT
RUN a2enmod rewrite expires
# Fri, 06 Jan 2023 06:04:58 GMT
ARG YOURLS_VERSION=1.9.1
# Fri, 06 Jan 2023 06:04:58 GMT
ARG YOURLS_SHA256=0bf53290e8f86ea2e0121aac70f7c64d70d3dfb54823acb9dcc343dd7c5f455a
# Fri, 06 Jan 2023 06:04:58 GMT
LABEL org.opencontainers.image.version=1.9.1
# Fri, 06 Jan 2023 06:04:58 GMT
ENV YOURLS_VERSION=1.9.1
# Fri, 06 Jan 2023 06:04:58 GMT
ENV YOURLS_SHA256=0bf53290e8f86ea2e0121aac70f7c64d70d3dfb54823acb9dcc343dd7c5f455a
# Fri, 06 Jan 2023 06:05:00 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Fri, 06 Jan 2023 06:05:00 GMT
COPY --chown=www-data:www-datafile:f5584b9849b80034920f4de5f1297cb1be461f765f3437b87ddf6c86daa6499d in /usr/src/yourls/user/ 
# Fri, 06 Jan 2023 06:05:00 GMT
COPY file:975ababf859e7cabd8184ab0b2b317a5d8d3ccb6f4922be7f2a5d28c20d075a2 in /usr/local/bin/ 
# Fri, 06 Jan 2023 06:05:00 GMT
COPY file:5b7ff05d0c98ad759c4bec0ef8a7ce74cae42e95b42564b55f43b341c2c3e3f5 in /usr/src/yourls/ 
# Fri, 06 Jan 2023 06:05:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Jan 2023 06:05:01 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:f8686edc9eb6f431c8c17a5eddc7bd38917d3b2d7835970d4fdb2ad0db464766`  
		Last Modified: Wed, 21 Dec 2022 02:05:08 GMT  
		Size: 26.6 MB (26559455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13dbb8de606b0f3d134da534a92e95d7e64924e21a9da63f1acf5f770151b217`  
		Last Modified: Wed, 21 Dec 2022 21:52:38 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8c75b7feafe5c1472546089e973b9927e0deed72e4259fc0d8d21a6a123f927`  
		Last Modified: Wed, 21 Dec 2022 21:52:51 GMT  
		Size: 69.3 MB (69321332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c20e1e24e25c1485227c7002e4c00565aa7f85c6c3e4f80b87c5dca435e30f5d`  
		Last Modified: Wed, 21 Dec 2022 21:52:38 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2107dded52a8a1d78469f718aa0de0dfdca5379b18962bbd44914c9faa43c95e`  
		Last Modified: Wed, 21 Dec 2022 21:53:27 GMT  
		Size: 18.0 MB (17997761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fe372701f61ed8eaf00d0ef1ebc526dcf908c0569af2b30b375ed0dc69a5ae6`  
		Last Modified: Wed, 21 Dec 2022 21:53:24 GMT  
		Size: 434.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9113ea9d118b2d3fd2336b37675c183a8fe18b917568521515a1fa605febe77d`  
		Last Modified: Wed, 21 Dec 2022 21:53:24 GMT  
		Size: 488.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82e9f8c7e77bde0d005b88cfce7472f5b14573410a4ff2f56c279781bdd24ea8`  
		Last Modified: Fri, 06 Jan 2023 01:46:57 GMT  
		Size: 12.1 MB (12092000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afc21476560a968abb91785b8da87a0971c5759cbfdfff9fc038875388b6af12`  
		Last Modified: Fri, 06 Jan 2023 01:46:54 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82b8ee6a0487c41ad351c3f8260081e6d2765ac0fc132eaf518c5b4b60c7cff2`  
		Last Modified: Fri, 06 Jan 2023 01:46:56 GMT  
		Size: 9.5 MB (9537725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4e5208ad3489148e66169644e480c0f26464d6a93dde5871ce07e0a8203c0f6`  
		Last Modified: Fri, 06 Jan 2023 01:46:54 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7027aaf58530f712bd793fd30db826668994fbec19fbedbccd13340ac74e3d19`  
		Last Modified: Fri, 06 Jan 2023 01:46:54 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72ed9550481c6233fbac1e20806c72dd1f240185123e43afb85d5e1a791f8bff`  
		Last Modified: Fri, 06 Jan 2023 01:46:54 GMT  
		Size: 891.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5ac4ad9bca4383949fe31e61e5c9b46e3691cee2aabfa5934b3055ff82df10f`  
		Last Modified: Fri, 06 Jan 2023 06:07:05 GMT  
		Size: 138.4 KB (138403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3df977bcedea3d1afca96a8bf275f57cca3aeb301a01b04036bb3fee3028309a`  
		Last Modified: Fri, 06 Jan 2023 06:07:05 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb81a35e229c3c13ec83a0d546ffdbe0bd80d1503006a2b93ab805fabf8fff24`  
		Last Modified: Fri, 06 Jan 2023 06:07:03 GMT  
		Size: 344.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7c821bbcbe8785c70085f35473629f3706434f3660de8749cae9aea3205bc0e`  
		Last Modified: Fri, 06 Jan 2023 06:07:04 GMT  
		Size: 3.9 MB (3903533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa3f8084a9471fa57367a6610b8ae231ea22f3eae8f356cd63002bfb068896d5`  
		Last Modified: Fri, 06 Jan 2023 06:07:03 GMT  
		Size: 2.1 KB (2052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae3bc89c05fe953d3647ff6f24e47fa4fe0fc06cdd3a8855dff6b6490c34caeb`  
		Last Modified: Fri, 06 Jan 2023 06:07:03 GMT  
		Size: 1.6 KB (1556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9554f8e15b1fe26e0c5c016aee3b50456888d93ea3deff948bd4e441dd7f0a7a`  
		Last Modified: Fri, 06 Jan 2023 06:07:03 GMT  
		Size: 333.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:apache` - linux; arm64 variant v8

```console
$ docker pull yourls@sha256:5c1e56b5e7bbb7483c5b4ce727c58a703e3d79c03abf64223d7c887d66ed5712
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.1 MB (164050057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aae72da06003d7a125f1b371560239441854065ecae2d04fbea8de5aaf23d559`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 21 Dec 2022 01:39:48 GMT
ADD file:3ff0cc8d111595978eb50cdba91144382ce083c400d45785d53dbb03615a4890 in / 
# Wed, 21 Dec 2022 01:39:48 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 06:06:05 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 21 Dec 2022 06:06:05 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 21 Dec 2022 06:06:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 06:06:22 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 21 Dec 2022 06:06:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 21 Dec 2022 06:09:27 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 21 Dec 2022 06:09:27 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 21 Dec 2022 06:09:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 21 Dec 2022 06:09:35 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 21 Dec 2022 06:09:35 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 21 Dec 2022 06:09:35 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 21 Dec 2022 06:09:35 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 21 Dec 2022 06:09:36 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 21 Dec 2022 06:58:51 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 06 Jan 2023 00:37:06 GMT
ENV PHP_VERSION=8.1.14
# Fri, 06 Jan 2023 00:37:06 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.14.tar.xz.asc
# Fri, 06 Jan 2023 00:37:06 GMT
ENV PHP_SHA256=e16e47a872d58685913ac848ce92ec49f42c1828110c98c65fb6265a08724a1a
# Fri, 06 Jan 2023 00:37:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 06 Jan 2023 00:37:17 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 06 Jan 2023 00:40:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 06 Jan 2023 00:40:12 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Fri, 06 Jan 2023 00:40:13 GMT
RUN docker-php-ext-enable sodium
# Fri, 06 Jan 2023 00:40:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 06 Jan 2023 00:40:13 GMT
STOPSIGNAL SIGWINCH
# Fri, 06 Jan 2023 00:40:13 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 06 Jan 2023 00:40:13 GMT
WORKDIR /var/www/html
# Fri, 06 Jan 2023 00:40:13 GMT
EXPOSE 80
# Fri, 06 Jan 2023 00:40:13 GMT
CMD ["apache2-foreground"]
# Fri, 06 Jan 2023 04:44:22 GMT
LABEL org.opencontainers.image.title=YOURLS
# Fri, 06 Jan 2023 04:44:22 GMT
LABEL org.opencontainers.image.description=Your Own URL Shortener
# Fri, 06 Jan 2023 04:44:22 GMT
LABEL org.opencontainers.image.url=https://yourls.org/
# Fri, 06 Jan 2023 04:44:22 GMT
LABEL org.opencontainers.image.documentation=https://yourls.org/
# Fri, 06 Jan 2023 04:44:22 GMT
LABEL org.opencontainers.image.vendor=YOURLS Org
# Fri, 06 Jan 2023 04:44:22 GMT
LABEL org.opencontainers.image.authors=YOURLS
# Fri, 06 Jan 2023 04:44:22 GMT
LABEL org.opencontainers.image.licenses=MIT
# Fri, 06 Jan 2023 04:44:22 GMT
LABEL io.artifacthub.package.readme-url=https://raw.githubusercontent.com/YOURLS/YOURLS/master/README.md
# Fri, 06 Jan 2023 04:45:16 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli
# Fri, 06 Jan 2023 04:45:16 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 06 Jan 2023 04:45:17 GMT
RUN a2enmod rewrite expires
# Fri, 06 Jan 2023 04:45:17 GMT
ARG YOURLS_VERSION=1.9.1
# Fri, 06 Jan 2023 04:45:17 GMT
ARG YOURLS_SHA256=0bf53290e8f86ea2e0121aac70f7c64d70d3dfb54823acb9dcc343dd7c5f455a
# Fri, 06 Jan 2023 04:45:17 GMT
LABEL org.opencontainers.image.version=1.9.1
# Fri, 06 Jan 2023 04:45:17 GMT
ENV YOURLS_VERSION=1.9.1
# Fri, 06 Jan 2023 04:45:17 GMT
ENV YOURLS_SHA256=0bf53290e8f86ea2e0121aac70f7c64d70d3dfb54823acb9dcc343dd7c5f455a
# Fri, 06 Jan 2023 04:45:19 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Fri, 06 Jan 2023 04:45:19 GMT
COPY --chown=www-data:www-datafile:f5584b9849b80034920f4de5f1297cb1be461f765f3437b87ddf6c86daa6499d in /usr/src/yourls/user/ 
# Fri, 06 Jan 2023 04:45:19 GMT
COPY file:975ababf859e7cabd8184ab0b2b317a5d8d3ccb6f4922be7f2a5d28c20d075a2 in /usr/local/bin/ 
# Fri, 06 Jan 2023 04:45:19 GMT
COPY file:5b7ff05d0c98ad759c4bec0ef8a7ce74cae42e95b42564b55f43b341c2c3e3f5 in /usr/src/yourls/ 
# Fri, 06 Jan 2023 04:45:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Jan 2023 04:45:19 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:4b7f5b2a311310809ab89d92f6f71b0462722fe855d3b92c93098a528aa08791`  
		Last Modified: Wed, 21 Dec 2022 01:43:12 GMT  
		Size: 30.0 MB (30044772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:165ed9670c1d43fe031d8dbdf1245e91ddcc8a7b9ebef601b6fbc74b965f0aaa`  
		Last Modified: Wed, 21 Dec 2022 08:06:04 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:952f716ee879c83e623ce98be3a2d7e20cc2f76201d414323bf4df4115191b97`  
		Last Modified: Wed, 21 Dec 2022 08:06:14 GMT  
		Size: 86.9 MB (86926576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce55625aa2b47393d76205f33f38efd485c611b282d0f06efa824b515e3006dd`  
		Last Modified: Wed, 21 Dec 2022 08:06:03 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aec000a9f339ae26b6d2b7e4d0e0b8999a704635cb0492acabdcb39386b87a65`  
		Last Modified: Wed, 21 Dec 2022 08:06:40 GMT  
		Size: 19.2 MB (19166186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ebad50c90d4b14cd5063ea1ac2e84011c82d77ef362e18c22072c9f8aff34e`  
		Last Modified: Wed, 21 Dec 2022 08:06:38 GMT  
		Size: 471.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ae770a57a4d6d026941fda54c54aaf2c10e4bf1807348a3a25859aacd1b1b4a`  
		Last Modified: Wed, 21 Dec 2022 08:06:38 GMT  
		Size: 513.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c291ce88696e50a2c8be58368fda243845776eaa8510fcd892306f7f1d008740`  
		Last Modified: Fri, 06 Jan 2023 02:01:05 GMT  
		Size: 12.1 MB (12092812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfb2faa21fcc5c3c180afcfb4da30674b2664c903944c571d92ad27545b7b5fb`  
		Last Modified: Fri, 06 Jan 2023 02:01:02 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a46d5bca88e7ddeb0b7dd9875499f24bd4e6ef2fd759199bf9e5e2ea36729ee`  
		Last Modified: Fri, 06 Jan 2023 02:01:04 GMT  
		Size: 11.1 MB (11112922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74012f233148d7e9620205bfbc1148b073f2b3609eceb71034b63473636e77bb`  
		Last Modified: Fri, 06 Jan 2023 02:01:02 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff2c3fdc1c9ac719d0be8abeecc66487a521598663cdbeb0a0282f7800960827`  
		Last Modified: Fri, 06 Jan 2023 02:01:02 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd95aa49c9ca9e765f5bd11b8ff311814295608b12412195950fbc6fe9627d93`  
		Last Modified: Fri, 06 Jan 2023 02:01:02 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6a5d4da7cbc424059cedea1a5ff55dd716d3b6ee2dfcb18b3224e7ab4c23f26`  
		Last Modified: Fri, 06 Jan 2023 04:48:24 GMT  
		Size: 793.1 KB (793060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49a53b4e26d27538c4b0411f6c6a147764e2b85fc22511aeeb575f577604c18c`  
		Last Modified: Fri, 06 Jan 2023 04:48:23 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:502150e65909da687292f21e540abb7e46fa7c661e263ec501c499bb01397063`  
		Last Modified: Fri, 06 Jan 2023 04:48:22 GMT  
		Size: 351.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3448e90512aa5b49f9be1c4eb3d319724f8b789ea0443a22a97243e681280bf5`  
		Last Modified: Fri, 06 Jan 2023 04:48:22 GMT  
		Size: 3.9 MB (3903532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e52552db6f6282ea30f39c181d49cf872c767dbeb7e99fa6afa9aad26315f4b7`  
		Last Modified: Fri, 06 Jan 2023 04:48:22 GMT  
		Size: 2.1 KB (2053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32ba7ae41ed4160588caad4246439fbd0251dbcd4c0feb7f9952ba949b20b892`  
		Last Modified: Fri, 06 Jan 2023 04:48:22 GMT  
		Size: 1.6 KB (1556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58525a04f776dac8139c47d2440d4e045196986d03031c76e7076d921d2a24ff`  
		Last Modified: Fri, 06 Jan 2023 04:48:22 GMT  
		Size: 331.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:apache` - linux; 386

```console
$ docker pull yourls@sha256:b217c38ed5dec456f8d5c32af5a4c39c4d2345369cae1ec3d06f7ebcb5a30546
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.2 MB (172165047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff51428d2e9812e136456b47f7e575bd7e952d79addcfe4b5c7155bcf0074c93`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 21 Dec 2022 01:39:22 GMT
ADD file:5f553fdf893bb3198d173c48f4531e9bfdbab61798c1aa8217fd80e9d686d7ae in / 
# Wed, 21 Dec 2022 01:39:22 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:39:08 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 21 Dec 2022 02:39:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 21 Dec 2022 02:39:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:39:29 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 21 Dec 2022 02:39:30 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 21 Dec 2022 02:42:50 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 21 Dec 2022 02:42:51 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 21 Dec 2022 02:43:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 21 Dec 2022 02:43:02 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 21 Dec 2022 02:43:03 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 21 Dec 2022 02:43:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 21 Dec 2022 02:43:04 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 21 Dec 2022 02:43:05 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 21 Dec 2022 03:34:21 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 06 Jan 2023 00:32:42 GMT
ENV PHP_VERSION=8.1.14
# Fri, 06 Jan 2023 00:32:43 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.14.tar.xz.asc
# Fri, 06 Jan 2023 00:32:44 GMT
ENV PHP_SHA256=e16e47a872d58685913ac848ce92ec49f42c1828110c98c65fb6265a08724a1a
# Fri, 06 Jan 2023 00:32:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 06 Jan 2023 00:32:58 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 06 Jan 2023 00:35:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 06 Jan 2023 00:35:46 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Fri, 06 Jan 2023 00:35:46 GMT
RUN docker-php-ext-enable sodium
# Fri, 06 Jan 2023 00:35:47 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 06 Jan 2023 00:35:48 GMT
STOPSIGNAL SIGWINCH
# Fri, 06 Jan 2023 00:35:50 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 06 Jan 2023 00:35:50 GMT
WORKDIR /var/www/html
# Fri, 06 Jan 2023 00:35:51 GMT
EXPOSE 80
# Fri, 06 Jan 2023 00:35:52 GMT
CMD ["apache2-foreground"]
# Fri, 06 Jan 2023 05:33:14 GMT
LABEL org.opencontainers.image.title=YOURLS
# Fri, 06 Jan 2023 05:33:15 GMT
LABEL org.opencontainers.image.description=Your Own URL Shortener
# Fri, 06 Jan 2023 05:33:16 GMT
LABEL org.opencontainers.image.url=https://yourls.org/
# Fri, 06 Jan 2023 05:33:17 GMT
LABEL org.opencontainers.image.documentation=https://yourls.org/
# Fri, 06 Jan 2023 05:33:18 GMT
LABEL org.opencontainers.image.vendor=YOURLS Org
# Fri, 06 Jan 2023 05:33:19 GMT
LABEL org.opencontainers.image.authors=YOURLS
# Fri, 06 Jan 2023 05:33:20 GMT
LABEL org.opencontainers.image.licenses=MIT
# Fri, 06 Jan 2023 05:33:21 GMT
LABEL io.artifacthub.package.readme-url=https://raw.githubusercontent.com/YOURLS/YOURLS/master/README.md
# Fri, 06 Jan 2023 05:33:58 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli
# Fri, 06 Jan 2023 05:33:59 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 06 Jan 2023 05:34:00 GMT
RUN a2enmod rewrite expires
# Fri, 06 Jan 2023 05:34:01 GMT
ARG YOURLS_VERSION=1.9.1
# Fri, 06 Jan 2023 05:34:02 GMT
ARG YOURLS_SHA256=0bf53290e8f86ea2e0121aac70f7c64d70d3dfb54823acb9dcc343dd7c5f455a
# Fri, 06 Jan 2023 05:34:03 GMT
LABEL org.opencontainers.image.version=1.9.1
# Fri, 06 Jan 2023 05:34:04 GMT
ENV YOURLS_VERSION=1.9.1
# Fri, 06 Jan 2023 05:34:05 GMT
ENV YOURLS_SHA256=0bf53290e8f86ea2e0121aac70f7c64d70d3dfb54823acb9dcc343dd7c5f455a
# Fri, 06 Jan 2023 05:34:08 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Fri, 06 Jan 2023 05:34:09 GMT
COPY --chown=www-data:www-datafile:f5584b9849b80034920f4de5f1297cb1be461f765f3437b87ddf6c86daa6499d in /usr/src/yourls/user/ 
# Fri, 06 Jan 2023 05:34:10 GMT
COPY file:975ababf859e7cabd8184ab0b2b317a5d8d3ccb6f4922be7f2a5d28c20d075a2 in /usr/local/bin/ 
# Fri, 06 Jan 2023 05:34:11 GMT
COPY file:5b7ff05d0c98ad759c4bec0ef8a7ce74cae42e95b42564b55f43b341c2c3e3f5 in /usr/src/yourls/ 
# Fri, 06 Jan 2023 05:34:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Jan 2023 05:34:12 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:3228cb514e81f042720b7fd118ace0f279d1a4bc422b7e24189514a574dfa546`  
		Last Modified: Wed, 21 Dec 2022 01:44:46 GMT  
		Size: 32.4 MB (32375745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7110976b695f91ec9f6d3d2dba4974dcb6f42afe84906d50adc945fe6584059b`  
		Last Modified: Wed, 21 Dec 2022 04:55:18 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bad2fa6fb8e9d0bed7870f237359cbb374ecf422d0ec601c64b0c77bd0e059`  
		Last Modified: Wed, 21 Dec 2022 04:55:31 GMT  
		Size: 92.7 MB (92716428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cb541bbb0d1d84df303bf8cc14996815ca0ee0de4ca13450a3c4a0a70aba37b`  
		Last Modified: Wed, 21 Dec 2022 04:55:18 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c924ed040cc70fb75fd335d86f8a9b944be216ed081af016f975bbbf170fa98`  
		Last Modified: Wed, 21 Dec 2022 04:56:03 GMT  
		Size: 19.5 MB (19515942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd73ac1df6b260089ac59e7d6d965092a75171f1d7e33d2d3680d8a39b3c8050`  
		Last Modified: Wed, 21 Dec 2022 04:56:00 GMT  
		Size: 431.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0b06672aed4320ba35409b7f4321cd2349bc1777fd18bda6e556e1c6a6c958c`  
		Last Modified: Wed, 21 Dec 2022 04:56:00 GMT  
		Size: 485.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ddace3e71750afeaa1d2a4046fbe086353c7d133b09243fef4067ae3c184c9`  
		Last Modified: Fri, 06 Jan 2023 02:10:09 GMT  
		Size: 11.9 MB (11876412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33c9bec46db37848c6ae5a074efb67ebbf246f42c5d2a54ad4bf392e67da7dfb`  
		Last Modified: Fri, 06 Jan 2023 02:10:06 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff32515f539d7e16b5ed70d88d3078d9f313e013cf4e4d75551b4ce97cde9efc`  
		Last Modified: Fri, 06 Jan 2023 02:10:08 GMT  
		Size: 11.3 MB (11272100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6808702319edf8ed76e6e7a00926f8d93fad486f87ca80c39d9eaa47680e6d99`  
		Last Modified: Fri, 06 Jan 2023 02:10:06 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de5e0c0be038e344d36d225976ddc90c638c7ef0ae44eb6d3b9b4f7fbf6f0467`  
		Last Modified: Fri, 06 Jan 2023 02:10:06 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32bb14c653627f4a00926f9b55111818ffc43554d7a863baf1c53735983675b1`  
		Last Modified: Fri, 06 Jan 2023 02:10:06 GMT  
		Size: 895.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44dec4031c0952241b18d77326ddedebfe749e5d247f0d8459f0fe857c82a427`  
		Last Modified: Fri, 06 Jan 2023 05:37:16 GMT  
		Size: 494.9 KB (494915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d540a54d9d8626bdd685816d913bbc31238ba9c32ecf91a22c260040bc955c6`  
		Last Modified: Fri, 06 Jan 2023 05:37:16 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9472efb243bae5180f7f05ddb5a7485a91e62889d0e7eb78db564d51d65327f4`  
		Last Modified: Fri, 06 Jan 2023 05:37:14 GMT  
		Size: 344.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9859b121d5caf755ebb1b1a78e26c0375adf4b0bf1e6b18d436b53f56177a62`  
		Last Modified: Fri, 06 Jan 2023 05:37:15 GMT  
		Size: 3.9 MB (3903429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7acaa6004cd58c0190059ec21a47f229bf6834cf70e8a2f3374e878b10af764d`  
		Last Modified: Fri, 06 Jan 2023 05:37:14 GMT  
		Size: 2.1 KB (2054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b217ebd4c862dde27350183b05210e063a0c7c2b1ce65939b2693fe75359665`  
		Last Modified: Fri, 06 Jan 2023 05:37:14 GMT  
		Size: 1.6 KB (1553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47b4db893971a13195e5f9843f27976ccacd8c70789ada0bc19ba2da01745e07`  
		Last Modified: Fri, 06 Jan 2023 05:37:14 GMT  
		Size: 335.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:apache` - linux; mips64le

```console
$ docker pull yourls@sha256:89d688c8e5e28b414d1367aa737559ff63260f500051127ad331033fe833938f
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.7 MB (146712863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:136927a3a7265cca8f29bfc936d5fd4b843a723ac5eb9032c927bb5ab0eba902`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 21 Dec 2022 01:10:32 GMT
ADD file:45a0ac3f00e914341df42a4d2a56b9081a224ee58e1167fb05ca87662d42f24c in / 
# Wed, 21 Dec 2022 01:10:37 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 14:59:31 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 21 Dec 2022 14:59:34 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 21 Dec 2022 15:01:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 15:01:12 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 21 Dec 2022 15:01:18 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 21 Dec 2022 15:16:06 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 21 Dec 2022 15:16:09 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 21 Dec 2022 15:17:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 21 Dec 2022 15:17:10 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 21 Dec 2022 15:17:16 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 21 Dec 2022 15:17:19 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 21 Dec 2022 15:17:23 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 21 Dec 2022 15:17:26 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 21 Dec 2022 17:13:30 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 06 Jan 2023 00:19:44 GMT
ENV PHP_VERSION=8.1.14
# Fri, 06 Jan 2023 00:19:47 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.14.tar.xz.asc
# Fri, 06 Jan 2023 00:19:51 GMT
ENV PHP_SHA256=e16e47a872d58685913ac848ce92ec49f42c1828110c98c65fb6265a08724a1a
# Fri, 06 Jan 2023 00:20:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 06 Jan 2023 00:20:43 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 06 Jan 2023 00:34:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 06 Jan 2023 00:34:21 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Fri, 06 Jan 2023 00:34:28 GMT
RUN docker-php-ext-enable sodium
# Fri, 06 Jan 2023 00:34:31 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 06 Jan 2023 00:34:35 GMT
STOPSIGNAL SIGWINCH
# Fri, 06 Jan 2023 00:34:38 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 06 Jan 2023 00:34:41 GMT
WORKDIR /var/www/html
# Fri, 06 Jan 2023 00:34:45 GMT
EXPOSE 80
# Fri, 06 Jan 2023 00:34:48 GMT
CMD ["apache2-foreground"]
# Fri, 06 Jan 2023 07:42:53 GMT
LABEL org.opencontainers.image.title=YOURLS
# Fri, 06 Jan 2023 07:42:57 GMT
LABEL org.opencontainers.image.description=Your Own URL Shortener
# Fri, 06 Jan 2023 07:43:00 GMT
LABEL org.opencontainers.image.url=https://yourls.org/
# Fri, 06 Jan 2023 07:43:04 GMT
LABEL org.opencontainers.image.documentation=https://yourls.org/
# Fri, 06 Jan 2023 07:43:08 GMT
LABEL org.opencontainers.image.vendor=YOURLS Org
# Fri, 06 Jan 2023 07:43:11 GMT
LABEL org.opencontainers.image.authors=YOURLS
# Fri, 06 Jan 2023 07:43:15 GMT
LABEL org.opencontainers.image.licenses=MIT
# Fri, 06 Jan 2023 07:43:19 GMT
LABEL io.artifacthub.package.readme-url=https://raw.githubusercontent.com/YOURLS/YOURLS/master/README.md
# Fri, 06 Jan 2023 07:44:25 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli
# Fri, 06 Jan 2023 07:44:31 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 06 Jan 2023 07:44:37 GMT
RUN a2enmod rewrite expires
# Fri, 06 Jan 2023 07:44:40 GMT
ARG YOURLS_VERSION=1.9.1
# Fri, 06 Jan 2023 07:44:44 GMT
ARG YOURLS_SHA256=0bf53290e8f86ea2e0121aac70f7c64d70d3dfb54823acb9dcc343dd7c5f455a
# Fri, 06 Jan 2023 07:44:48 GMT
LABEL org.opencontainers.image.version=1.9.1
# Fri, 06 Jan 2023 07:44:51 GMT
ENV YOURLS_VERSION=1.9.1
# Fri, 06 Jan 2023 07:44:55 GMT
ENV YOURLS_SHA256=0bf53290e8f86ea2e0121aac70f7c64d70d3dfb54823acb9dcc343dd7c5f455a
# Fri, 06 Jan 2023 07:45:05 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Fri, 06 Jan 2023 07:45:08 GMT
COPY --chown=www-data:www-datafile:f5584b9849b80034920f4de5f1297cb1be461f765f3437b87ddf6c86daa6499d in /usr/src/yourls/user/ 
# Fri, 06 Jan 2023 07:45:11 GMT
COPY file:975ababf859e7cabd8184ab0b2b317a5d8d3ccb6f4922be7f2a5d28c20d075a2 in /usr/local/bin/ 
# Fri, 06 Jan 2023 07:45:14 GMT
COPY file:5b7ff05d0c98ad759c4bec0ef8a7ce74cae42e95b42564b55f43b341c2c3e3f5 in /usr/src/yourls/ 
# Fri, 06 Jan 2023 07:45:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Jan 2023 07:45:21 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:5410793baaff16536eff1e5ac655d98039bd44f581c42d6ceb254202d1196477`  
		Last Modified: Wed, 21 Dec 2022 01:18:42 GMT  
		Size: 29.6 MB (29619894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f5a270b32df097d661fbe270a470bd35c56224b48f850e9b1036002daac3603`  
		Last Modified: Wed, 21 Dec 2022 19:51:26 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da4b98b0b273d18374f1846d0509aa5d94de35bdc7c06ac5e4aae4f1f1e37563`  
		Last Modified: Wed, 21 Dec 2022 19:52:20 GMT  
		Size: 72.0 MB (72018901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be37e23167f53c12ded8f61dc0467a44c241de238ea984bb317dac2e030fc1a5`  
		Last Modified: Wed, 21 Dec 2022 19:51:26 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21ce1aea7b69a4a282c6e621feb4cadf804d42a1cd1c5cea2fad568a398d63f3`  
		Last Modified: Wed, 21 Dec 2022 19:53:00 GMT  
		Size: 18.9 MB (18940097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7129478266010b0d49c75ed4233624ffeb8685028f1c2a0f57536c16d8c53763`  
		Last Modified: Wed, 21 Dec 2022 19:52:47 GMT  
		Size: 437.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a22ce54417e8f311761b30d742fa33dc4420231121a1fd8b2021fa39c133fba`  
		Last Modified: Wed, 21 Dec 2022 19:52:46 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c8432b90af037e4cdcc7dda7c9c40b56248762e51b4c596f68058662ccfe2e5`  
		Last Modified: Fri, 06 Jan 2023 02:02:18 GMT  
		Size: 11.9 MB (11875613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac89d4fb435456ef0ec4e3b65f0e470c9a7b94d062b41b8a742c79f0869d2d07`  
		Last Modified: Fri, 06 Jan 2023 02:02:12 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba9a0cefcc12da94aa844efc6e930517c928378a34d89125acb0df4d3ff6e58`  
		Last Modified: Fri, 06 Jan 2023 02:02:21 GMT  
		Size: 10.2 MB (10195848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60d1c48b55e69b6208b5489c9e34026089b7d87e460ed03116d801a44c2b98fb`  
		Last Modified: Fri, 06 Jan 2023 02:02:12 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05072677d8fb33eb95f73f0fb8015a6a35a121ca9d9f33b72df2f7e09d1fa9ed`  
		Last Modified: Fri, 06 Jan 2023 02:02:12 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d156ec629538a873b7392208a346b6ff144aa146fd1f3cf5157c3faccb13bce`  
		Last Modified: Fri, 06 Jan 2023 02:02:12 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efebd43861b0cd47fd73158d8ea435eca419f2dc9330b72e1d969495fabc4fe7`  
		Last Modified: Fri, 06 Jan 2023 07:48:14 GMT  
		Size: 149.0 KB (148971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d02e1ddba6d5821515e016799fcac7392a116ff5d20a5e5c19065fe2771097b`  
		Last Modified: Fri, 06 Jan 2023 07:48:14 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:217bed9eb95befecaa107e7099b12496eb0129836190293783232683b7b9a93c`  
		Last Modified: Fri, 06 Jan 2023 07:48:12 GMT  
		Size: 350.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e66d85843a5926bc79458164cb28b8695e90236a52fe2a382328335cedb580e`  
		Last Modified: Fri, 06 Jan 2023 07:48:16 GMT  
		Size: 3.9 MB (3903429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:937bf36815dfb41c74985290299d37c4c9f7c02d3725cb5d7d7e2502f1bca824`  
		Last Modified: Fri, 06 Jan 2023 07:48:12 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20cb57d942bf1d3ad6c04c2c59cd74134e4efb51be4efda8c36060424d29e054`  
		Last Modified: Fri, 06 Jan 2023 07:48:12 GMT  
		Size: 1.6 KB (1556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3b66e0efec0d8365dfd4b0c562bdb2bb168ac123698a93a118230e8f72406ba`  
		Last Modified: Fri, 06 Jan 2023 07:48:12 GMT  
		Size: 335.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:apache` - linux; ppc64le

```console
$ docker pull yourls@sha256:fbdc07208911b333c9f15a341bcd1336089ef5fc746411abb60567ddfa911ef6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.0 MB (170000939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e96912975f038acc0e295e6499a19d84a2ad8326423147da4deb57ea0a927965`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 21 Dec 2022 01:17:41 GMT
ADD file:5ab731e5c1e145738476449b6b0748f44822bb2cd6c53ae5bbf6ae6bfec83383 in / 
# Wed, 21 Dec 2022 01:17:43 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:54:28 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 21 Dec 2022 02:54:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 21 Dec 2022 02:55:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:55:12 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 21 Dec 2022 02:55:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 21 Dec 2022 03:00:08 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 21 Dec 2022 03:00:08 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 21 Dec 2022 03:00:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 21 Dec 2022 03:00:31 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 21 Dec 2022 03:00:33 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 21 Dec 2022 03:00:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 21 Dec 2022 03:00:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 21 Dec 2022 03:00:34 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 21 Dec 2022 03:38:23 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 06 Jan 2023 00:07:12 GMT
ENV PHP_VERSION=8.1.14
# Fri, 06 Jan 2023 00:07:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.14.tar.xz.asc
# Fri, 06 Jan 2023 00:07:13 GMT
ENV PHP_SHA256=e16e47a872d58685913ac848ce92ec49f42c1828110c98c65fb6265a08724a1a
# Fri, 06 Jan 2023 00:07:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 06 Jan 2023 00:07:37 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 06 Jan 2023 00:11:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 06 Jan 2023 00:11:32 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Fri, 06 Jan 2023 00:11:33 GMT
RUN docker-php-ext-enable sodium
# Fri, 06 Jan 2023 00:11:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 06 Jan 2023 00:11:33 GMT
STOPSIGNAL SIGWINCH
# Fri, 06 Jan 2023 00:11:34 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 06 Jan 2023 00:11:34 GMT
WORKDIR /var/www/html
# Fri, 06 Jan 2023 00:11:34 GMT
EXPOSE 80
# Fri, 06 Jan 2023 00:11:35 GMT
CMD ["apache2-foreground"]
# Fri, 06 Jan 2023 05:53:16 GMT
LABEL org.opencontainers.image.title=YOURLS
# Fri, 06 Jan 2023 05:53:16 GMT
LABEL org.opencontainers.image.description=Your Own URL Shortener
# Fri, 06 Jan 2023 05:53:17 GMT
LABEL org.opencontainers.image.url=https://yourls.org/
# Fri, 06 Jan 2023 05:53:17 GMT
LABEL org.opencontainers.image.documentation=https://yourls.org/
# Fri, 06 Jan 2023 05:53:18 GMT
LABEL org.opencontainers.image.vendor=YOURLS Org
# Fri, 06 Jan 2023 05:53:18 GMT
LABEL org.opencontainers.image.authors=YOURLS
# Fri, 06 Jan 2023 05:53:18 GMT
LABEL org.opencontainers.image.licenses=MIT
# Fri, 06 Jan 2023 05:53:18 GMT
LABEL io.artifacthub.package.readme-url=https://raw.githubusercontent.com/YOURLS/YOURLS/master/README.md
# Fri, 06 Jan 2023 05:53:50 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli
# Fri, 06 Jan 2023 05:53:51 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 06 Jan 2023 05:53:53 GMT
RUN a2enmod rewrite expires
# Fri, 06 Jan 2023 05:53:53 GMT
ARG YOURLS_VERSION=1.9.1
# Fri, 06 Jan 2023 05:53:53 GMT
ARG YOURLS_SHA256=0bf53290e8f86ea2e0121aac70f7c64d70d3dfb54823acb9dcc343dd7c5f455a
# Fri, 06 Jan 2023 05:53:53 GMT
LABEL org.opencontainers.image.version=1.9.1
# Fri, 06 Jan 2023 05:53:54 GMT
ENV YOURLS_VERSION=1.9.1
# Fri, 06 Jan 2023 05:53:54 GMT
ENV YOURLS_SHA256=0bf53290e8f86ea2e0121aac70f7c64d70d3dfb54823acb9dcc343dd7c5f455a
# Fri, 06 Jan 2023 05:53:57 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Fri, 06 Jan 2023 05:53:57 GMT
COPY --chown=www-data:www-datafile:f5584b9849b80034920f4de5f1297cb1be461f765f3437b87ddf6c86daa6499d in /usr/src/yourls/user/ 
# Fri, 06 Jan 2023 05:53:58 GMT
COPY file:975ababf859e7cabd8184ab0b2b317a5d8d3ccb6f4922be7f2a5d28c20d075a2 in /usr/local/bin/ 
# Fri, 06 Jan 2023 05:53:58 GMT
COPY file:5b7ff05d0c98ad759c4bec0ef8a7ce74cae42e95b42564b55f43b341c2c3e3f5 in /usr/src/yourls/ 
# Fri, 06 Jan 2023 05:53:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Jan 2023 05:53:59 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:ba010cdd67bb149ba042a834d84020887fc3f8ca9d8e51b31f3104286cafb9ba`  
		Last Modified: Wed, 21 Dec 2022 01:23:22 GMT  
		Size: 35.3 MB (35268748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba7e47853cce58ab3b0e90477d33a7cba4e32fe2c4869183d5b159cc2a331137`  
		Last Modified: Wed, 21 Dec 2022 04:35:19 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2f2925c57c4227f5aaf5bfc813e2b13f014cf5db5bc7ad9f18dd4134fe67a22`  
		Last Modified: Wed, 21 Dec 2022 04:35:43 GMT  
		Size: 86.6 MB (86632961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6559957d2a1157e881884b86d6b3ad933922be2896c5787bda3c2c9442a9add8`  
		Last Modified: Wed, 21 Dec 2022 04:35:18 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56f0ad6bf5c9b9867714546e715fd3fcb027e09d7dee2efb3e590dc4969dc532`  
		Last Modified: Wed, 21 Dec 2022 04:36:20 GMT  
		Size: 20.5 MB (20464165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4410cbfb5dadcb662ff50f58fa2ca753afb440501006c1cd221a552593fab1ae`  
		Last Modified: Wed, 21 Dec 2022 04:36:15 GMT  
		Size: 480.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8e3c972f7a55a635258cdd551bd3717135cb0099cf868f969a24560e0222982`  
		Last Modified: Wed, 21 Dec 2022 04:36:15 GMT  
		Size: 515.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f02368d11a762b9d70ec99a33b014123d5900b53df6a813c60238ac9246b579`  
		Last Modified: Fri, 06 Jan 2023 01:32:42 GMT  
		Size: 12.1 MB (12093437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d42762853db726da6b6c4068983fc803ce9876f5ec7fd245147e1cec2ef8a287`  
		Last Modified: Fri, 06 Jan 2023 01:32:38 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75de8b8d6f84386ff6bc43f9bbc616a3795dd3ff224adf5675d9c1397fe68c40`  
		Last Modified: Fri, 06 Jan 2023 01:32:42 GMT  
		Size: 11.4 MB (11444073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f1328c225cd6a8bc09b5a309d6a9bfeb745fe174c5c6fc76e74a1b570ae2764`  
		Last Modified: Fri, 06 Jan 2023 01:32:38 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18faee3d70d54dd9bf5913523d2e61f6bf3d3bc61b8534bde7064da012b9f993`  
		Last Modified: Fri, 06 Jan 2023 01:32:38 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b10de95116e8a5bdc7351d6964afabe3d3094ac1fe84e94271d609ae5beb49bd`  
		Last Modified: Fri, 06 Jan 2023 01:32:38 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d35e2693891464e55eb4ebe551722af5ed63e9f8c14ffc9c740acc0a5639daad`  
		Last Modified: Fri, 06 Jan 2023 05:56:35 GMT  
		Size: 183.8 KB (183812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3ac7f2ec377510f507c6f3dc455eb29414561393d32757fcbf0691783cddef0`  
		Last Modified: Fri, 06 Jan 2023 05:56:35 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a8245f80d1ebcab51deeb68d6e5ef01dfe7036b28bdf9fd9a558b70677caffb`  
		Last Modified: Fri, 06 Jan 2023 05:56:33 GMT  
		Size: 344.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bd874cac8febec79f5160590795295fcffb7f5560b92cab5026b8ec3fc6b739`  
		Last Modified: Fri, 06 Jan 2023 05:56:34 GMT  
		Size: 3.9 MB (3903538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fab71c4214eee99020dcc17e928d43f45a1ae1f489ca50dcb41c777009f1a84`  
		Last Modified: Fri, 06 Jan 2023 05:56:33 GMT  
		Size: 2.1 KB (2053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ed803b34182af7280c81bb3dfd653b56ff06fc2f3ae417cf8749e0be80f78a6`  
		Last Modified: Fri, 06 Jan 2023 05:56:33 GMT  
		Size: 1.6 KB (1557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14365419c3373561f8bd0c194bcbee8277eb8a6ff7951b83e1adb9a1ece081d3`  
		Last Modified: Fri, 06 Jan 2023 05:56:33 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:apache` - linux; s390x

```console
$ docker pull yourls@sha256:d64a8d31f7a259a203296fa7d97f00f33145221c1293ad0643d72f2743c6fc80
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.7 MB (146676496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cedb5ad57dd08644b83765d75a37c15a734d36f28fb0c420df21d13b344f020`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 21 Dec 2022 01:43:11 GMT
ADD file:c1d41928e802c0b63beb07130c33bcc6dbdeb380a7f47510163cb176891e682a in / 
# Wed, 21 Dec 2022 01:43:14 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 08:46:41 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 21 Dec 2022 08:46:42 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 21 Dec 2022 08:47:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 08:47:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 21 Dec 2022 08:47:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 21 Dec 2022 08:50:31 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 21 Dec 2022 08:50:32 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 21 Dec 2022 08:50:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 21 Dec 2022 08:50:48 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 21 Dec 2022 08:50:49 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 21 Dec 2022 08:50:50 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 21 Dec 2022 08:50:50 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 21 Dec 2022 08:50:51 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 21 Dec 2022 09:22:45 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 06 Jan 2023 00:31:50 GMT
ENV PHP_VERSION=8.1.14
# Fri, 06 Jan 2023 00:31:50 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.14.tar.xz.asc
# Fri, 06 Jan 2023 00:31:50 GMT
ENV PHP_SHA256=e16e47a872d58685913ac848ce92ec49f42c1828110c98c65fb6265a08724a1a
# Fri, 06 Jan 2023 00:32:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 06 Jan 2023 00:32:02 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 06 Jan 2023 00:36:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 06 Jan 2023 00:36:24 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Fri, 06 Jan 2023 00:36:25 GMT
RUN docker-php-ext-enable sodium
# Fri, 06 Jan 2023 00:36:26 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 06 Jan 2023 00:36:26 GMT
STOPSIGNAL SIGWINCH
# Fri, 06 Jan 2023 00:36:27 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 06 Jan 2023 00:36:27 GMT
WORKDIR /var/www/html
# Fri, 06 Jan 2023 00:36:28 GMT
EXPOSE 80
# Fri, 06 Jan 2023 00:36:29 GMT
CMD ["apache2-foreground"]
# Fri, 06 Jan 2023 04:33:45 GMT
LABEL org.opencontainers.image.title=YOURLS
# Fri, 06 Jan 2023 04:33:45 GMT
LABEL org.opencontainers.image.description=Your Own URL Shortener
# Fri, 06 Jan 2023 04:33:46 GMT
LABEL org.opencontainers.image.url=https://yourls.org/
# Fri, 06 Jan 2023 04:33:46 GMT
LABEL org.opencontainers.image.documentation=https://yourls.org/
# Fri, 06 Jan 2023 04:33:47 GMT
LABEL org.opencontainers.image.vendor=YOURLS Org
# Fri, 06 Jan 2023 04:33:47 GMT
LABEL org.opencontainers.image.authors=YOURLS
# Fri, 06 Jan 2023 04:33:48 GMT
LABEL org.opencontainers.image.licenses=MIT
# Fri, 06 Jan 2023 04:33:48 GMT
LABEL io.artifacthub.package.readme-url=https://raw.githubusercontent.com/YOURLS/YOURLS/master/README.md
# Fri, 06 Jan 2023 04:34:23 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli
# Fri, 06 Jan 2023 04:34:24 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 06 Jan 2023 04:34:26 GMT
RUN a2enmod rewrite expires
# Fri, 06 Jan 2023 04:34:26 GMT
ARG YOURLS_VERSION=1.9.1
# Fri, 06 Jan 2023 04:34:26 GMT
ARG YOURLS_SHA256=0bf53290e8f86ea2e0121aac70f7c64d70d3dfb54823acb9dcc343dd7c5f455a
# Fri, 06 Jan 2023 04:34:27 GMT
LABEL org.opencontainers.image.version=1.9.1
# Fri, 06 Jan 2023 04:34:27 GMT
ENV YOURLS_VERSION=1.9.1
# Fri, 06 Jan 2023 04:34:28 GMT
ENV YOURLS_SHA256=0bf53290e8f86ea2e0121aac70f7c64d70d3dfb54823acb9dcc343dd7c5f455a
# Fri, 06 Jan 2023 04:34:32 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Fri, 06 Jan 2023 04:34:33 GMT
COPY --chown=www-data:www-datafile:f5584b9849b80034920f4de5f1297cb1be461f765f3437b87ddf6c86daa6499d in /usr/src/yourls/user/ 
# Fri, 06 Jan 2023 04:34:33 GMT
COPY file:975ababf859e7cabd8184ab0b2b317a5d8d3ccb6f4922be7f2a5d28c20d075a2 in /usr/local/bin/ 
# Fri, 06 Jan 2023 04:34:33 GMT
COPY file:5b7ff05d0c98ad759c4bec0ef8a7ce74cae42e95b42564b55f43b341c2c3e3f5 in /usr/src/yourls/ 
# Fri, 06 Jan 2023 04:34:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Jan 2023 04:34:34 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:197dcf20f55386b4c3f5fbace4720b64b5b0b606658b4ea9925121b9dbe7d638`  
		Last Modified: Wed, 21 Dec 2022 01:49:12 GMT  
		Size: 29.6 MB (29629760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f06b0a5b87ea33b07c7e0b2ada0ffe18d1394f7d690c637918a2c779b623953`  
		Last Modified: Wed, 21 Dec 2022 10:12:39 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:330fb3f4500910897db299c8d8e47fde1212f6b8d99cf8348ed38274f551d1fa`  
		Last Modified: Wed, 21 Dec 2022 10:12:49 GMT  
		Size: 71.6 MB (71626832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a651f7097feb056709f04934684791beade995e9817cdfefdefb820880ecd9b7`  
		Last Modified: Wed, 21 Dec 2022 10:12:39 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f7f2b08f592f1c4fabf7d985370f8a6cbf0042795a700a4d61fda53640c0e41`  
		Last Modified: Wed, 21 Dec 2022 10:13:12 GMT  
		Size: 19.1 MB (19072275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45030a51aec28e95687fa4bf504ef17a2811e336740fb00acd5170bcead75a96`  
		Last Modified: Wed, 21 Dec 2022 10:13:09 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:469270d1ecee84ea56fc6d10fa3de3a08104fe99e945c6fa317d56b4987a0ebf`  
		Last Modified: Wed, 21 Dec 2022 10:13:09 GMT  
		Size: 513.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa830ff2180002cff2a3f4aad4b4e6fbab831517841f04d01a515ef7d57349c0`  
		Last Modified: Fri, 06 Jan 2023 01:57:06 GMT  
		Size: 12.1 MB (12092614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3077f3d45579ab272639031f98c249f20e027740fb2c023ead3b34ff0159dba4`  
		Last Modified: Fri, 06 Jan 2023 01:57:04 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75ec1720e3ffc9f2288eb10ef85904860819921254c9dbc55f1690bf4815c608`  
		Last Modified: Fri, 06 Jan 2023 01:57:06 GMT  
		Size: 10.2 MB (10183030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ebccc1696d07abb739163bdb9310598c17da14025372cbd1a637c0abe09f11f`  
		Last Modified: Fri, 06 Jan 2023 01:57:04 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43857725bba8da4fe06e577630ec9aa9f5d462b788048428428e7785a4ddc6fd`  
		Last Modified: Fri, 06 Jan 2023 01:57:04 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb01566fca97050d1639886842e8a2293c2909f129b712e4eaf152042d73225a`  
		Last Modified: Fri, 06 Jan 2023 01:57:04 GMT  
		Size: 897.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d580d97bda040222be4539d1c791b59e9a78cc50af645f38645893b67abc610`  
		Last Modified: Fri, 06 Jan 2023 04:37:28 GMT  
		Size: 158.2 KB (158234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:810e058af7b762a6d21c5ae432e97ca97ebcef37212d65ceccb68836cd6e3688`  
		Last Modified: Fri, 06 Jan 2023 04:37:28 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afbad88a6a4d487057be5ba90c428ce95b0e4985653d33ad44b9de3d916d5b7f`  
		Last Modified: Fri, 06 Jan 2023 04:37:27 GMT  
		Size: 350.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42d660fdee38aff7ab7635d23a815889e6cb36f97e0c64271d82761ea274b58b`  
		Last Modified: Fri, 06 Jan 2023 04:37:27 GMT  
		Size: 3.9 MB (3903534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b951ac95d3026c1eaefe1a6ac25c7443e01f8b27045315854f8ada5dbc1bb117`  
		Last Modified: Fri, 06 Jan 2023 04:37:27 GMT  
		Size: 2.1 KB (2055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f20e1214cb4f5a3c09078f263d215f982d47553ea9cb548734c2be31d77c2b2e`  
		Last Modified: Fri, 06 Jan 2023 04:37:27 GMT  
		Size: 1.6 KB (1555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b022026412b7c7b16b8f67a7ca37fb572251af75d0ccc030bc916a5263489d8f`  
		Last Modified: Fri, 06 Jan 2023 04:37:26 GMT  
		Size: 335.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
