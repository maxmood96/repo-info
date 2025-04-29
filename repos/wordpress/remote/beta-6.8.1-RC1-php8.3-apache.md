## `wordpress:beta-6.8.1-RC1-php8.3-apache`

```console
$ docker pull wordpress@sha256:a08ad30d574831202620cb2986b04a13cf73d0b10d3630d7471ff55e793bcb7d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `wordpress:beta-6.8.1-RC1-php8.3-apache` - linux; amd64

```console
$ docker pull wordpress@sha256:b4639d3f337453a4da8e49a697f51ddf92dfe4c24cb3ada2838e8477fa6eeb2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.2 MB (248216423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e4791124bcf5e2a420f72d63f1c1c19de61028fdfa6de15d8ab3c46be0e1d47`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 10 Apr 2025 18:46:32 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Thu, 10 Apr 2025 18:46:32 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 10 Apr 2025 18:46:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 10 Apr 2025 18:46:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Apr 2025 18:46:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 10 Apr 2025 18:46:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 10 Apr 2025 18:46:32 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 10 Apr 2025 18:46:32 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 10 Apr 2025 18:46:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 10 Apr 2025 18:46:32 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 10 Apr 2025 18:46:32 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 10 Apr 2025 18:46:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 10 Apr 2025 18:46:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 10 Apr 2025 18:46:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 10 Apr 2025 18:46:32 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 10 Apr 2025 18:46:32 GMT
ENV PHP_VERSION=8.3.20
# Thu, 10 Apr 2025 18:46:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.20.tar.xz.asc
# Thu, 10 Apr 2025 18:46:32 GMT
ENV PHP_SHA256=f15914e071b5bddaf1475b5f2ba68107e8b8846655f9e89690fb7cd410b0db6c
# Thu, 10 Apr 2025 18:46:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 10 Apr 2025 18:46:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 10 Apr 2025 18:46:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 10 Apr 2025 18:46:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 10 Apr 2025 18:46:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 10 Apr 2025 18:46:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 10 Apr 2025 18:46:32 GMT
STOPSIGNAL SIGWINCH
# Thu, 10 Apr 2025 18:46:32 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 10 Apr 2025 18:46:32 GMT
WORKDIR /var/www/html
# Thu, 10 Apr 2025 18:46:32 GMT
EXPOSE map[80/tcp:{}]
# Thu, 10 Apr 2025 18:46:32 GMT
CMD ["apache2-foreground"]
# Mon, 28 Apr 2025 19:03:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Apr 2025 19:03:12 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Mon, 28 Apr 2025 19:03:12 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Mon, 28 Apr 2025 19:03:12 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Mon, 28 Apr 2025 19:03:12 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Mon, 28 Apr 2025 19:03:12 GMT
RUN set -eux; 	version='6.8.1-RC1'; 	sha1='1c8d27d51ece5b56aa511eaaf0ceef26617a254b'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Mon, 28 Apr 2025 19:03:12 GMT
VOLUME [/var/www/html]
# Mon, 28 Apr 2025 19:03:12 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Mon, 28 Apr 2025 19:03:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 28 Apr 2025 19:03:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 28 Apr 2025 19:03:12 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Mon, 28 Apr 2025 21:08:01 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7342773645e17421c0bdc6c3328b0eb5066ebbddb46703e478d5e144aabb7774`  
		Last Modified: Mon, 28 Apr 2025 21:53:48 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6742248fe35df62d6669f6b002a19d18a41bc87200e7648fd09b75b79ab9d88b`  
		Last Modified: Mon, 28 Apr 2025 21:53:51 GMT  
		Size: 104.3 MB (104325366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d09d9032f0a417f214a8cc6ee1d3b3a9ef491bea6a5f64bb131fc8899e1809bd`  
		Last Modified: Mon, 28 Apr 2025 21:53:48 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e664cc377faffcb056ea2aee27368908ff62503f4bc95e102112a919f955a6e`  
		Last Modified: Mon, 28 Apr 2025 21:53:49 GMT  
		Size: 20.1 MB (20123787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbf5025d207a93dd3c32a3a3638658a2134fb9b57b708f71a5df302732b1c1f0`  
		Last Modified: Mon, 28 Apr 2025 21:53:49 GMT  
		Size: 438.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa8b11d585636dd85c40e32190df48c5a5cf8eb49279650bc71f9aec95838dcf`  
		Last Modified: Mon, 28 Apr 2025 21:53:49 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a963733eb06d595c99ca60689b61bf6aed448db6e0377561b8a4c5c02a4c1a02`  
		Last Modified: Mon, 28 Apr 2025 21:53:51 GMT  
		Size: 12.7 MB (12677483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b386c40fe703fd6ee18108c82543f2347f83c19afccc6e2f7f94aa86f707a1fa`  
		Last Modified: Mon, 28 Apr 2025 21:53:50 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d43e69495ca329c434856178c983d8b8de1f1db900731929de1050e45a33206f`  
		Last Modified: Mon, 28 Apr 2025 21:53:52 GMT  
		Size: 11.7 MB (11657214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e8022c65f7fd6949425c2660868947d03741d415f9eed1617b056424e28d5d`  
		Last Modified: Mon, 28 Apr 2025 21:53:52 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e10769bc92ff0caa168e536ad48025826421d0b18142e07447bca80cd4489339`  
		Last Modified: Mon, 28 Apr 2025 21:53:53 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f9de49fb7a526ce7ed46b195d0d28adb0da949674553e3461a23ad92d473c23`  
		Last Modified: Mon, 28 Apr 2025 21:53:53 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:526a27ac8df1ab1a1869f0926aec24b19af6594e21f70d9a048f902ee0d0b8f6`  
		Last Modified: Mon, 28 Apr 2025 22:15:08 GMT  
		Size: 26.3 MB (26253853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5db64a3be6c45f1c2fb82f8d23c2d7e77db817efbd91b8be6927b40a94f4fae1`  
		Last Modified: Mon, 28 Apr 2025 22:15:07 GMT  
		Size: 18.0 MB (18026606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29500e3f61b9dff54d61596f688df64c043836e895fb8fbcdbef6de92d893d19`  
		Last Modified: Mon, 28 Apr 2025 22:15:07 GMT  
		Size: 357.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ec1d8b8f8e162846bdc493ea2c27f35333e9dbba2d1e72689cd3542ba100f7`  
		Last Modified: Mon, 28 Apr 2025 22:15:07 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb363f3a5bdca0a07912581f268931de5af66391300eab943c75176dbcb7330`  
		Last Modified: Mon, 28 Apr 2025 22:15:08 GMT  
		Size: 19.2 KB (19151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4185bc1e8e7289b34f72d17555af7fb53c4f3ac5f844426b2f4ad2fe89a9796d`  
		Last Modified: Mon, 28 Apr 2025 22:15:09 GMT  
		Size: 26.9 MB (26894931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81525101fd429b4ae20e198da9d9cbecc0bca687194370085974341421ecad1c`  
		Last Modified: Mon, 28 Apr 2025 22:15:08 GMT  
		Size: 2.4 KB (2437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78e723e4368e3638bd3b6d9697fcfa3fe930ff91fc35d0fe8d6ffeaec5d84c6f`  
		Last Modified: Mon, 28 Apr 2025 22:15:09 GMT  
		Size: 1.7 KB (1725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.8.1-RC1-php8.3-apache` - unknown; unknown

```console
$ docker pull wordpress@sha256:d8e97d94f4e5ed33c96a5a4ae005a7130ab0f9bffd24eed644f187ab68595613
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8171916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f376c631e6c0e9f0e603f90cac802ad13329c537a44683b3947fcc3f949d702a`

```dockerfile
```

-	Layers:
	-	`sha256:0cfd0ae5dee18c5f918494129d54f0100ac1556a513340b67d208bee2a021955`  
		Last Modified: Mon, 28 Apr 2025 22:15:07 GMT  
		Size: 8.1 MB (8112500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1cc84acf90a6c9f0f8532ed6615718af991141d91ca0287adda212046283975`  
		Last Modified: Mon, 28 Apr 2025 22:15:07 GMT  
		Size: 59.4 KB (59416 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6.8.1-RC1-php8.3-apache` - linux; 386

```console
$ docker pull wordpress@sha256:831e3dabbc69623e85127c4b5f3a5c2c34b4f4074581add426636a7daf4354ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.6 MB (243555947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f110021a2c7b53988eeebd6915a9b2a964c7d1fa96a728dd77ed96f1aab1ee9c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 10 Apr 2025 18:46:32 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1745798400'
# Thu, 10 Apr 2025 18:46:32 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 10 Apr 2025 18:46:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 10 Apr 2025 18:46:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Apr 2025 18:46:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 10 Apr 2025 18:46:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 10 Apr 2025 18:46:32 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 10 Apr 2025 18:46:32 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 10 Apr 2025 18:46:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 10 Apr 2025 18:46:32 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 10 Apr 2025 18:46:32 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 10 Apr 2025 18:46:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 10 Apr 2025 18:46:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 10 Apr 2025 18:46:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 10 Apr 2025 18:46:32 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 10 Apr 2025 18:46:32 GMT
ENV PHP_VERSION=8.3.20
# Thu, 10 Apr 2025 18:46:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.20.tar.xz.asc
# Thu, 10 Apr 2025 18:46:32 GMT
ENV PHP_SHA256=f15914e071b5bddaf1475b5f2ba68107e8b8846655f9e89690fb7cd410b0db6c
# Thu, 10 Apr 2025 18:46:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 10 Apr 2025 18:46:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 10 Apr 2025 18:46:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 10 Apr 2025 18:46:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 10 Apr 2025 18:46:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 10 Apr 2025 18:46:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 10 Apr 2025 18:46:32 GMT
STOPSIGNAL SIGWINCH
# Thu, 10 Apr 2025 18:46:32 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 10 Apr 2025 18:46:32 GMT
WORKDIR /var/www/html
# Thu, 10 Apr 2025 18:46:32 GMT
EXPOSE map[80/tcp:{}]
# Thu, 10 Apr 2025 18:46:32 GMT
CMD ["apache2-foreground"]
# Mon, 28 Apr 2025 19:03:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Apr 2025 19:03:12 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Mon, 28 Apr 2025 19:03:12 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Mon, 28 Apr 2025 19:03:12 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Mon, 28 Apr 2025 19:03:12 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Mon, 28 Apr 2025 19:03:12 GMT
RUN set -eux; 	version='6.8.1-RC1'; 	sha1='1c8d27d51ece5b56aa511eaaf0ceef26617a254b'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Mon, 28 Apr 2025 19:03:12 GMT
VOLUME [/var/www/html]
# Mon, 28 Apr 2025 19:03:12 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Mon, 28 Apr 2025 19:03:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 28 Apr 2025 19:03:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 28 Apr 2025 19:03:12 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:ad2e653a01d32a9a8676730797453c924f9d10fe1414178e7a26c35132c3691e`  
		Last Modified: Mon, 28 Apr 2025 21:08:11 GMT  
		Size: 29.2 MB (29210866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:842129b1c7190063331eeeb6e757f5be3060c6720bc8e5452f53c516ce6ac084`  
		Last Modified: Mon, 28 Apr 2025 21:48:40 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c64b7ac08f26a1eb3f5963075c6413ebda3cb3a7dcd36f2340c63edec03df64f`  
		Last Modified: Mon, 28 Apr 2025 21:49:53 GMT  
		Size: 101.5 MB (101507850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf859381b32872fd65d6c9e970b8de3029cbd4def5f96e7df7802a25f9c91731`  
		Last Modified: Mon, 28 Apr 2025 21:49:50 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c0f0cae94281265ae2fb4533fad5bfb3dab26267e20a5ce7033d068a57bc7cd`  
		Last Modified: Mon, 28 Apr 2025 21:49:51 GMT  
		Size: 20.6 MB (20638465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:250eb2d3484b0b86c0cca7b0e4c9d3817dd53d907aa7a7d1aae2157ee5bbab6a`  
		Last Modified: Mon, 28 Apr 2025 21:49:51 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b15e390d8c6ba334c18305f7a7476652e2160beb2981cc07335c39fa1f6ac73`  
		Last Modified: Mon, 28 Apr 2025 21:49:51 GMT  
		Size: 481.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c886b18df97f98a8b19806cf2947818af5c7f71512ece3f72cc566a515c61f69`  
		Last Modified: Mon, 28 Apr 2025 21:49:52 GMT  
		Size: 12.7 MB (12676442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f7d2badb4feba80c826117a24f8b465a9eedb580fed3bb8f14fad30cc36207d`  
		Last Modified: Mon, 28 Apr 2025 21:49:52 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df00f92593be401260d95ed01bc8ccc0e09fe076cacd288c4d7982f403d66249`  
		Last Modified: Mon, 28 Apr 2025 21:49:53 GMT  
		Size: 11.9 MB (11883354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d4a4842829f59ca006659d07ea932cc7e51b9513f44578122e0ec2d44f1b703`  
		Last Modified: Mon, 28 Apr 2025 21:49:53 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6513768c69f27c2bd05b05a1c593a2f8995d360edfca725d7de45829d11003c8`  
		Last Modified: Mon, 28 Apr 2025 21:49:53 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18aee1cabba5844106359125dd1cd0571dbf017697f60c9a19e3ba77c828066d`  
		Last Modified: Mon, 28 Apr 2025 21:49:53 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e34937ef1b8a9a316fc3714e80f7d0e3d9056656b53d4d544473e00c89ff79a`  
		Last Modified: Mon, 28 Apr 2025 22:15:14 GMT  
		Size: 26.7 MB (26701029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9c0df92eee86bd3e9463c56900e982ad034d5da1a3b6ddeb56aa80030840670`  
		Last Modified: Mon, 28 Apr 2025 22:15:13 GMT  
		Size: 14.0 MB (14013487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76b340a7c6dd4f705409b3addb64742c7b6738741cad1adf84c68452811b5ee1`  
		Last Modified: Mon, 28 Apr 2025 22:15:12 GMT  
		Size: 358.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee7aedde626d469511976e3ef9d33c70ac979ebd46a7d0148714eedec33a6f25`  
		Last Modified: Mon, 28 Apr 2025 22:15:12 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f6e77c0a3eab32531f44db3ccf180e285c2d3c9b5b960c21d5bb9287aa2054a`  
		Last Modified: Mon, 28 Apr 2025 22:15:13 GMT  
		Size: 19.1 KB (19145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f2cfd873f9fcaf8b4f8d9a94c0d061d5439cf6b11f360322b3931b563ba7185`  
		Last Modified: Mon, 28 Apr 2025 22:15:15 GMT  
		Size: 26.9 MB (26894937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd58b7cd70a922dace953a84c02bea72cb01cc2e6f558c3156b776acfeb477e4`  
		Last Modified: Mon, 28 Apr 2025 22:15:14 GMT  
		Size: 2.4 KB (2437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5763152716c73e81e8d05f4b46963ace6abe1bff1be7ded850c87e16425d7ec`  
		Last Modified: Mon, 28 Apr 2025 22:15:14 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.8.1-RC1-php8.3-apache` - unknown; unknown

```console
$ docker pull wordpress@sha256:2aeda65b962deddea0d3e8928aa2c4fb18fd46b910a21f78c0d0673e9d92e9ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8145030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4f1ad38a770ed0372a45340d2d67b27af26431b7a31916d4934072db9cc80fd`

```dockerfile
```

-	Layers:
	-	`sha256:536d7bf8f351546b42dbfcc2f8f00b5635673868497e614e82280cd6d0e80600`  
		Last Modified: Mon, 28 Apr 2025 22:15:12 GMT  
		Size: 8.1 MB (8085686 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d3029160c79b4577dab3473dc463cd4ba15db4c944933eb5b818e82be7f6546`  
		Last Modified: Mon, 28 Apr 2025 22:15:12 GMT  
		Size: 59.3 KB (59344 bytes)  
		MIME: application/vnd.in-toto+json
