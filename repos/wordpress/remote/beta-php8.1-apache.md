## `wordpress:beta-php8.1-apache`

```console
$ docker pull wordpress@sha256:92fe62fa202f75cef03eb2db070fb6ba1fa14e21d436beb4fc74bf5de1b8733e
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

### `wordpress:beta-php8.1-apache` - linux; amd64

```console
$ docker pull wordpress@sha256:ae24b7e4237280db4188d45557fd5175da21430230de190973085d3d82b3dffc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.5 MB (257512076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:632bb144231deb2a18a4be5a34c5a1f6f90ff3874a483ba34d7660b5d9fb8a52`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:32 GMT
ADD file:a9a95cfab16803be03e59ade41622ef5061cf90f2d034304fe4ac1ee9ff30389 in / 
# Fri, 27 Sep 2024 04:29:32 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:40:06 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Fri, 27 Sep 2024 05:40:06 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 27 Sep 2024 05:40:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:40:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 27 Sep 2024 05:40:25 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Fri, 27 Sep 2024 05:44:30 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 27 Sep 2024 05:44:30 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 27 Sep 2024 05:44:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Fri, 27 Sep 2024 05:44:38 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Fri, 27 Sep 2024 05:44:39 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Fri, 27 Sep 2024 05:44:39 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Sep 2024 05:44:39 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Sep 2024 05:44:39 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 27 Sep 2024 07:14:06 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 27 Sep 2024 07:14:06 GMT
ENV PHP_VERSION=8.1.30
# Fri, 27 Sep 2024 07:14:06 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.30.tar.xz.asc
# Fri, 27 Sep 2024 07:14:06 GMT
ENV PHP_SHA256=f24a6007f0b25a53cb7fbaee69c85017e0345b62089c2425a0afb7e177192ed1
# Fri, 27 Sep 2024 07:14:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 27 Sep 2024 07:14:16 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 27 Sep 2024 07:17:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 27 Sep 2024 07:17:50 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Fri, 27 Sep 2024 07:17:50 GMT
RUN docker-php-ext-enable sodium
# Fri, 27 Sep 2024 07:17:50 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 27 Sep 2024 07:17:50 GMT
STOPSIGNAL SIGWINCH
# Fri, 27 Sep 2024 07:17:50 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 27 Sep 2024 07:17:51 GMT
WORKDIR /var/www/html
# Fri, 27 Sep 2024 07:17:51 GMT
EXPOSE 80
# Fri, 27 Sep 2024 07:17:51 GMT
CMD ["apache2-foreground"]
# Tue, 01 Oct 2024 07:26:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Oct 2024 07:26:35 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 01 Oct 2024 07:26:35 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 01 Oct 2024 07:26:35 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 01 Oct 2024 07:26:35 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Tue, 01 Oct 2024 07:26:35 GMT
RUN set -eux; 	version='6.7-beta1'; 	sha1='5425031b02d6917ae8fb357d7453a96c215e6f5a'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 01 Oct 2024 07:26:35 GMT
VOLUME [/var/www/html]
# Tue, 01 Oct 2024 07:26:35 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 01 Oct 2024 07:26:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Oct 2024 07:26:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Oct 2024 07:26:35 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab`  
		Last Modified: Fri, 27 Sep 2024 04:33:11 GMT  
		Size: 29.1 MB (29126276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07fc0890b857ec241446d5da032bf36da2a006ce8868ba150a76a1ee16772b39`  
		Last Modified: Fri, 27 Sep 2024 07:40:54 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:141aa7d58c576d5efbf995cfdd139044be15add60b2f0e5f7b295fdc4cc511d3`  
		Last Modified: Fri, 27 Sep 2024 07:41:08 GMT  
		Size: 104.3 MB (104345685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2720d4bca8b3db19acbea04618296e463e4cde1df16c277954505ad4e50893eb`  
		Last Modified: Fri, 27 Sep 2024 07:40:54 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82deca51468c5fb0464e6db26d14da0d5605682524cb4acfafbbc7cc55a2b20e`  
		Last Modified: Fri, 27 Sep 2024 07:41:32 GMT  
		Size: 20.3 MB (20327579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dec741dfa52689fcf27c3934a0b87bdaefb62c643d04fe352f88589f791315e9`  
		Last Modified: Fri, 27 Sep 2024 07:41:29 GMT  
		Size: 437.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e204b0efab9499a1608734207890fb199b60d100af89f57dc74f1ca26a00f8d5`  
		Last Modified: Fri, 27 Sep 2024 07:41:29 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da3427d4ab01d78991b04f53d5c5bdc37e084ea50769ce9eff9452f0592a5226`  
		Last Modified: Fri, 27 Sep 2024 07:49:23 GMT  
		Size: 12.2 MB (12183478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75c32fd90f5c9f3e8170ecd62580890f28aed26cfa08f51a02476fba95d150d3`  
		Last Modified: Fri, 27 Sep 2024 07:49:20 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea57467a10b99b7aa65f65ac913b02a35b4e917e92cdcc89609ad6e55e5cf103`  
		Last Modified: Fri, 27 Sep 2024 07:49:22 GMT  
		Size: 11.2 MB (11155427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56c9d963ab4007b6a878512836854f5b6d2de2021d668d85fc5974abc6aecf6b`  
		Last Modified: Fri, 27 Sep 2024 07:49:20 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f772313021358e3d78b26d5a9a38c793c3d9ddfe1b9467ebb95b12e810c6286`  
		Last Modified: Fri, 27 Sep 2024 07:49:20 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2f5f2697bee1d53945c239318e1326770d58a121065168fdcc59e42b77db2fa`  
		Last Modified: Fri, 27 Sep 2024 07:49:20 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feaca3488fd20939674e135424f090f64dca8eb913a12df13b03dd21d9668ace`  
		Last Modified: Tue, 01 Oct 2024 22:24:30 GMT  
		Size: 26.3 MB (26255197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e5aa8da0927017417734031ada06d5472f5ac2d0585839a7e962a598f06d22a`  
		Last Modified: Tue, 01 Oct 2024 22:24:30 GMT  
		Size: 17.4 MB (17441659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bbfb10d2918cabd8c6f2a00c1f5836b9e92b11e00e7ecac80eef4c856253750`  
		Last Modified: Tue, 01 Oct 2024 22:24:30 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1391be8d39404eb11b6c996d943140ac693ead649387fe16966cc921e1d9c58`  
		Last Modified: Tue, 01 Oct 2024 22:24:30 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:802ec9105923e610e9ee7afffb7662f398c2f292d1ccc5d664350867599f6f15`  
		Last Modified: Tue, 01 Oct 2024 22:24:31 GMT  
		Size: 19.2 KB (19175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ff309e46085de14f9d39dd69d7c24a4124e0ae49ff54fd248e44ae9b277351`  
		Last Modified: Tue, 01 Oct 2024 22:24:31 GMT  
		Size: 36.6 MB (36647221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1d977915f357b5362e146e88b8d6d49f3880d5d40ac4d96107eebb6f4c77aae`  
		Last Modified: Tue, 01 Oct 2024 22:24:31 GMT  
		Size: 2.4 KB (2435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bcd4271518dd54522832bb67233255bb1ce983673770fe27c55421a59cd1d95`  
		Last Modified: Tue, 01 Oct 2024 22:24:31 GMT  
		Size: 1.7 KB (1726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-php8.1-apache` - unknown; unknown

```console
$ docker pull wordpress@sha256:e67112f2b172c5f2af56d1289b97a35b62a4feb29e4a512fc82dbdbde6e4c25f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8151932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91702dc97ebd21dee165d20b90f768df6af1a091bfcd1b3dd157df3e3ae21740`

```dockerfile
```

-	Layers:
	-	`sha256:f57666fa4a17686a9b508499936cafb12484c11f09cf069c7aae53824c78b757`  
		Last Modified: Tue, 01 Oct 2024 22:24:30 GMT  
		Size: 8.1 MB (8092101 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb8ecee401a9a82179dfe0324c2a0ca4cf99e39b30017018346e8de534d15c3d`  
		Last Modified: Tue, 01 Oct 2024 22:24:30 GMT  
		Size: 59.8 KB (59831 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-php8.1-apache` - linux; arm variant v5

```console
$ docker pull wordpress@sha256:b54ba17b956ce5f7937ea213e5a15f439135d01b3679a1c462e8c949cb89d1d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.4 MB (226408817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d3ce6b22d222cfc730b6d57df49595899108bf925f09b571c67da69d77cc4bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 27 Sep 2024 03:19:20 GMT
ADD file:91b876c600b7d3198bc98296224f6861440f56fcbd15a2188c95a8785b94061a in / 
# Fri, 27 Sep 2024 03:19:20 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 04:06:51 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Fri, 27 Sep 2024 04:06:51 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 27 Sep 2024 04:07:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 04:07:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 27 Sep 2024 04:07:15 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Fri, 27 Sep 2024 04:10:28 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 27 Sep 2024 04:10:28 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 27 Sep 2024 04:10:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Fri, 27 Sep 2024 04:10:42 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Fri, 27 Sep 2024 04:10:43 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Fri, 27 Sep 2024 04:10:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Sep 2024 04:10:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Sep 2024 04:10:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 27 Sep 2024 04:47:55 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 27 Sep 2024 04:47:55 GMT
ENV PHP_VERSION=8.1.30
# Fri, 27 Sep 2024 04:47:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.30.tar.xz.asc
# Fri, 27 Sep 2024 04:47:55 GMT
ENV PHP_SHA256=f24a6007f0b25a53cb7fbaee69c85017e0345b62089c2425a0afb7e177192ed1
# Fri, 27 Sep 2024 04:48:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 27 Sep 2024 04:48:11 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 27 Sep 2024 04:50:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 27 Sep 2024 04:50:53 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Fri, 27 Sep 2024 04:50:53 GMT
RUN docker-php-ext-enable sodium
# Fri, 27 Sep 2024 04:50:53 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 27 Sep 2024 04:50:53 GMT
STOPSIGNAL SIGWINCH
# Fri, 27 Sep 2024 04:50:53 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 27 Sep 2024 04:50:54 GMT
WORKDIR /var/www/html
# Fri, 27 Sep 2024 04:50:54 GMT
EXPOSE 80
# Fri, 27 Sep 2024 04:50:54 GMT
CMD ["apache2-foreground"]
# Tue, 01 Oct 2024 07:26:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Oct 2024 07:26:35 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 01 Oct 2024 07:26:35 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 01 Oct 2024 07:26:35 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 01 Oct 2024 07:26:35 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Tue, 01 Oct 2024 07:26:35 GMT
RUN set -eux; 	version='6.7-beta1'; 	sha1='5425031b02d6917ae8fb357d7453a96c215e6f5a'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 01 Oct 2024 07:26:35 GMT
VOLUME [/var/www/html]
# Tue, 01 Oct 2024 07:26:35 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 01 Oct 2024 07:26:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Oct 2024 07:26:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Oct 2024 07:26:35 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:75a20c44e8becd141ba586ea413a1649251437a207502d4f8ad23d208f013e60`  
		Last Modified: Fri, 27 Sep 2024 03:21:44 GMT  
		Size: 26.9 MB (26887302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4abee9b0737593e9835dc555292a01c58c3fb19f389ffbb556e3ec83d8222c6`  
		Last Modified: Fri, 27 Sep 2024 04:57:48 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36e5de77c609405dc64f2e8c8206bbec62da53ccc60aedc603672b7a337a412b`  
		Last Modified: Fri, 27 Sep 2024 04:58:03 GMT  
		Size: 82.0 MB (81995092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ddddd6ae7c7fda37305d6bc5117d36ac423f550ff4c6ad424d1de53e6b2a1e0`  
		Last Modified: Fri, 27 Sep 2024 04:57:48 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deccef66bda4d8995be278ceb309f484f6a52595d369da981611dc922e98e887`  
		Last Modified: Fri, 27 Sep 2024 04:58:27 GMT  
		Size: 19.6 MB (19624329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20f63ad9166a15b4f481cc55af64fe92ea1c78d1a77d1d9d16f34bf495afdfae`  
		Last Modified: Fri, 27 Sep 2024 04:58:23 GMT  
		Size: 438.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5517924e644a07b5b6ba20a6189dc63a69c99f73da7e8bdb535bfaccaa37d098`  
		Last Modified: Fri, 27 Sep 2024 04:58:23 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2da8bbc94cc6d9c9a8507c804ba9a062f7a10621dc6e12342a7285c40089e14`  
		Last Modified: Fri, 27 Sep 2024 05:03:02 GMT  
		Size: 12.2 MB (12181585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfaaaaf79b932ff94b395318d78e4ecbe1c64f7640731dce335dd7a4330630e9`  
		Last Modified: Fri, 27 Sep 2024 05:02:59 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37986c6e22596aea4fa7022795f5a31570c93642e5e93703e3a3acb921a7207e`  
		Last Modified: Fri, 27 Sep 2024 05:03:01 GMT  
		Size: 10.1 MB (10118961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01328ae7c7e30d302c17fa00a77b1a6dbcc3322ce9f9a0352e8f2cd2ea7b201f`  
		Last Modified: Fri, 27 Sep 2024 05:02:59 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dc0ac5e4ac06936d6db3fcbd81c9cd409f80aece82d884719b0dc8f39403a55`  
		Last Modified: Fri, 27 Sep 2024 05:02:59 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc2ccbe79e9e54188682a951e55b121344ec5e844dcbe1fe783fffc0fd12dbc`  
		Last Modified: Fri, 27 Sep 2024 05:02:59 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af6686befdefda56c2ef9b98171afc940f1dbea542be1930926a78a8dfce56bb`  
		Last Modified: Fri, 27 Sep 2024 16:36:51 GMT  
		Size: 25.7 MB (25705984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ff72dc898d47303947f5e65aea79b1d30f77df047f29c8e89a592364527867`  
		Last Modified: Fri, 27 Sep 2024 16:36:51 GMT  
		Size: 13.2 MB (13218799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e4e23ee2d61b4a199eec0f219d9fc81764008fad3f1937ea78cd6036e42f863`  
		Last Modified: Fri, 27 Sep 2024 16:36:50 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bd84f829546b87787cdce6eaa9492b3f4e75e95a732d356bb210431eb45352f`  
		Last Modified: Fri, 27 Sep 2024 16:36:50 GMT  
		Size: 391.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aa6607e7928c7ee166696e1edaa482189689cf8f8fa9d3777129397c746f945`  
		Last Modified: Fri, 27 Sep 2024 16:36:51 GMT  
		Size: 19.2 KB (19161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eff8b9f28744506057a2950fe53250aea306a48f2731aa299449b757e472f89`  
		Last Modified: Tue, 01 Oct 2024 23:28:20 GMT  
		Size: 36.6 MB (36647223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:826e1a6efd41756e828288e3a786db77e274cada67eca7c5c4b5e1c3001e86ce`  
		Last Modified: Tue, 01 Oct 2024 23:28:19 GMT  
		Size: 2.4 KB (2431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72b6275d723d699b8183ae7e65be06838f584d1956cc4436f04eb66104092985`  
		Last Modified: Tue, 01 Oct 2024 23:28:19 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-php8.1-apache` - unknown; unknown

```console
$ docker pull wordpress@sha256:d912a166cdd2e5723044cec3ccdf6a0fdbd299e8fc8d740a5db61fe41b818093
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7958768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5a567fa9c78692f5d6384ebdf4ca9748e76c01f8b75ee8f2cf040aa6e814d9e`

```dockerfile
```

-	Layers:
	-	`sha256:6250742aeec7c004ddaec925c9bc86fd2cb58e35d6e7ea2824f1f5e58467bcb0`  
		Last Modified: Tue, 01 Oct 2024 23:28:19 GMT  
		Size: 7.9 MB (7898725 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fdf3de3a9cd6d54923fa15fd0239a7986d6854fe2ae00ad93a388fe0663eec2`  
		Last Modified: Tue, 01 Oct 2024 23:28:18 GMT  
		Size: 60.0 KB (60043 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-php8.1-apache` - linux; arm variant v7

```console
$ docker pull wordpress@sha256:c1559d3459a834882a5d3c4b8f38eb52dfaa3d8802b10d36c40dd2382feb8ddd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.2 MB (200187234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bec18736fc4c6b2fd7be7d2180b58ca6e974d899c75b12d174e0774c73c9b6bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 04 Sep 2024 19:03:11 GMT
ADD file:90772cdf7913d0ef1bf41e513a6205fa3195a1583476a536ec770e8381f77ac1 in / 
# Wed, 04 Sep 2024 19:03:11 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 04 Sep 2024 19:03:11 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 19:03:11 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 04 Sep 2024 19:03:11 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 04 Sep 2024 19:03:11 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 04 Sep 2024 19:03:11 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 04 Sep 2024 19:03:11 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 04 Sep 2024 19:03:11 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 04 Sep 2024 19:03:11 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 04 Sep 2024 19:03:11 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 04 Sep 2024 19:03:11 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 04 Sep 2024 19:03:11 GMT
ENV PHP_VERSION=8.1.29
# Wed, 04 Sep 2024 19:03:11 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.29.tar.xz.asc
# Wed, 04 Sep 2024 19:03:11 GMT
ENV PHP_SHA256=288884af60581d4284baba2ace9ca6d646f72facbd3e3c2dd2acc7fe6f903536
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 04 Sep 2024 19:03:11 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 04 Sep 2024 19:03:11 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 04 Sep 2024 19:03:11 GMT
RUN docker-php-ext-enable sodium
# Wed, 04 Sep 2024 19:03:11 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 04 Sep 2024 19:03:11 GMT
STOPSIGNAL SIGWINCH
# Wed, 04 Sep 2024 19:03:11 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 04 Sep 2024 19:03:11 GMT
WORKDIR /var/www/html
# Wed, 04 Sep 2024 19:03:11 GMT
EXPOSE 80
# Wed, 04 Sep 2024 19:03:11 GMT
CMD ["apache2-foreground"]
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 04 Sep 2024 19:03:11 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 	version='6.6.2-RC1'; 	sha1='bd7048a400d418783114485589f16ce8d96b25f2'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Wed, 04 Sep 2024 19:03:11 GMT
VOLUME [/var/www/html]
# Wed, 04 Sep 2024 19:03:11 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Wed, 04 Sep 2024 19:03:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 04 Sep 2024 19:03:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 04 Sep 2024 19:03:11 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:670631d7a00e03a2701d6b6aff29204afdeff4cd2da308462d92f5743156ede1`  
		Last Modified: Wed, 04 Sep 2024 22:01:44 GMT  
		Size: 24.7 MB (24718265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52af8d0fa86c9b158af0ab781cb65e065749146b3fe2c329cb4e9d0af8b14067`  
		Last Modified: Thu, 05 Sep 2024 00:26:44 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1ecdfb85b1e01962d1365bfe3926bbbfe42185d9c8b60d0930000a9db914c4f`  
		Last Modified: Thu, 05 Sep 2024 00:26:57 GMT  
		Size: 76.2 MB (76163311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:860c94c7af381cee44c718f3a335927de4a439a9ae12847fc214772a3860cd10`  
		Last Modified: Thu, 05 Sep 2024 00:26:44 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cae1097b4dec4fa4f7c19f8af46ce5d5a11f166910ab19a3f03481dcbf2c05d1`  
		Last Modified: Thu, 05 Sep 2024 00:27:21 GMT  
		Size: 19.1 MB (19065552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:058c6166ff928aaba746c5eed7f88c59d3291587055d2c72a797d2822575c866`  
		Last Modified: Thu, 05 Sep 2024 00:27:18 GMT  
		Size: 437.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5148041e15e73d623fd28b30026d084e8ab19285799c3ea4739efeabdbb429c4`  
		Last Modified: Thu, 05 Sep 2024 00:27:18 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adba8d6d7fc727ed621c075d07a47ffeb6a440edc4600ec95746f4fbe8dc6ed1`  
		Last Modified: Thu, 05 Sep 2024 00:35:29 GMT  
		Size: 12.2 MB (12157492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8641214d5e3ca4107985d0fcecbb6fec08b75eafc0a7378313d2cdae85826068`  
		Last Modified: Thu, 05 Sep 2024 00:35:25 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:706911532f5f3999ae50050ab1170f8d9e60c86e047e104a5b8d48783d21a066`  
		Last Modified: Thu, 05 Sep 2024 00:35:28 GMT  
		Size: 9.6 MB (9583383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8be06055cc9ee4e5949d74d4bf948a8a803155509b724467ca8b903202a272ee`  
		Last Modified: Thu, 05 Sep 2024 00:35:25 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44c749bbef9b21a50ffc2eb805c18284196379886f00696779f4d21ae2662d9a`  
		Last Modified: Thu, 05 Sep 2024 00:35:25 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:946af6261b0a01d4eca0e16ad21696667f1f54b6e322b0b2c3ddf139479852c8`  
		Last Modified: Thu, 05 Sep 2024 00:35:25 GMT  
		Size: 896.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3549c7a4e85d30c6252b1376ff59416a2064bc6a861f1adc19b5153b170a9d6`  
		Last Modified: Fri, 06 Sep 2024 04:17:51 GMT  
		Size: 25.1 MB (25074018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7309119468b365d892e9ff50c9a51c8ae78dabed77604004adae309ec0cdcd8`  
		Last Modified: Fri, 06 Sep 2024 04:17:50 GMT  
		Size: 8.9 MB (8931215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaac1280ac934fc3c05b61b05e0a3a4fd4cbf018b6d97de987689d8727bdcb07`  
		Last Modified: Fri, 06 Sep 2024 04:17:50 GMT  
		Size: 357.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6da4d5c2dd8ce1b5ba504f13dc78d742ed92d1c85862acdb930e785b02bfa4d`  
		Last Modified: Fri, 06 Sep 2024 04:17:50 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a48632ae13282fd6216b53d8b4865d725b6382dfcb22fe7384ab56b88ace6c8`  
		Last Modified: Fri, 06 Sep 2024 04:17:51 GMT  
		Size: 19.2 KB (19159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a4931ae50cbe574f73ef540634f69b177ccb46399356387cc56a195eda0c115`  
		Last Modified: Fri, 06 Sep 2024 05:44:00 GMT  
		Size: 24.5 MB (24464542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e2935da0f9ec7083ec4b2f904d8e2e1dabb29942fba1f151e0337e9184b41d5`  
		Last Modified: Fri, 06 Sep 2024 05:43:59 GMT  
		Size: 2.4 KB (2350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f568e37212c19afac44809cb9bbcec6e02b4701af62931dd76bfd361cf8766db`  
		Last Modified: Fri, 06 Sep 2024 05:44:00 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-php8.1-apache` - unknown; unknown

```console
$ docker pull wordpress@sha256:1f3d584d8ef88630862dc97064efcada7d9a26ce7e6722dddecd80b3eb60fc94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7878887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eb4d13033b02ae771714e4ce83246f3c1ce07a27450e244d3b4e69bfbf021fa`

```dockerfile
```

-	Layers:
	-	`sha256:d8d18bef19335a97040d642f14ff2fc3853b1b3d897ba6e723a45d277cee9631`  
		Last Modified: Fri, 06 Sep 2024 05:43:59 GMT  
		Size: 7.8 MB (7818342 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6e0ffa36b628253bb9d488a91967f2192ffd615706dc825225041633abcbc34`  
		Last Modified: Fri, 06 Sep 2024 05:43:59 GMT  
		Size: 60.5 KB (60545 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-php8.1-apache` - linux; arm64 variant v8

```console
$ docker pull wordpress@sha256:25589916b766aa5e95726d707af37300fa96144c49668c163653f3e20fd6730e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.5 MB (231527271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4c5cf2ededa79a9537a1ecee9d85080a13eb1894622e9e4c1e417ca04d107f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 04 Sep 2024 19:03:11 GMT
ADD file:06a1877f1e100122a40ed52ce771bfa7e2ab3d28323780f58f1e5b57c1e576f9 in / 
# Wed, 04 Sep 2024 19:03:11 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 04 Sep 2024 19:03:11 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 19:03:11 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 04 Sep 2024 19:03:11 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 04 Sep 2024 19:03:11 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 04 Sep 2024 19:03:11 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 04 Sep 2024 19:03:11 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 04 Sep 2024 19:03:11 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 04 Sep 2024 19:03:11 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 04 Sep 2024 19:03:11 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 04 Sep 2024 19:03:11 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 04 Sep 2024 19:03:11 GMT
ENV PHP_VERSION=8.1.29
# Wed, 04 Sep 2024 19:03:11 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.29.tar.xz.asc
# Wed, 04 Sep 2024 19:03:11 GMT
ENV PHP_SHA256=288884af60581d4284baba2ace9ca6d646f72facbd3e3c2dd2acc7fe6f903536
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 04 Sep 2024 19:03:11 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 04 Sep 2024 19:03:11 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 04 Sep 2024 19:03:11 GMT
RUN docker-php-ext-enable sodium
# Wed, 04 Sep 2024 19:03:11 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 04 Sep 2024 19:03:11 GMT
STOPSIGNAL SIGWINCH
# Wed, 04 Sep 2024 19:03:11 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 04 Sep 2024 19:03:11 GMT
WORKDIR /var/www/html
# Wed, 04 Sep 2024 19:03:11 GMT
EXPOSE 80
# Wed, 04 Sep 2024 19:03:11 GMT
CMD ["apache2-foreground"]
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 04 Sep 2024 19:03:11 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 	version='6.6.2-RC1'; 	sha1='bd7048a400d418783114485589f16ce8d96b25f2'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Wed, 04 Sep 2024 19:03:11 GMT
VOLUME [/var/www/html]
# Wed, 04 Sep 2024 19:03:11 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Wed, 04 Sep 2024 19:03:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 04 Sep 2024 19:03:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 04 Sep 2024 19:03:11 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:92c3b3500be621c72c7ac6432a9d8f731f145f4a1535361ffd3a304e55f7ccda`  
		Last Modified: Wed, 04 Sep 2024 21:42:36 GMT  
		Size: 29.2 MB (29156545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9125f50077837c519800d65edc67294c009e30fcc820455fbefc671b63081421`  
		Last Modified: Thu, 05 Sep 2024 00:18:28 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c15c4686903cb5bbd6cabc5447788b26574756d94e02c0952258c66bb2b4379`  
		Last Modified: Thu, 05 Sep 2024 00:18:40 GMT  
		Size: 98.1 MB (98131394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8893eb8a52e8af8365ae670e2549bcff74923def7137abb8dbd4657905297f01`  
		Last Modified: Thu, 05 Sep 2024 00:18:27 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa55da0753dad27fbf674997a6a04397736c543162afcaccd636738da352c108`  
		Last Modified: Thu, 05 Sep 2024 00:19:05 GMT  
		Size: 20.3 MB (20325421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60a3e15a12625719622136bcd7ea9d8c614ad174f11b4e5d64ee1a0e103a7c94`  
		Last Modified: Thu, 05 Sep 2024 00:19:02 GMT  
		Size: 435.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c70c9882f3f52155ce9e7d769b5539a7fdb5eeab8c65342778b58511aabe9dd3`  
		Last Modified: Thu, 05 Sep 2024 00:19:02 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6df8bc477c0b4ebcd99bf4025637668563f54849c3309613389f8851f747ccd0`  
		Last Modified: Thu, 05 Sep 2024 00:26:51 GMT  
		Size: 12.2 MB (12159054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71368ad6d04e5375760a94508d5f2bcac930d31ac8ca5e71aae02dcb2b72444f`  
		Last Modified: Thu, 05 Sep 2024 00:26:48 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a42b2a521335cd2fa30f5ae615c162522c73dc5d82548de4ca83cdfd3e712d34`  
		Last Modified: Thu, 05 Sep 2024 00:26:50 GMT  
		Size: 11.2 MB (11154472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:755d7960f72e390a428a0d15529e4724fac767ff7ac0e54b2ead95a52d5e0c2f`  
		Last Modified: Thu, 05 Sep 2024 00:26:48 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:900f27d2e1d2d6483465657a26ef8697582c839d23ae081249cfe389bd9cf7d2`  
		Last Modified: Thu, 05 Sep 2024 00:26:48 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58049867589abcac9f2348e6c1e8905ab34c66288ee702a23bbee7d62d2a9be3`  
		Last Modified: Thu, 05 Sep 2024 00:26:48 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52e31e14a95caad0780d758442c45bad7b13aff6c5f3355ae15a5bf76e29f4f9`  
		Last Modified: Thu, 05 Sep 2024 20:42:12 GMT  
		Size: 26.2 MB (26172518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d34326f2dd44db0e15c256f3ea17041c0dfbd737fdefd729c6218b012fe1fa19`  
		Last Modified: Thu, 05 Sep 2024 20:42:12 GMT  
		Size: 9.9 MB (9933878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c2d236a5bd75e67ba6fa081d522a82d304632b04b7e5433cfa364de14827918`  
		Last Modified: Thu, 05 Sep 2024 20:42:11 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:975c633ffe996ec75c5f06412435b606972dba0929ecfc91095fd50707be2588`  
		Last Modified: Thu, 05 Sep 2024 20:42:11 GMT  
		Size: 391.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d6c4bd98c9255447234bd1dd2b2183a1022754a6f1821d7fd63fba6cc4ac7b5`  
		Last Modified: Thu, 05 Sep 2024 20:42:12 GMT  
		Size: 19.2 KB (19159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98b147d58b2522e9fc1de951d0b2768e2222a07140f31788b829be05333625f9`  
		Last Modified: Fri, 06 Sep 2024 00:05:57 GMT  
		Size: 24.5 MB (24464544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d005d1ff03debba71c9b8168462b9f4245eb64c24056d7a905daf8db8247542d`  
		Last Modified: Fri, 06 Sep 2024 00:05:56 GMT  
		Size: 2.3 KB (2349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:996a0c904215f5979cccd5f5e7c13523af4f44ba87bf2e5310892d9a91494e92`  
		Last Modified: Fri, 06 Sep 2024 00:05:56 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-php8.1-apache` - unknown; unknown

```console
$ docker pull wordpress@sha256:d1721e97cc5543cc3b4c2b445db6bd11e9ab6da68e071495a6239dafcc52af3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8096764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfedd0ffa417498d9dc8973e4ababd4f9771b53633ece63f75ed82b9bc81aa49`

```dockerfile
```

-	Layers:
	-	`sha256:b150176dd2d755c151be03af328c5b1a7623d6260090c36432a3ed102644c600`  
		Last Modified: Fri, 06 Sep 2024 00:05:56 GMT  
		Size: 8.0 MB (8036017 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5845724ff7a4a42e0a38b50ef904197336a9a5c5a5aaabe31bbd0fcaa58ba8d6`  
		Last Modified: Fri, 06 Sep 2024 00:05:55 GMT  
		Size: 60.7 KB (60747 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-php8.1-apache` - linux; 386

```console
$ docker pull wordpress@sha256:b464ee7450c32817eda5e07537f790ee01f73581e4ea53965ca24052f5409f10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.9 MB (252889961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa9a05027b796b3a483953da9f3e3b32c6c2c6f984d0cb5eac3d0a64a654405c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 27 Sep 2024 07:23:00 GMT
ADD file:7ad74dd13b6c84de2920c6d09de06e914d0b78ba06ae75260d6e6ff344a4b024 in / 
# Fri, 27 Sep 2024 07:23:01 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 08:12:16 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Fri, 27 Sep 2024 08:12:16 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 27 Sep 2024 08:12:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 08:12:41 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 27 Sep 2024 08:12:42 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Fri, 27 Sep 2024 08:19:39 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 27 Sep 2024 08:19:39 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 27 Sep 2024 08:19:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Fri, 27 Sep 2024 08:19:50 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Fri, 27 Sep 2024 08:19:51 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Fri, 27 Sep 2024 08:19:51 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Sep 2024 08:19:51 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Sep 2024 08:19:51 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 27 Sep 2024 10:49:29 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 27 Sep 2024 10:49:29 GMT
ENV PHP_VERSION=8.1.30
# Fri, 27 Sep 2024 10:49:29 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.30.tar.xz.asc
# Fri, 27 Sep 2024 10:49:29 GMT
ENV PHP_SHA256=f24a6007f0b25a53cb7fbaee69c85017e0345b62089c2425a0afb7e177192ed1
# Fri, 27 Sep 2024 10:49:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 27 Sep 2024 10:49:41 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 27 Sep 2024 10:55:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 27 Sep 2024 10:55:57 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Fri, 27 Sep 2024 10:55:57 GMT
RUN docker-php-ext-enable sodium
# Fri, 27 Sep 2024 10:55:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 27 Sep 2024 10:55:58 GMT
STOPSIGNAL SIGWINCH
# Fri, 27 Sep 2024 10:55:58 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 27 Sep 2024 10:55:58 GMT
WORKDIR /var/www/html
# Fri, 27 Sep 2024 10:55:58 GMT
EXPOSE 80
# Fri, 27 Sep 2024 10:55:58 GMT
CMD ["apache2-foreground"]
# Tue, 01 Oct 2024 07:26:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Oct 2024 07:26:35 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 01 Oct 2024 07:26:35 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 01 Oct 2024 07:26:35 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 01 Oct 2024 07:26:35 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Tue, 01 Oct 2024 07:26:35 GMT
RUN set -eux; 	version='6.7-beta1'; 	sha1='5425031b02d6917ae8fb357d7453a96c215e6f5a'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 01 Oct 2024 07:26:35 GMT
VOLUME [/var/www/html]
# Tue, 01 Oct 2024 07:26:35 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 01 Oct 2024 07:26:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Oct 2024 07:26:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Oct 2024 07:26:35 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:c953524ed27d53ce5e7d4e7487137789de73f4058e96b05284eefbcae1b47c26`  
		Last Modified: Fri, 27 Sep 2024 07:27:04 GMT  
		Size: 30.1 MB (30144216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:138795898cf1de35ac46bb272c1c2476a14caa25663387836c955b1d89e2f74e`  
		Last Modified: Fri, 27 Sep 2024 11:31:40 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ec2d8cda04ca38232896364bf367b18146c275503f43c81e6298173cc87253`  
		Last Modified: Fri, 27 Sep 2024 11:32:02 GMT  
		Size: 101.5 MB (101514377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b02e654bcb676bf538ed8701ea1e8b582043bd3457c58bfc84a0010d5d901176`  
		Last Modified: Fri, 27 Sep 2024 11:31:39 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ee4662d7837b680b2cf24f465f80bcef0300f1ec9bbb06e018c3978e371c90e`  
		Last Modified: Fri, 27 Sep 2024 11:32:30 GMT  
		Size: 20.8 MB (20842963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:615b9307c3c3e45c2cfbb1dd17c4ff6c4be3f73f822dd0da5db7f24a3821eae7`  
		Last Modified: Fri, 27 Sep 2024 11:32:24 GMT  
		Size: 437.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef1d934e341d81156439ae04b7ad4f0a24a93ed31030a9ca4125ebd8a4745c0d`  
		Last Modified: Fri, 27 Sep 2024 11:32:24 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e13efb3f5bef345588c83b59f50be95586449c0fa36348dc638ba878078568d`  
		Last Modified: Fri, 27 Sep 2024 11:41:26 GMT  
		Size: 12.2 MB (12182626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dc0e45b48d78020b78e9e6ecd1693d2392ee7e0f91b2ee8060bbf2aee3fdfdb`  
		Last Modified: Fri, 27 Sep 2024 11:41:23 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc40d6741157698a63bd3ca63d9c1429aabe6deb5ccb335032a2cb57cff5a3d`  
		Last Modified: Fri, 27 Sep 2024 11:41:26 GMT  
		Size: 11.4 MB (11379767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea69ae79f2c05633437eb1178790976df38cb1331b0b79f7945218f3e6492aa4`  
		Last Modified: Fri, 27 Sep 2024 11:41:23 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2efa80983389af4bea27442eb33fd7c721282dda917807a47b3de805d4153938`  
		Last Modified: Fri, 27 Sep 2024 11:41:23 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef1c1a0b29a2dd1fb19f5426c5cade0300bc8da85109028b3b1f4b9952a25726`  
		Last Modified: Fri, 27 Sep 2024 11:41:23 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:838de9f8fcaabd1c183a88997dd4d075eb3675333668f1801d268ccca436b200`  
		Last Modified: Tue, 01 Oct 2024 22:24:37 GMT  
		Size: 26.7 MB (26696327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c76dd08ab035ddc772f8aa8d3c6fc479c009277be4face191a9ad2f223b0b2da`  
		Last Modified: Tue, 01 Oct 2024 22:24:36 GMT  
		Size: 13.5 MB (13452927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6aeff532c8aac90365fd2143b3361fe670b651d35f73075ed690de4a76b0462`  
		Last Modified: Tue, 01 Oct 2024 22:24:36 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9affd4e1889d83b04fc0fcb99a5dc130c2f9ab7d5c539ed2f560356c1109275`  
		Last Modified: Tue, 01 Oct 2024 22:24:36 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2598d875f426140400a75a35096c6b66ffd11b1216cd3362812c07eb3fcc3712`  
		Last Modified: Tue, 01 Oct 2024 22:24:37 GMT  
		Size: 19.2 KB (19161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6a1bae48e35f1439e97c1b4c4dc3a1de2948d636179eae7ad8cb7a8bdf3a27b`  
		Last Modified: Tue, 01 Oct 2024 22:24:38 GMT  
		Size: 36.6 MB (36647221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8672264c2b9ae7bdabe4ede7a9a561f2362dc22f0c6dedd081e2828d98431b04`  
		Last Modified: Tue, 01 Oct 2024 22:24:38 GMT  
		Size: 2.4 KB (2432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e2c7c3f38bb53a1f02cbe51f02b6a2abdf33c856a0dc1488fdb106d8e9dd240`  
		Last Modified: Tue, 01 Oct 2024 22:24:38 GMT  
		Size: 1.7 KB (1729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-php8.1-apache` - unknown; unknown

```console
$ docker pull wordpress@sha256:db66af2b6d6d00b59935538ee5039a4a866dc0a561d4ad5c47d424809d1a17f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8125455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af64d630e78851318006c1c95a345b0750521e633dc3226fac87f99a896adef4`

```dockerfile
```

-	Layers:
	-	`sha256:61ec89b9e27006d4c2a3b90add5da3bcde5de176d21c35c47e8751b97693500b`  
		Last Modified: Tue, 01 Oct 2024 22:24:36 GMT  
		Size: 8.1 MB (8065629 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a14427509f196dc8b80eaaf0a2237ecb3f064db06c9267a2eeec6f6b3d6eb1d`  
		Last Modified: Tue, 01 Oct 2024 22:24:35 GMT  
		Size: 59.8 KB (59826 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-php8.1-apache` - linux; mips64le

```console
$ docker pull wordpress@sha256:088073c686d835d616229cb97c6faf1cf0a285f9e060e7141c04e07c1433261c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.7 MB (227695584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f09d07fec27fbc98dc30da0163932642e1e6a83b7032020d4c86ddb8899a2f2d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 27 Sep 2024 09:03:05 GMT
ADD file:673970f358f62b6b095139e9647b41b9af839d4e01f7698755b040f471ff80b2 in / 
# Fri, 27 Sep 2024 09:03:10 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 11:12:08 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Fri, 27 Sep 2024 11:12:10 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 27 Sep 2024 11:13:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 11:14:04 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 27 Sep 2024 11:14:10 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Fri, 27 Sep 2024 11:31:46 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 27 Sep 2024 11:31:49 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 27 Sep 2024 11:32:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Fri, 27 Sep 2024 11:32:49 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Fri, 27 Sep 2024 11:32:56 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Fri, 27 Sep 2024 11:32:59 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Sep 2024 11:33:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Sep 2024 11:33:07 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 27 Sep 2024 14:51:39 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 27 Sep 2024 14:51:43 GMT
ENV PHP_VERSION=8.1.30
# Fri, 27 Sep 2024 14:51:47 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.30.tar.xz.asc
# Fri, 27 Sep 2024 14:51:51 GMT
ENV PHP_SHA256=f24a6007f0b25a53cb7fbaee69c85017e0345b62089c2425a0afb7e177192ed1
# Fri, 27 Sep 2024 14:52:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 27 Sep 2024 14:52:44 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 27 Sep 2024 15:08:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 27 Sep 2024 15:08:19 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Fri, 27 Sep 2024 15:08:26 GMT
RUN docker-php-ext-enable sodium
# Fri, 27 Sep 2024 15:08:30 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 27 Sep 2024 15:08:33 GMT
STOPSIGNAL SIGWINCH
# Fri, 27 Sep 2024 15:08:37 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 27 Sep 2024 15:08:41 GMT
WORKDIR /var/www/html
# Fri, 27 Sep 2024 15:08:44 GMT
EXPOSE 80
# Fri, 27 Sep 2024 15:08:48 GMT
CMD ["apache2-foreground"]
# Tue, 01 Oct 2024 07:26:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Oct 2024 07:26:35 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 01 Oct 2024 07:26:35 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 01 Oct 2024 07:26:35 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 01 Oct 2024 07:26:35 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Tue, 01 Oct 2024 07:26:35 GMT
RUN set -eux; 	version='6.7-beta1'; 	sha1='5425031b02d6917ae8fb357d7453a96c215e6f5a'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 01 Oct 2024 07:26:35 GMT
VOLUME [/var/www/html]
# Tue, 01 Oct 2024 07:26:35 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 01 Oct 2024 07:26:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Oct 2024 07:26:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Oct 2024 07:26:35 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:75358c79454e0fed44aa25dd323536443b4a1230fc432aa226620e470d72cf5f`  
		Last Modified: Fri, 27 Sep 2024 09:11:36 GMT  
		Size: 29.1 MB (29124858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af5bc07367e99f8b3d37849edf8598b8b8dc860c49d5da934eca00acc807d99`  
		Last Modified: Fri, 27 Sep 2024 15:41:03 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4eca0e563a9f07292b1663ae5dfa7c783cbc0a92a6ba5d05b288972fb04e775`  
		Last Modified: Fri, 27 Sep 2024 15:42:01 GMT  
		Size: 80.7 MB (80667686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9156dcf9823554c8d34a92fdc097bd66f5c019cd7aaf13a36ad10f26246aefa`  
		Last Modified: Fri, 27 Sep 2024 15:41:03 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf2b3b50cb0cb73e94fc9bacab2655b94a7220edded2a4c7eaf3e8eb5045dc3`  
		Last Modified: Fri, 27 Sep 2024 15:42:41 GMT  
		Size: 20.1 MB (20069201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f49bc3e7d6cb95e2d77d06f2542a1a0512de39fede06dd9c8ec8e9d9a338b8`  
		Last Modified: Fri, 27 Sep 2024 15:42:27 GMT  
		Size: 438.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c71ff0ef306529b5f488b2a07fc5fc7891371b193a282d1187bd2a49c611643`  
		Last Modified: Fri, 27 Sep 2024 15:42:27 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4151a8dd477bd1112dda5d8bf570874953a540e143ef6177591362c48774af0`  
		Last Modified: Fri, 27 Sep 2024 15:50:25 GMT  
		Size: 12.0 MB (11976852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e6fc2f8202ccff05f393b6086e52c668fd710b7ce455665284c6432af577c74`  
		Last Modified: Fri, 27 Sep 2024 15:50:19 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22b079734aac6e6d87d37d098c9a96ff1cf4a0cb364660e274e2911b54cf8169`  
		Last Modified: Fri, 27 Sep 2024 15:50:27 GMT  
		Size: 10.2 MB (10227981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2acd46146a0428917fcf6857b6c63d3ece219b01e069d85185d3997896eea72`  
		Last Modified: Fri, 27 Sep 2024 15:50:19 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b21566a17c5cb4a4488e377a03ac7bbd5144ac69e3ca1f7d33f2b261441707e`  
		Last Modified: Fri, 27 Sep 2024 15:50:19 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c60dd209409534717ad772292b04badb3730660f06b82c67e50b7a76c7d6affd`  
		Last Modified: Fri, 27 Sep 2024 15:50:19 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c85c44b6964c8c6acf348f2086bef3122384fe112a45d12740fe1d85816f7b4b`  
		Last Modified: Sat, 28 Sep 2024 19:47:04 GMT  
		Size: 26.0 MB (26026564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b3cb03a15a48c33dd98c59d3e20b185bd2a1e3c3f84f35fbac38afa54248568`  
		Last Modified: Sat, 28 Sep 2024 19:47:03 GMT  
		Size: 12.9 MB (12925682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bfbcf6c86c08a6f62d7fd90a9c6af12825eb74a9d753a1d1deef3e52622d986`  
		Last Modified: Sat, 28 Sep 2024 19:47:01 GMT  
		Size: 358.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:521f511804a4f8b6d278d57673a7ed00aa0cb17ebdc479cad24a13d290a290f9`  
		Last Modified: Sat, 28 Sep 2024 19:47:01 GMT  
		Size: 391.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b53319d8354f3933068685ff17654025305356cd23131ff519a0ae4ad93f84b`  
		Last Modified: Sat, 28 Sep 2024 19:47:02 GMT  
		Size: 19.2 KB (19161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47fd3b7eb101143abcf74973f09b8805c441aacffbf6c632d29b0d31250fa763`  
		Last Modified: Tue, 01 Oct 2024 22:38:51 GMT  
		Size: 36.6 MB (36647223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5031518ff7ad94d645c3c0b4654ca6046c401b8f1abe52feb29786676b5ba2d`  
		Last Modified: Tue, 01 Oct 2024 22:38:47 GMT  
		Size: 2.4 KB (2435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80d82e0c98943f9c130a901f6bd120ee6c9ad18b7700d7f776777d0735987210`  
		Last Modified: Tue, 01 Oct 2024 22:38:47 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-php8.1-apache` - unknown; unknown

```console
$ docker pull wordpress@sha256:0d914b52bf7a9870cf2affc8496821f1b4f7ee3e67a3029275370c8962ea80d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 KB (59765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0432dd5f88eed265b688500c76c12f2d9e8887e6e844018a39597580495688e`

```dockerfile
```

-	Layers:
	-	`sha256:07b57316321a4e70bb18da8aa6e7c09e7cf9250977c208627bdb7bce5940e4f4`  
		Last Modified: Tue, 01 Oct 2024 22:38:46 GMT  
		Size: 59.8 KB (59765 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-php8.1-apache` - linux; ppc64le

```console
$ docker pull wordpress@sha256:ed4ef8d2f52a7336dd8bf7a27e15a34ddb21211818776512abad8a1ba5655ee2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.7 MB (244703896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:162bacacae8240d46dee2467d0e4757a419dbfc7d658a106397755535c2fc8ca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 04 Sep 2024 19:03:11 GMT
ADD file:d83b2f8d4d3fd22a390140e3bebefb48e5f086d072ad6062f6446b4fc42ec7a8 in / 
# Wed, 04 Sep 2024 19:03:11 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 04 Sep 2024 19:03:11 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 19:03:11 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 04 Sep 2024 19:03:11 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 04 Sep 2024 19:03:11 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 04 Sep 2024 19:03:11 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 04 Sep 2024 19:03:11 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 04 Sep 2024 19:03:11 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 04 Sep 2024 19:03:11 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 04 Sep 2024 19:03:11 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 04 Sep 2024 19:03:11 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 04 Sep 2024 19:03:11 GMT
ENV PHP_VERSION=8.1.29
# Wed, 04 Sep 2024 19:03:11 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.29.tar.xz.asc
# Wed, 04 Sep 2024 19:03:11 GMT
ENV PHP_SHA256=288884af60581d4284baba2ace9ca6d646f72facbd3e3c2dd2acc7fe6f903536
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 04 Sep 2024 19:03:11 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 04 Sep 2024 19:03:11 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 04 Sep 2024 19:03:11 GMT
RUN docker-php-ext-enable sodium
# Wed, 04 Sep 2024 19:03:11 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 04 Sep 2024 19:03:11 GMT
STOPSIGNAL SIGWINCH
# Wed, 04 Sep 2024 19:03:11 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 04 Sep 2024 19:03:11 GMT
WORKDIR /var/www/html
# Wed, 04 Sep 2024 19:03:11 GMT
EXPOSE 80
# Wed, 04 Sep 2024 19:03:11 GMT
CMD ["apache2-foreground"]
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 04 Sep 2024 19:03:11 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 	version='6.6.2-RC1'; 	sha1='bd7048a400d418783114485589f16ce8d96b25f2'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Wed, 04 Sep 2024 19:03:11 GMT
VOLUME [/var/www/html]
# Wed, 04 Sep 2024 19:03:11 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Wed, 04 Sep 2024 19:03:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 04 Sep 2024 19:03:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 04 Sep 2024 19:03:11 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:f19b11698292330b7d980ed50b0141417eec298d865e0c1b305ce7a8b80b572d`  
		Last Modified: Wed, 04 Sep 2024 22:30:11 GMT  
		Size: 33.1 MB (33122358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ea9222f7ab10e7e2a9b68be641a3f942d5a7828fdd853395622a6bb1c0ce0f`  
		Last Modified: Sat, 07 Sep 2024 01:42:02 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c14aed28a8d8a0a890612409f5cac111426f3ccecc75786a57fb266d50a47a42`  
		Last Modified: Sat, 07 Sep 2024 01:42:23 GMT  
		Size: 103.3 MB (103326259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6076862523211f1e3bf09abbf03b4bc3beb2b313a114be849f608398557061d4`  
		Last Modified: Sat, 07 Sep 2024 01:42:02 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbcb6449d94292efa1b0f3f8acf720645fe8b0db81c78ce01a422c2415da0f08`  
		Last Modified: Sat, 07 Sep 2024 01:42:49 GMT  
		Size: 21.5 MB (21510317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8c2ee151e748c1ae77973207201be7e82f8613048a36819f15befa339967db4`  
		Last Modified: Sat, 07 Sep 2024 01:42:45 GMT  
		Size: 435.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81066d28556925500cf4f448448ac971d1f366021d57d2db657c78025b27ecba`  
		Last Modified: Sat, 07 Sep 2024 01:42:45 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9bd97bdab928a664badc6c229cb0d0ed4c6844e02a0384eaaef7de8b283b859`  
		Last Modified: Sat, 07 Sep 2024 01:56:19 GMT  
		Size: 12.2 MB (12158818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5238835fd7891c85a95652ee7a5a5bffd78b0f9bdb05f9230fb5fb4dab8dab3f`  
		Last Modified: Sat, 07 Sep 2024 01:56:16 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64c22530f1d2d26d8f67e4f8d90dfcef74d89bf4edf6b7011f0c8d34d93fc96d`  
		Last Modified: Sat, 07 Sep 2024 01:56:19 GMT  
		Size: 11.5 MB (11526245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dad7bf486101ae6c069b3881e25331e829337b5841dbd5c76e440295ee0dcbd`  
		Last Modified: Sat, 07 Sep 2024 01:56:16 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99f2cd3d198e015a6958d641f96c4be0886f072116297c18a9224e83416dd5fb`  
		Last Modified: Sat, 07 Sep 2024 01:56:16 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b06b62c12d16c31c9ca85b549d42954640081e73afb4e3e2ebfdccf5d1ac3017`  
		Last Modified: Sat, 07 Sep 2024 01:56:16 GMT  
		Size: 895.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:633cab97fbd20fa62da46047a35dd9a5daa3fff092cec4af45070f0136efe64d`  
		Last Modified: Sat, 07 Sep 2024 12:47:46 GMT  
		Size: 27.3 MB (27337231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c46e0888b8777ecc38ca088979e152ce75ea430f4b12c0930a4865010793d2d5`  
		Last Modified: Sat, 07 Sep 2024 12:47:45 GMT  
		Size: 11.2 MB (11228670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:039cdfc88eda3ba05a8753cd30bf5b65c7077a07039f085a8a6c2f1386d26989`  
		Last Modified: Sat, 07 Sep 2024 12:47:44 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a225501230ad4ff3a50ab2254adee5af0b7bd6f9b5eeaf7c73a791cf84e6710`  
		Last Modified: Sat, 07 Sep 2024 12:47:44 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd6f3e102482d654aaa66cec5f37999c051b7476120d00ba5634d1402e5c973d`  
		Last Modified: Sat, 07 Sep 2024 12:47:45 GMT  
		Size: 19.2 KB (19157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:842345930d4fc0e79971206cfeca766d0d5a5f27986a05067a78d985b8fcc913`  
		Last Modified: Sat, 07 Sep 2024 13:18:51 GMT  
		Size: 24.5 MB (24464537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03fa48a4b8acce437f1b2d2389edd274d2e4a30ebf3fc547b780698ab13d0955`  
		Last Modified: Sat, 07 Sep 2024 13:18:50 GMT  
		Size: 2.4 KB (2351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47c841f07169a9376db5e974ba80993067d53b854745faa358983bb3dfcbcbac`  
		Last Modified: Sat, 07 Sep 2024 13:18:50 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-php8.1-apache` - unknown; unknown

```console
$ docker pull wordpress@sha256:f7e4ade5a8680fca1283054b1c94e20c7ee6bb587217bd7f05a28ceb8bef9ec3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (8046389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84a36c56a289eb83608a7020a1dbc8b87a3ce8922d739bb57f9794746d8e71c4`

```dockerfile
```

-	Layers:
	-	`sha256:ccc6d855cf66f3451c8dd22fcf8dbc835845e792c6396f8060c7578be2606464`  
		Last Modified: Sat, 07 Sep 2024 13:18:50 GMT  
		Size: 8.0 MB (7985917 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8018e4619c0f3dc66db2b73bd2915963d482119fe9293bf9f7b1abf7f802651a`  
		Last Modified: Sat, 07 Sep 2024 13:18:49 GMT  
		Size: 60.5 KB (60472 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-php8.1-apache` - linux; s390x

```console
$ docker pull wordpress@sha256:3904138058c89ec1810214d582e3f0e2988419c3d93e610d074d7be217003850
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.8 MB (210794643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f462ce8311d6efcf66cf7b5fbae7237ef248492fb747e7215d799cd2bf2df08b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 04 Sep 2024 19:03:11 GMT
ADD file:728128617ba2b026c358eb266cd495be84354c4e5dc4ecc2953cb829190a4546 in / 
# Wed, 04 Sep 2024 19:03:11 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 04 Sep 2024 19:03:11 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 19:03:11 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 04 Sep 2024 19:03:11 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 04 Sep 2024 19:03:11 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 04 Sep 2024 19:03:11 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 04 Sep 2024 19:03:11 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 04 Sep 2024 19:03:11 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 04 Sep 2024 19:03:11 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 04 Sep 2024 19:03:11 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 04 Sep 2024 19:03:11 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 04 Sep 2024 19:03:11 GMT
ENV PHP_VERSION=8.1.29
# Wed, 04 Sep 2024 19:03:11 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.29.tar.xz.asc
# Wed, 04 Sep 2024 19:03:11 GMT
ENV PHP_SHA256=288884af60581d4284baba2ace9ca6d646f72facbd3e3c2dd2acc7fe6f903536
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 04 Sep 2024 19:03:11 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 04 Sep 2024 19:03:11 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 04 Sep 2024 19:03:11 GMT
RUN docker-php-ext-enable sodium
# Wed, 04 Sep 2024 19:03:11 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 04 Sep 2024 19:03:11 GMT
STOPSIGNAL SIGWINCH
# Wed, 04 Sep 2024 19:03:11 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 04 Sep 2024 19:03:11 GMT
WORKDIR /var/www/html
# Wed, 04 Sep 2024 19:03:11 GMT
EXPOSE 80
# Wed, 04 Sep 2024 19:03:11 GMT
CMD ["apache2-foreground"]
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 04 Sep 2024 19:03:11 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 	version='6.6.2-RC1'; 	sha1='bd7048a400d418783114485589f16ce8d96b25f2'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Wed, 04 Sep 2024 19:03:11 GMT
VOLUME [/var/www/html]
# Wed, 04 Sep 2024 19:03:11 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Wed, 04 Sep 2024 19:03:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 04 Sep 2024 19:03:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 04 Sep 2024 19:03:11 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:95fe27c895a828dc681ee4a0cbea0264c47528dad525efdb9641a375666536bd`  
		Last Modified: Wed, 04 Sep 2024 21:47:41 GMT  
		Size: 27.5 MB (27490321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f9c3e85da8b09b5b347e0de23df0ba14b87db8c71b84ff72bafeff05ac4c45d`  
		Last Modified: Wed, 04 Sep 2024 23:43:14 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2d162a779ea2f70207f50c43a8ea8a2afc36c812e56c03883aef22591b1fadd`  
		Last Modified: Wed, 04 Sep 2024 23:43:27 GMT  
		Size: 80.8 MB (80817858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d512ffc352f972eede4ede7944fbab31c430f84671da665932f51478717b92e0`  
		Last Modified: Wed, 04 Sep 2024 23:43:14 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63da7cad6f7a39f230d1e8de14363803877b8b1c89328c737be2154969bd6f8c`  
		Last Modified: Wed, 04 Sep 2024 23:43:43 GMT  
		Size: 20.1 MB (20099476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e25d89a6f279f62c6f2c2b233479dea22c0d2c23888634ff212bbda2c33066c`  
		Last Modified: Wed, 04 Sep 2024 23:43:40 GMT  
		Size: 437.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1efd0f24c30aa86b4c75e8ddb0e50a36663b9a80a3d8339de48eded5ecf46ef`  
		Last Modified: Wed, 04 Sep 2024 23:43:40 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78c87aab69585cd731ba0cbce6703da5b0ac03ddd5be5ccbe78cd37a5c8bb229`  
		Last Modified: Wed, 04 Sep 2024 23:49:10 GMT  
		Size: 12.2 MB (12157797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b7b3f54beb30faf5b5844577eaf61174138f0a6d39311d094285b609369e51b`  
		Last Modified: Wed, 04 Sep 2024 23:49:06 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c47e914ec1fa7e0ebed85c893617723034ee4227919c74f66e9bf05ebe94e8a`  
		Last Modified: Wed, 04 Sep 2024 23:49:08 GMT  
		Size: 10.4 MB (10395876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e66f21d2de16ac2e80b9af7ed9e5d206f76263368f5fd892cf48522b2df85a2`  
		Last Modified: Wed, 04 Sep 2024 23:49:06 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:788790c8a59ccddea6a0d80a3afcbd81963ec16c7aaba13406e6836f56250cd7`  
		Last Modified: Wed, 04 Sep 2024 23:49:06 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70833864b28db30205b966daa9e38c1e16aec9359e003e26b055c947e65ec8d6`  
		Last Modified: Wed, 04 Sep 2024 23:49:06 GMT  
		Size: 896.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80f5c4eb8bdc4c0900f278c298a9292329b94f3b9c90e520c1c1277143b3e138`  
		Last Modified: Fri, 06 Sep 2024 02:33:07 GMT  
		Size: 25.9 MB (25899075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6ad54cad0ed9f2dc7cd1cd69de5a4026d73761014dd6f923e4d61d607763f99`  
		Last Modified: Fri, 06 Sep 2024 02:33:07 GMT  
		Size: 9.4 MB (9440246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36cc22693466b58bdc0e02c115bdafb519e4fe92e5f5862179b3022f37283903`  
		Last Modified: Fri, 06 Sep 2024 02:33:06 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d757e919733e7a74096f0fab9ff26c39fba2d9ed021d57eb29db623aa0322ca`  
		Last Modified: Fri, 06 Sep 2024 02:33:07 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47efd7bb9b1dfaa32f0bd9a96efb45a06283501c2bbd9b690d311a3dbca1ded`  
		Last Modified: Fri, 06 Sep 2024 02:33:07 GMT  
		Size: 19.2 KB (19154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4407e2b061ee98ef3895f0dd58e1a5d860d816884958aa6e4b3f5b8d96b021c1`  
		Last Modified: Fri, 06 Sep 2024 03:55:16 GMT  
		Size: 24.5 MB (24464534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8863b3c79ecc443819952860e539020e860b9801bd4297a13480fb331a9a927d`  
		Last Modified: Fri, 06 Sep 2024 03:55:15 GMT  
		Size: 2.4 KB (2351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15a3ccf4efaec2286e4cbd58558dc265cc704ff501b17a38c0758fa35880d650`  
		Last Modified: Fri, 06 Sep 2024 03:55:15 GMT  
		Size: 1.7 KB (1729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-php8.1-apache` - unknown; unknown

```console
$ docker pull wordpress@sha256:a537846930bd1d4159929ba96fb86586935beb9bdde3976428d632f2a593a912
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7898375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:045dfd24b52d54111c52f4dffdf035cfb777cba1b81d19c4bf4367dc9a8abe43`

```dockerfile
```

-	Layers:
	-	`sha256:b3bc58eb3c348b514cfb495735ff3e20270e131b6ac7fde17a303c91625020f7`  
		Last Modified: Fri, 06 Sep 2024 03:55:15 GMT  
		Size: 7.8 MB (7838003 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0815e9c788dd4a23d4e67712926afa306f5dbec8802e954af326e5db9eda055`  
		Last Modified: Fri, 06 Sep 2024 03:55:15 GMT  
		Size: 60.4 KB (60372 bytes)  
		MIME: application/vnd.in-toto+json
