## `wordpress:beta-6.7-apache`

```console
$ docker pull wordpress@sha256:ae5ab6d598d5778821e7e07dd60c5b90d133693baa80e37f7d32f195ae967043
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

### `wordpress:beta-6.7-apache` - linux; amd64

```console
$ docker pull wordpress@sha256:c2944461453f8ce3714c9cd26ad5f713a1e38fb87f97365a96f35b9640776002
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.8 MB (247764440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57538d324fa989b443ede91355cce8f6151822dd68edb33167d78ba29ab9848b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 24 Oct 2024 13:43:42 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
CMD ["bash"]
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 24 Oct 2024 13:43:42 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 24 Oct 2024 13:43:42 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_VERSION=8.2.25
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.25.tar.xz.asc
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_SHA256=330b54876ea1d05ade12ee9726167332058bccd58dffa1d4e12117f6b4f616b9
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 24 Oct 2024 13:43:42 GMT
STOPSIGNAL SIGWINCH
# Thu, 24 Oct 2024 13:43:42 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
WORKDIR /var/www/html
# Thu, 24 Oct 2024 13:43:42 GMT
EXPOSE map[80/tcp:{}]
# Thu, 24 Oct 2024 13:43:42 GMT
CMD ["apache2-foreground"]
# Mon, 11 Nov 2024 20:03:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 Nov 2024 20:03:11 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Mon, 11 Nov 2024 20:03:11 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Mon, 11 Nov 2024 20:03:11 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Mon, 11 Nov 2024 20:03:11 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Mon, 11 Nov 2024 20:03:11 GMT
RUN set -eux; 	version='6.7-RC5'; 	sha1='f3103a0adc6bd356ce743b6f0ad12d0be6f6ac36'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Mon, 11 Nov 2024 20:03:11 GMT
VOLUME [/var/www/html]
# Mon, 11 Nov 2024 20:03:11 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Mon, 11 Nov 2024 20:03:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 11 Nov 2024 20:03:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 11 Nov 2024 20:03:11 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:400f75d9900933d30012ae07a280ee314031d6a2601fe469564c57626344628a`  
		Last Modified: Tue, 12 Nov 2024 02:35:50 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e532b66579ca9090a88a11bcdf58bc8e3a1905bfa119ce4b8ae488acba54ca93`  
		Last Modified: Tue, 12 Nov 2024 02:35:52 GMT  
		Size: 104.3 MB (104345685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ac50b358b78087371933f3818b150ef49b93a4f520a04c6942d6e5966c97fad`  
		Last Modified: Tue, 12 Nov 2024 02:35:50 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8ecb69d311b1181be24831dde5171ea00f5e4d6bed8d31e51d620106415aaaf`  
		Last Modified: Tue, 12 Nov 2024 02:35:50 GMT  
		Size: 20.1 MB (20123880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c047dfa11941ada6ddbe46380f704a04a17f208756469239974a7af0df7378d0`  
		Last Modified: Tue, 12 Nov 2024 02:35:51 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef42461ff613cf822d2b86e0063b7d0599c29de666a23ef2ba283a86a24c1a88`  
		Last Modified: Tue, 12 Nov 2024 02:35:51 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c524fd1548ce282b7066301e749020ccd5aa2863cb86531c47c58e092404d93`  
		Last Modified: Tue, 12 Nov 2024 02:35:52 GMT  
		Size: 12.3 MB (12254756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50edcb1570eff66dd9e3b25933366082da74bf20ea6e96457b8a039a5ee0c517`  
		Last Modified: Tue, 12 Nov 2024 02:35:51 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb08836f49b3f0d2273b0462d9adc33862bd8728182d43cd49efaead28aeb67e`  
		Last Modified: Tue, 12 Nov 2024 02:35:52 GMT  
		Size: 11.4 MB (11409884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c23822149981d4e949a62c840ed95968ad6435207101bed113cb17c69e7d9ff`  
		Last Modified: Tue, 12 Nov 2024 02:35:52 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3e55308e305faad7e8a7364cd3103e3393c916147a4e5713684137201c2588`  
		Last Modified: Tue, 12 Nov 2024 02:35:53 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f217c2e0f353496b2100626fbcdfde08d294f33435bfe71a85b11482ece6c1e`  
		Last Modified: Tue, 12 Nov 2024 02:35:53 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fae362f23edd5fb6f90f10964a7af1416dced9f73e3c880376bd255f9ffb2ad`  
		Last Modified: Tue, 12 Nov 2024 20:09:14 GMT  
		Size: 26.3 MB (26254500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fec6944ffdb69974caec76e9fdb94bb71e3e6e688364c25fbde90fd5823d844`  
		Last Modified: Tue, 12 Nov 2024 20:09:14 GMT  
		Size: 17.5 MB (17471984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecedefb36d201bc48a258b972da9fa42c0a744011128c0d2f71fef33dbde5b22`  
		Last Modified: Tue, 12 Nov 2024 20:09:13 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:055e100d2cea5bb6c660c703dabeb52003d4075bab071957cc1fd27a5881e7fa`  
		Last Modified: Tue, 12 Nov 2024 20:09:13 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b461ead75afe839a0d55e10cb0eeac6cc226e339dff7828ea92776985c16d3b`  
		Last Modified: Tue, 12 Nov 2024 20:09:14 GMT  
		Size: 19.2 KB (19151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69b141862bbda2a345970c3d5a1569153a40a4b8bc9144d0f70f9eec0b9592a1`  
		Last Modified: Tue, 12 Nov 2024 20:09:15 GMT  
		Size: 26.7 MB (26746208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193540c52af4adef33f923345ff98843fc3cd0961994c098c9880b202b424445`  
		Last Modified: Tue, 12 Nov 2024 20:09:15 GMT  
		Size: 2.4 KB (2438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccdbd8638c0c1a794934711a3157a8bec834e09c6690f56ead634527651158e9`  
		Last Modified: Tue, 12 Nov 2024 20:09:15 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.7-apache` - unknown; unknown

```console
$ docker pull wordpress@sha256:41e1aaad98be11637a6e3b6a0c406247fd6c12012a94c3d3cc737c87adccae80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8189058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96728693132364b3f79f67ce504d071c60cc28a82e0782e610a142b968bf2442`

```dockerfile
```

-	Layers:
	-	`sha256:fceeef5593b8581eae78413cbd7c5d2c89777bf7260c02c755d47719b673164d`  
		Last Modified: Tue, 12 Nov 2024 20:09:13 GMT  
		Size: 8.1 MB (8125758 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca2a6b3a74f034b84a6febb14225c3e74f2b941f15e5ae20d7ffa3c9bb0c93f8`  
		Last Modified: Tue, 12 Nov 2024 20:09:13 GMT  
		Size: 63.3 KB (63300 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6.7-apache` - linux; arm variant v5

```console
$ docker pull wordpress@sha256:c8ffb6ece626591fbdfa5c096f308fe1176e4ecdfe99f7af8f0e633fa24fb0ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.7 MB (216705032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7ce2952c532636203f9e9924f607fa04e85da6866c47585327577a6bf91e525`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 24 Oct 2024 13:43:42 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
CMD ["bash"]
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 24 Oct 2024 13:43:42 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 24 Oct 2024 13:43:42 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_VERSION=8.2.25
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.25.tar.xz.asc
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_SHA256=330b54876ea1d05ade12ee9726167332058bccd58dffa1d4e12117f6b4f616b9
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 24 Oct 2024 13:43:42 GMT
STOPSIGNAL SIGWINCH
# Thu, 24 Oct 2024 13:43:42 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
WORKDIR /var/www/html
# Thu, 24 Oct 2024 13:43:42 GMT
EXPOSE map[80/tcp:{}]
# Thu, 24 Oct 2024 13:43:42 GMT
CMD ["apache2-foreground"]
# Mon, 11 Nov 2024 20:03:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 Nov 2024 20:03:11 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Mon, 11 Nov 2024 20:03:11 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Mon, 11 Nov 2024 20:03:11 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Mon, 11 Nov 2024 20:03:11 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Mon, 11 Nov 2024 20:03:11 GMT
RUN set -eux; 	version='6.7-RC5'; 	sha1='f3103a0adc6bd356ce743b6f0ad12d0be6f6ac36'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Mon, 11 Nov 2024 20:03:11 GMT
VOLUME [/var/www/html]
# Mon, 11 Nov 2024 20:03:11 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Mon, 11 Nov 2024 20:03:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 11 Nov 2024 20:03:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 11 Nov 2024 20:03:11 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:5ecbccf2cc6c4ffb179160d83e2f057a548b6aea719fc2b9b49c502da3d570e3`  
		Last Modified: Tue, 12 Nov 2024 00:55:10 GMT  
		Size: 26.9 MB (26890058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a0ecfad706f423d72f784713c6e330fb07894f5581828886246a6f696dc5dcd`  
		Last Modified: Tue, 12 Nov 2024 02:32:34 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bdc0003cb59a2246daf9c98d60695941f3b7fb3e946787615b6b24498c2902a`  
		Last Modified: Tue, 12 Nov 2024 02:32:37 GMT  
		Size: 82.0 MB (81992661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30d7cc6d2cd608d6e46c893c66f11311b91174768d7c19e4e8fab10922f896d1`  
		Last Modified: Tue, 12 Nov 2024 02:32:34 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dc288200a587c04c4a516848305eb50a074c72c0da800766f18c69bf488a295`  
		Last Modified: Tue, 12 Nov 2024 02:38:57 GMT  
		Size: 19.4 MB (19419230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd8e4f30b1778e27afb7a2ff3afe61620a6461135330c97674b47ec1cba026cc`  
		Last Modified: Tue, 12 Nov 2024 02:38:56 GMT  
		Size: 437.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:464be6317f9579fddccfdb0447cafdd2b1dd8b860a64422d6dc5ff442e9bb491`  
		Last Modified: Tue, 12 Nov 2024 02:38:56 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f8ebd18ae3f14556164436fa0d85ddb353f8a1128786a1fd4541f9712d07782`  
		Last Modified: Tue, 12 Nov 2024 04:02:15 GMT  
		Size: 12.3 MB (12253184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b2618ff9378d468fb1184d19c5f1da58142516f607f6cba3af68d19f6beec45`  
		Last Modified: Tue, 12 Nov 2024 04:02:14 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d1b76f1957d95f72e17268a94eee95088a2cf42cafbac4b66da6ed854eeed21`  
		Last Modified: Tue, 12 Nov 2024 04:02:15 GMT  
		Size: 10.4 MB (10392847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e449f62e8cd60216bc2f546e993bebcd4ee51b229ac224bfb0d1791552a6ce2c`  
		Last Modified: Tue, 12 Nov 2024 04:02:14 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4ac27ab7a9f78c55da42c79834a77957249e22964978a87ab4e2ac358915345`  
		Last Modified: Tue, 12 Nov 2024 04:02:15 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c3ca3f4bc777b59fa6a38c8ab3ab11f8a842a35d9f90d3b2333ca3bfcf839fe`  
		Last Modified: Tue, 12 Nov 2024 04:02:15 GMT  
		Size: 886.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be9a353b64bccdd3cd5ed78695dd80b8a95ea0a476c89957283d18847bc569fe`  
		Last Modified: Tue, 12 Nov 2024 11:05:11 GMT  
		Size: 25.7 MB (25703820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37693d8e8a43648b826ad1a690357afb52e93c32acbe6f78f4c4b32e3039c324`  
		Last Modified: Tue, 12 Nov 2024 11:05:11 GMT  
		Size: 13.3 MB (13277500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c29de69bf666cf19553aff04ac2e9fc14fde3d84c880f90db5c5f0ff6373043a`  
		Last Modified: Tue, 12 Nov 2024 11:05:11 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e692258bb05ab32a8783443129333f123d0938ff0ad8d6d08161fd7a784cdde3`  
		Last Modified: Tue, 12 Nov 2024 11:05:10 GMT  
		Size: 391.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7e0b0a1d0ef460e503357fab19fbcb078d786648bde92b135539f93e1bff55c`  
		Last Modified: Tue, 12 Nov 2024 11:05:11 GMT  
		Size: 19.2 KB (19157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f857cf2263c0f07d288f18117adbb182e10b124ac98c72f3f88dff475551419`  
		Last Modified: Tue, 12 Nov 2024 23:24:34 GMT  
		Size: 26.7 MB (26746184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a21c6a87105877bc986f3fce603c3308c1ce94e144376f65387310a960f5e6`  
		Last Modified: Tue, 12 Nov 2024 23:24:33 GMT  
		Size: 2.4 KB (2435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d25804ed67933dad06d91a2da11aed18c4af71ad35fb1ad1704e3240bac8c2cf`  
		Last Modified: Tue, 12 Nov 2024 23:24:33 GMT  
		Size: 1.7 KB (1726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.7-apache` - unknown; unknown

```console
$ docker pull wordpress@sha256:899e8944582c5fdbcc0401fd82d7f63412875a6dc60319776bd510994c818dd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7995232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f77ebfcfa3314d9e20a4e397aa78626ef26b0e7e5ffd83870fc3e227637d2cb0`

```dockerfile
```

-	Layers:
	-	`sha256:ad0f34f0b31f9132254525e008651c69958241524e14cf9db035c56bfb823fb4`  
		Last Modified: Tue, 12 Nov 2024 23:24:33 GMT  
		Size: 7.9 MB (7931704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a81c55d4d328a0878962d713faf8bb51eea7495cd34822a661fb49451a484b66`  
		Last Modified: Tue, 12 Nov 2024 23:24:32 GMT  
		Size: 63.5 KB (63528 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6.7-apache` - linux; arm variant v7

```console
$ docker pull wordpress@sha256:5fb2d1d0422f13340a28416f3fb4c9e3428913b29215cd53c80028014653c19f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.7 MB (205713043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09a2a8f0b6afb6ac01b7a78d7c9ae7d545194f188ee8d59a861a4531f38a4952`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 24 Oct 2024 13:43:42 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
CMD ["bash"]
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 24 Oct 2024 13:43:42 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 24 Oct 2024 13:43:42 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_VERSION=8.2.25
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.25.tar.xz.asc
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_SHA256=330b54876ea1d05ade12ee9726167332058bccd58dffa1d4e12117f6b4f616b9
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 24 Oct 2024 13:43:42 GMT
STOPSIGNAL SIGWINCH
# Thu, 24 Oct 2024 13:43:42 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
WORKDIR /var/www/html
# Thu, 24 Oct 2024 13:43:42 GMT
EXPOSE map[80/tcp:{}]
# Thu, 24 Oct 2024 13:43:42 GMT
CMD ["apache2-foreground"]
# Mon, 11 Nov 2024 20:03:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 Nov 2024 20:03:11 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Mon, 11 Nov 2024 20:03:11 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Mon, 11 Nov 2024 20:03:11 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Mon, 11 Nov 2024 20:03:11 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Mon, 11 Nov 2024 20:03:11 GMT
RUN set -eux; 	version='6.7-RC5'; 	sha1='f3103a0adc6bd356ce743b6f0ad12d0be6f6ac36'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Mon, 11 Nov 2024 20:03:11 GMT
VOLUME [/var/www/html]
# Mon, 11 Nov 2024 20:03:11 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Mon, 11 Nov 2024 20:03:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 11 Nov 2024 20:03:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 11 Nov 2024 20:03:11 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:ddd3c6488ea8b62db6811ba136fe14cba70219532910e67a91ed3388ec9f5757`  
		Last Modified: Tue, 12 Nov 2024 00:56:42 GMT  
		Size: 24.7 MB (24718909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4297c5ae3c7e8e8915409622802213bf4512c2b4a0bf9a86ed680878ddc18a70`  
		Last Modified: Tue, 12 Nov 2024 03:10:01 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc4b50adcb7cdffa12052ba1589718b3c06d474e40507177a93fc914de46e895`  
		Last Modified: Tue, 12 Nov 2024 03:10:04 GMT  
		Size: 76.2 MB (76162385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:681174cd466f54c52977f6c159c33d12bdd6aa108d2d06470ff258ce5d3fac19`  
		Last Modified: Tue, 12 Nov 2024 03:10:01 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3956adc6ba757482684b1a409597f790541c714f71ba631eee7d291574e817e`  
		Last Modified: Tue, 12 Nov 2024 03:15:54 GMT  
		Size: 18.9 MB (18857501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1e647e764fe2dcfbd101cd5fcaaec1c944c7cd89cd40a65dcd2442b62733654`  
		Last Modified: Tue, 12 Nov 2024 03:15:53 GMT  
		Size: 433.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:429807ca1f9d7d3c489deadada060b40a6d8bd76e76a48f0a9298d511be0304c`  
		Last Modified: Tue, 12 Nov 2024 03:15:53 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d182f4c6df47bdbe3801f7d6d20ad82afa8001530cd368ebd61776e5f50fa3ad`  
		Last Modified: Tue, 12 Nov 2024 08:04:05 GMT  
		Size: 12.3 MB (12253256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70022f0643e3c81a43c68d9dcf290573d5a8b74a3056e95d556f8bd898350a24`  
		Last Modified: Tue, 12 Nov 2024 08:04:04 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85edb6998fe32e0449c2b45b63c9f40c23f96c703a8722b3cadf0dd3b571a76a`  
		Last Modified: Tue, 12 Nov 2024 08:04:05 GMT  
		Size: 9.8 MB (9824931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53fbe069c23ad21b149523d0d100a569b4c601bd3b71b58265ba8e91e3175801`  
		Last Modified: Tue, 12 Nov 2024 08:04:04 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c4049646dc9e66848219df55afd2063bf3b7bd0ca7b3ca89ebf11ddb694da9`  
		Last Modified: Tue, 12 Nov 2024 08:04:05 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd3b1967ec410bfa1f113f761eaefd23810d8f7b1f979498f2ea2917bcd170ea`  
		Last Modified: Tue, 12 Nov 2024 08:04:05 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4954ab198fac73644df59b74086e995c670520860a25e082ce35bf47f2bc97c9`  
		Last Modified: Wed, 13 Nov 2024 07:13:32 GMT  
		Size: 25.1 MB (25077412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03dd05dd44cf18ac27c65db0126c3edb5a8d6ee804faf730e0efa6b1769a99d1`  
		Last Modified: Wed, 13 Nov 2024 07:13:31 GMT  
		Size: 12.0 MB (12042889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f597f371f594eb258c9f7f140aabe7ae93183bd596048520ed40d785afc4529`  
		Last Modified: Wed, 13 Nov 2024 07:13:31 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdcda7dd6b8a033b0929727bb24875deba589d788cbeb2088e3a8337a0671c0d`  
		Last Modified: Wed, 13 Nov 2024 07:13:31 GMT  
		Size: 391.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3007c0ddb372dc1b35ac5594096bff39bbd1d36f0050731d52d877e4683d880`  
		Last Modified: Wed, 13 Nov 2024 07:13:32 GMT  
		Size: 19.2 KB (19156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b3e9c88b95131cd8122860e71a18839778852504c5a7e412caf5452bef8c636`  
		Last Modified: Wed, 13 Nov 2024 07:31:32 GMT  
		Size: 26.7 MB (26746204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:188ca23f013e3a3d45460a6145821ba08fa5af88972c5a84b7bacda57f50c628`  
		Last Modified: Wed, 13 Nov 2024 07:31:31 GMT  
		Size: 2.4 KB (2438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:355213c65fdad21d4b1fe912d50469c7e3848d52e3049a0714dc15747c73b27d`  
		Last Modified: Wed, 13 Nov 2024 07:31:31 GMT  
		Size: 1.7 KB (1726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.7-apache` - unknown; unknown

```console
$ docker pull wordpress@sha256:ec14244e47a78b1fce194765f2ca21b13c097e48a6c425983a07e7182898a279
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7999918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1946ec5720b0c8e6dcbb2e0a998a49cee53efd0f991205d27fa53c922bec2941`

```dockerfile
```

-	Layers:
	-	`sha256:f3d119e906dae06817bba52e4689011cd6b662cecf7d8eecd17bfb401e54ec27`  
		Last Modified: Wed, 13 Nov 2024 07:31:31 GMT  
		Size: 7.9 MB (7936398 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f58c3248d9eb2111b54d40aebd1a047d866ee95719b5c530a975a59214e5fd6`  
		Last Modified: Wed, 13 Nov 2024 07:31:30 GMT  
		Size: 63.5 KB (63520 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6.7-apache` - linux; arm64 variant v8

```console
$ docker pull wordpress@sha256:f7204c026ed326ab6c5b21efc827240d76f83372d64c3032c1f0f133cdbf7d62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.8 MB (237816269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2c8b414b182e834545c9177d0e507a4e206bf54305c01a482f5c670f71d5b74`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 24 Oct 2024 13:43:42 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
CMD ["bash"]
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 24 Oct 2024 13:43:42 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 24 Oct 2024 13:43:42 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_VERSION=8.2.25
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.25.tar.xz.asc
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_SHA256=330b54876ea1d05ade12ee9726167332058bccd58dffa1d4e12117f6b4f616b9
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 24 Oct 2024 13:43:42 GMT
STOPSIGNAL SIGWINCH
# Thu, 24 Oct 2024 13:43:42 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
WORKDIR /var/www/html
# Thu, 24 Oct 2024 13:43:42 GMT
EXPOSE map[80/tcp:{}]
# Thu, 24 Oct 2024 13:43:42 GMT
CMD ["apache2-foreground"]
# Mon, 11 Nov 2024 20:03:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 Nov 2024 20:03:11 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Mon, 11 Nov 2024 20:03:11 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Mon, 11 Nov 2024 20:03:11 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Mon, 11 Nov 2024 20:03:11 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Mon, 11 Nov 2024 20:03:11 GMT
RUN set -eux; 	version='6.7-RC5'; 	sha1='f3103a0adc6bd356ce743b6f0ad12d0be6f6ac36'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Mon, 11 Nov 2024 20:03:11 GMT
VOLUME [/var/www/html]
# Mon, 11 Nov 2024 20:03:11 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Mon, 11 Nov 2024 20:03:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 11 Nov 2024 20:03:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 11 Nov 2024 20:03:11 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29e9756e7bfc559baf6454131f81839efb97d80f167664be5b4272ac469b5960`  
		Last Modified: Tue, 12 Nov 2024 03:32:16 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e27785ead77c6cc3a0473bbe35b537db4b7a71bc35c6289f88af2c9ee06119`  
		Last Modified: Tue, 12 Nov 2024 03:32:19 GMT  
		Size: 98.1 MB (98130714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27a00cfa6daf2de029a0f81a774bb1018582dc28b1eb0b8bb09c1d7672fb91ce`  
		Last Modified: Tue, 12 Nov 2024 03:32:16 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca35e1d28ad7ebbff66a1fdc4d24ada4c30b131fd323f6cbea4b7fb07bc8d706`  
		Last Modified: Tue, 12 Nov 2024 03:36:02 GMT  
		Size: 20.1 MB (20120907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410639cb967ec54ee760206ed58c1613b50690b91d753ac3ebf143807443f069`  
		Last Modified: Tue, 12 Nov 2024 03:36:01 GMT  
		Size: 439.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f9efafdf219d3eb366948d2078a5f7f1d4ff893121d52b94c89678ccbee36ac`  
		Last Modified: Tue, 12 Nov 2024 03:36:01 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7946ba9a569f7e501c4f65b60c14167db6ae2052d4f038db286852df797af96`  
		Last Modified: Tue, 12 Nov 2024 07:23:33 GMT  
		Size: 12.3 MB (12254617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67f1de0deede2eea05e09dfb8a4bd8e892e3d808eef90b51356361daa7908115`  
		Last Modified: Tue, 12 Nov 2024 07:23:32 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d96ecd01e3f5ffa0265fa88830a9f954864c62085c8683fd139f9274eb517e54`  
		Last Modified: Tue, 12 Nov 2024 07:23:33 GMT  
		Size: 11.4 MB (11417386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c470e029cbda8a745b58452eea84ffb1e4b18c339ef318651bb74678eebc3fc2`  
		Last Modified: Tue, 12 Nov 2024 07:23:32 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77cbd2f3c900a11e4239528e754af9ea385218d944926df0c65cf41cd3d7dbc7`  
		Last Modified: Tue, 12 Nov 2024 07:23:33 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:646aa471737e5afeb30a122b1b252d4898b4550224496770b174a2e0b34972f6`  
		Last Modified: Tue, 12 Nov 2024 07:23:33 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ab30a6e19b4a5da40159a5d31342b87f8355518a2e4e0990fe7dcab03ad8904`  
		Last Modified: Wed, 13 Nov 2024 02:12:14 GMT  
		Size: 26.2 MB (26174045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1635648fee755e48f029769b5c9e2d5d8007765fb0feae6049bf1d8b55f2cfd`  
		Last Modified: Wed, 13 Nov 2024 02:12:14 GMT  
		Size: 13.8 MB (13785508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:721605ec8cbc29b5818424686e9e0dcfdb061c61ec7154154ecf552530154358`  
		Last Modified: Wed, 13 Nov 2024 02:12:13 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bf2a3e9ff28cc6b79709184cc2ca0071be942fb957dbc422943c54feee4f0d6`  
		Last Modified: Wed, 13 Nov 2024 02:12:13 GMT  
		Size: 391.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dce276ad38f780ce79e8d4097dbad14063451c6abf35b1ed1d8b604ea99548c`  
		Last Modified: Wed, 13 Nov 2024 02:12:14 GMT  
		Size: 19.2 KB (19153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f9c2568b8e0fafef597b2a2d303c18fd8c9f331ee4fe8aad25d4c857c63eb03`  
		Last Modified: Wed, 13 Nov 2024 02:29:57 GMT  
		Size: 26.7 MB (26746183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc80482dde20d2c2e0393e5858c81e4c906900d6ca1e383f247414fab3632df`  
		Last Modified: Wed, 13 Nov 2024 02:29:56 GMT  
		Size: 2.4 KB (2439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6e8b41ce1feb9305787ba2f2d40f3192b6a256ce60c86a5eeb667c4527008ec`  
		Last Modified: Wed, 13 Nov 2024 02:29:56 GMT  
		Size: 1.7 KB (1729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.7-apache` - unknown; unknown

```console
$ docker pull wordpress@sha256:a0c1b02b9ef10018b0f9e0d118985b0231b05fa132aa5cd008c8db772155bf00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8218316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dd238775a27f2ceeb1e5e17960a03e4b1c1bd861fed42c3a9fdc8128e829fa4`

```dockerfile
```

-	Layers:
	-	`sha256:d05c7a223df5ab9613024ff32930fd757cbf7f58835034d50a9dcf54a45d6416`  
		Last Modified: Wed, 13 Nov 2024 02:29:56 GMT  
		Size: 8.2 MB (8154701 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a90842231a05890c0caa2f897256d8fcbf88aa30405772d6b8668fe4e0892636`  
		Last Modified: Wed, 13 Nov 2024 02:29:56 GMT  
		Size: 63.6 KB (63615 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6.7-apache` - linux; 386

```console
$ docker pull wordpress@sha256:0cc46638520d53f0cd08fdbb89b12fbe6d260453842b6ab3c88bca3f1361f240
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.2 MB (243156449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b6c1e05ea3b09219bae4378534b7d101d4d465b6df3a35e008eb149f20f759d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 24 Oct 2024 13:43:42 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
CMD ["bash"]
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 24 Oct 2024 13:43:42 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 24 Oct 2024 13:43:42 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_VERSION=8.2.25
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.25.tar.xz.asc
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_SHA256=330b54876ea1d05ade12ee9726167332058bccd58dffa1d4e12117f6b4f616b9
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 24 Oct 2024 13:43:42 GMT
STOPSIGNAL SIGWINCH
# Thu, 24 Oct 2024 13:43:42 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
WORKDIR /var/www/html
# Thu, 24 Oct 2024 13:43:42 GMT
EXPOSE map[80/tcp:{}]
# Thu, 24 Oct 2024 13:43:42 GMT
CMD ["apache2-foreground"]
# Mon, 11 Nov 2024 20:03:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 Nov 2024 20:03:11 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Mon, 11 Nov 2024 20:03:11 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Mon, 11 Nov 2024 20:03:11 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Mon, 11 Nov 2024 20:03:11 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Mon, 11 Nov 2024 20:03:11 GMT
RUN set -eux; 	version='6.7-RC5'; 	sha1='f3103a0adc6bd356ce743b6f0ad12d0be6f6ac36'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Mon, 11 Nov 2024 20:03:11 GMT
VOLUME [/var/www/html]
# Mon, 11 Nov 2024 20:03:11 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Mon, 11 Nov 2024 20:03:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 11 Nov 2024 20:03:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 11 Nov 2024 20:03:11 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:7379b58056e85869f90d8f78478cafd0c7468ad3b5085482a0850cee625a847a`  
		Last Modified: Tue, 12 Nov 2024 00:54:51 GMT  
		Size: 30.1 MB (30145450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e6aa68959e3142bef810ae40ce9d9fb27e8aee9ff4ae8634d70dca35f5fc4e5`  
		Last Modified: Tue, 12 Nov 2024 02:36:23 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16e621bc54389a6f4cc5195f76e44c98c06bea2f204a92b49ff9b5c2e8b012e0`  
		Last Modified: Tue, 12 Nov 2024 02:36:26 GMT  
		Size: 101.5 MB (101515043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f6833c9d664ad5005a990b8b5f5f9d7fc24ef88928bb6da2023075b78a98ac5`  
		Last Modified: Tue, 12 Nov 2024 02:36:14 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:365a9bdc5399c60371e8771ef0a38b9fe64fbb046be31fd5b859f91f9f896284`  
		Last Modified: Tue, 12 Nov 2024 02:36:24 GMT  
		Size: 20.6 MB (20638469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc4c46338eff630426f34653b21d0488b3bb16c93073fa52291f308b50da975c`  
		Last Modified: Tue, 12 Nov 2024 02:36:24 GMT  
		Size: 437.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:399974df35da6e022f4a2a50f56e70a355380268d1c9d3af38ac72e0105d3094`  
		Last Modified: Tue, 12 Nov 2024 02:36:24 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9f4640c43e435175f4c0e0600449beab7c1d3cd76fe3c600f143c52bf4df7d3`  
		Last Modified: Tue, 12 Nov 2024 02:36:25 GMT  
		Size: 12.3 MB (12254054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23328ade74f6167ee11a5782a1d7157e07ed4031652b522082ad12c02ef21917`  
		Last Modified: Tue, 12 Nov 2024 02:36:25 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50ace98562889741964d8e5699e9148e29110de00c2fdc5fa0df9250d2f0e968`  
		Last Modified: Tue, 12 Nov 2024 02:36:26 GMT  
		Size: 11.6 MB (11640486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e265d0896f0be609cb15bd9f78d78b47e5f51127b1c9260f50de7d0c9cd2ea8`  
		Last Modified: Tue, 12 Nov 2024 02:36:26 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:218b05273739a656a2a25f3d8a9142885eed375cb2a52f47081ebac9ca355ba7`  
		Last Modified: Tue, 12 Nov 2024 02:36:27 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26fb315c2ac5d41b19bcd26ace02ea591453735f2611b9d67f0ca8d33a6a76ac`  
		Last Modified: Tue, 12 Nov 2024 02:36:27 GMT  
		Size: 887.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca373d9063f10648f1962e81522d87b09e6b483b4946b477ca3c2bcb80b7a84d`  
		Last Modified: Wed, 13 Nov 2024 02:52:04 GMT  
		Size: 26.7 MB (26699998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46f15ebc8862260a1556c81c777121378189cd65ae3a29e9dd9612db647303ea`  
		Last Modified: Wed, 13 Nov 2024 02:52:04 GMT  
		Size: 13.5 MB (13487208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1bfe3530ba2cf580113b10a7b2040cf6b3c4439041c758ba8c9ba54ec8aed6e`  
		Last Modified: Wed, 13 Nov 2024 02:52:03 GMT  
		Size: 359.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c42a1cd4f1e40ba5249a2618649379dcf0b51b76fb08e525595e12dc7ed80407`  
		Last Modified: Wed, 13 Nov 2024 02:52:03 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e0dcae671c8b6a8b42c3416f4ee3f6cbb82a958f18dc05885926c0cc0957539`  
		Last Modified: Wed, 13 Nov 2024 02:52:04 GMT  
		Size: 19.2 KB (19154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b636730a505c5d29d80320dbe6413553de3f38e443edf03120797fe3ef979600`  
		Last Modified: Wed, 13 Nov 2024 02:52:04 GMT  
		Size: 26.7 MB (26746195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:704ff1f13a02ab85a6b7993177103aef8733a12b019fb94cbb77ec5fb709d120`  
		Last Modified: Wed, 13 Nov 2024 02:52:05 GMT  
		Size: 2.4 KB (2438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abd600e24cc3e691c854ed8fb0143a6c8e5c6ac27eb8c0ad5e4e5a8db0be3ea3`  
		Last Modified: Wed, 13 Nov 2024 02:52:05 GMT  
		Size: 1.7 KB (1729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.7-apache` - unknown; unknown

```console
$ docker pull wordpress@sha256:cb83bd0dc3c24469f0676dba40f9ef90b1cbabda6e28af7286fdcdd0b7392ede
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8162126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97dc6198e75c875c99aaa0356d860922c7f0c3f280f3b17c70a3f6eb421faac9`

```dockerfile
```

-	Layers:
	-	`sha256:404f8606499e605760927e608d6faf8ce91c5e250c99ddb303de30f32f26ae88`  
		Last Modified: Wed, 13 Nov 2024 02:52:03 GMT  
		Size: 8.1 MB (8098928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dcafb9c86ebc17ac3b67d2ff683e193964faf1439ce893e9fceedc9427c7a811`  
		Last Modified: Wed, 13 Nov 2024 02:52:03 GMT  
		Size: 63.2 KB (63198 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6.7-apache` - linux; mips64le

```console
$ docker pull wordpress@sha256:3b12f577ce8987ad62333f8d483a8fca2e23d4c51edacb87b96e52312ad5479e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.4 MB (218365506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e4a014f6643e6f0efae5ba32588e33bc7b9b7106b858e95f283ef400bcb2ae2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 24 Oct 2024 13:43:42 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
CMD ["bash"]
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 24 Oct 2024 13:43:42 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 24 Oct 2024 13:43:42 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_VERSION=8.2.25
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.25.tar.xz.asc
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_SHA256=330b54876ea1d05ade12ee9726167332058bccd58dffa1d4e12117f6b4f616b9
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 24 Oct 2024 13:43:42 GMT
STOPSIGNAL SIGWINCH
# Thu, 24 Oct 2024 13:43:42 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
WORKDIR /var/www/html
# Thu, 24 Oct 2024 13:43:42 GMT
EXPOSE map[80/tcp:{}]
# Thu, 24 Oct 2024 13:43:42 GMT
CMD ["apache2-foreground"]
# Mon, 11 Nov 2024 20:03:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 Nov 2024 20:03:11 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Mon, 11 Nov 2024 20:03:11 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Mon, 11 Nov 2024 20:03:11 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Mon, 11 Nov 2024 20:03:11 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Mon, 11 Nov 2024 20:03:11 GMT
RUN set -eux; 	version='6.7-RC5'; 	sha1='f3103a0adc6bd356ce743b6f0ad12d0be6f6ac36'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Mon, 11 Nov 2024 20:03:11 GMT
VOLUME [/var/www/html]
# Mon, 11 Nov 2024 20:03:11 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Mon, 11 Nov 2024 20:03:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 11 Nov 2024 20:03:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 11 Nov 2024 20:03:11 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:01c6d0bf10848996e396c89b66742849d41fd852c3610146badf9f612e62945b`  
		Last Modified: Tue, 12 Nov 2024 00:58:28 GMT  
		Size: 29.1 MB (29127365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:346c2177816783e9e289cf3372b166d07be052e7cc48f98690da6b177d62573f`  
		Last Modified: Tue, 12 Nov 2024 04:08:13 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd1c3070cec45196348f83431a430d224d58f2ae29c7f77034387a1da1bba0c0`  
		Last Modified: Tue, 12 Nov 2024 04:08:21 GMT  
		Size: 80.7 MB (80668697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d844fc4b81ddb360a025208b648de202ba45cd9113ce82fcab840d714a113030`  
		Last Modified: Tue, 12 Nov 2024 04:08:13 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3e3ea12fdbbab62c1af26697aefc532fc1af6a277566ab7f8e089e95811ac94`  
		Last Modified: Tue, 12 Nov 2024 04:28:45 GMT  
		Size: 20.1 MB (20069169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0f597baf51a1158f2bd7d1e67492508879d9f10f07022905b867a74f1563dca`  
		Last Modified: Tue, 12 Nov 2024 04:28:43 GMT  
		Size: 440.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1030ffb9a16f20c3ffe986bb80424e63d46a7e47d84a304997b65fbc6efb79e0`  
		Last Modified: Tue, 12 Nov 2024 04:28:43 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28d50a338c4a4762dd9ca62e556ccac8cabb2db396cda812be1d4ac9261be970`  
		Last Modified: Tue, 12 Nov 2024 09:03:21 GMT  
		Size: 12.3 MB (12253005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb0ac8109e1d1708997c2c85ce783eab19979adafdbabf22b569c9a725612297`  
		Last Modified: Tue, 12 Nov 2024 09:03:20 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ffa08f5c60ca3a2db8f20e7bce568cebad9beffd1b15d0b786b28c970389974`  
		Last Modified: Tue, 12 Nov 2024 09:03:21 GMT  
		Size: 10.5 MB (10490904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55683f82e8fdba9821be50995d9c27333453c8cd3b1b1431799f4f30bcf3b588`  
		Last Modified: Tue, 12 Nov 2024 09:03:20 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57b5797d5324a6e9ea751144d5b4239ffdc343219bc8c5902e2f411079074e19`  
		Last Modified: Tue, 12 Nov 2024 09:03:21 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3ecec9a69e862ee3f1f216286f4fa8aadfc3d64108e23ebeadf31c9e7bce1b5`  
		Last Modified: Tue, 12 Nov 2024 09:03:21 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d016b656c2519c6fcdfd1160afb6311c4b2f4be2b7d601fd657fe5b72394454`  
		Last Modified: Wed, 13 Nov 2024 01:13:50 GMT  
		Size: 26.0 MB (26025345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08dce1ff48ddbb07ba7bb6e5986a21121d9217d125ba7838e94cd42c295d96a5`  
		Last Modified: Wed, 13 Nov 2024 01:13:49 GMT  
		Size: 13.0 MB (12955237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53ad9d1f5c100264dd7e38016a8bce0f4fef6b210d184d456c8e1c259102af38`  
		Last Modified: Wed, 13 Nov 2024 01:13:47 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b09a3d1de35c3c1764bb0b6597df055c8d7bae43d13bf36539608ee0da46aa27`  
		Last Modified: Wed, 13 Nov 2024 01:13:47 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e294481a088027e939f1a18eb2e707e213a2a07dde714f3a3091d6407cd1365`  
		Last Modified: Wed, 13 Nov 2024 01:13:48 GMT  
		Size: 19.2 KB (19158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7923e2419602ebb8525d1f3544f0a35990d3d66804a7c22a1669e7ceb6c2c508`  
		Last Modified: Wed, 13 Nov 2024 01:51:14 GMT  
		Size: 26.7 MB (26746207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acdf8483e165a2f24c61cc71a05a89d6608b94ce6fb559c60f6b19513dc79182`  
		Last Modified: Wed, 13 Nov 2024 01:51:11 GMT  
		Size: 2.4 KB (2438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9cb4d58ee30253b3eb7beec8296ee68b55b5c93b79285442f9099cd54750b5b`  
		Last Modified: Wed, 13 Nov 2024 01:51:11 GMT  
		Size: 1.7 KB (1729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.7-apache` - unknown; unknown

```console
$ docker pull wordpress@sha256:8cf52591716a25a0b0956ae0b63a8e0e5715d7e13bd3db1f293094e3e5489b96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.3 KB (63266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a2434e9e0124591e1b94be1c844907123eb2d15fef981c33cbce6114b118b21`

```dockerfile
```

-	Layers:
	-	`sha256:07bb156b70bdb5cb40f5118ac727df74220b20540d004976e4be7bde94ed3a1b`  
		Last Modified: Wed, 13 Nov 2024 01:51:10 GMT  
		Size: 63.3 KB (63266 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6.7-apache` - linux; ppc64le

```console
$ docker pull wordpress@sha256:f4124badf9fd3d057c550f39be1e50fd23d36765a155a4bafedadfd4afa88d56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.6 MB (251580136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeccd8acb988b6b0c8ad9f3bb5340d68d733ebcb850a6e5d5f87a06a343dc29f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 24 Oct 2024 13:43:42 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
CMD ["bash"]
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 24 Oct 2024 13:43:42 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 24 Oct 2024 13:43:42 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_VERSION=8.2.25
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.25.tar.xz.asc
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_SHA256=330b54876ea1d05ade12ee9726167332058bccd58dffa1d4e12117f6b4f616b9
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 24 Oct 2024 13:43:42 GMT
STOPSIGNAL SIGWINCH
# Thu, 24 Oct 2024 13:43:42 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
WORKDIR /var/www/html
# Thu, 24 Oct 2024 13:43:42 GMT
EXPOSE map[80/tcp:{}]
# Thu, 24 Oct 2024 13:43:42 GMT
CMD ["apache2-foreground"]
# Mon, 11 Nov 2024 20:03:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 Nov 2024 20:03:11 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Mon, 11 Nov 2024 20:03:11 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Mon, 11 Nov 2024 20:03:11 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Mon, 11 Nov 2024 20:03:11 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Mon, 11 Nov 2024 20:03:11 GMT
RUN set -eux; 	version='6.7-RC5'; 	sha1='f3103a0adc6bd356ce743b6f0ad12d0be6f6ac36'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Mon, 11 Nov 2024 20:03:11 GMT
VOLUME [/var/www/html]
# Mon, 11 Nov 2024 20:03:11 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Mon, 11 Nov 2024 20:03:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 11 Nov 2024 20:03:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 11 Nov 2024 20:03:11 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:75e0ed8549227769329d9bb009b10ff68c47929fad577311f0d99115885347ef`  
		Last Modified: Tue, 12 Nov 2024 00:58:20 GMT  
		Size: 33.1 MB (33125353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b02cceb11c5f92ea5660ac6e0610c26c972c38dae66eeb9d41e3387390540062`  
		Last Modified: Tue, 12 Nov 2024 03:22:53 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c1d6ec9f7f7d2e7f8318e16194758fc58116d42583559cad4394fb117b2d735`  
		Last Modified: Tue, 12 Nov 2024 03:22:56 GMT  
		Size: 103.3 MB (103323960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e883340f45c1d0e36d2a728cca20410ca3254d93c803c062646dc430b8e41e7b`  
		Last Modified: Tue, 12 Nov 2024 03:22:53 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c2155f33ef158a9585945d382ada5e33cc0a6cb3faf942e6f840e0af8c0ef4e`  
		Last Modified: Tue, 12 Nov 2024 03:27:38 GMT  
		Size: 21.3 MB (21308382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69e7c3966720dc0d3b2f38f69d3927be83fe5fbd6d2d6ee5d45e6635cd22825b`  
		Last Modified: Tue, 12 Nov 2024 03:27:37 GMT  
		Size: 435.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6b76c10e03d21d789b97d145b294ce14e9afc78a7624eddb9a1e308056c07b3`  
		Last Modified: Tue, 12 Nov 2024 03:27:37 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2f3d6b5b94bf0aba00dd060df6cc08cbf6605d672478251206d151b0f039f5c`  
		Last Modified: Tue, 12 Nov 2024 05:51:50 GMT  
		Size: 12.3 MB (12254395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b953bb1f54caeeeac6b6c0b9c344c4d4ea88b7f7a2a4280761418ed46c6750`  
		Last Modified: Tue, 12 Nov 2024 05:51:49 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2370f407e506ef638034c515209285f4cf78c57a4e94c6ed3d9781251be6b513`  
		Last Modified: Tue, 12 Nov 2024 05:51:50 GMT  
		Size: 11.8 MB (11826833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db9471a72b72b9030689acfd28cb93fcb7f6f05ca40b1c193b4fff70b47f7ea9`  
		Last Modified: Tue, 12 Nov 2024 05:51:49 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25a4a6a153504d8db2f3e6384dd78cbd990c2fe97cc93e6426387ae19ad7956d`  
		Last Modified: Tue, 12 Nov 2024 05:51:50 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8533b29478ab357c0a26ae2e53e1e1ad8ff7ee87bf8176e3175a9e981f7c5364`  
		Last Modified: Tue, 12 Nov 2024 05:51:50 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e2b2646d5d2f4d8a11d9f437ff5604802b68a3e2a5fa8795bb71c6457f1af46`  
		Last Modified: Tue, 12 Nov 2024 15:34:03 GMT  
		Size: 27.3 MB (27337934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:755a833f89fa01a40c61c17c18ef9ffaabaf84ed39267b1d14d307de106b4f6d`  
		Last Modified: Tue, 12 Nov 2024 15:34:05 GMT  
		Size: 15.6 MB (15627513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:863a7bc29b59559e99e7d4cc91b11745347a67e53974257fabd15f791c01e95b`  
		Last Modified: Tue, 12 Nov 2024 15:34:02 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a87c3d6152f0e6d2309b8506b0e7fb6bfe30f924061c7d4ac4f6d144e442b03d`  
		Last Modified: Tue, 12 Nov 2024 15:34:02 GMT  
		Size: 391.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c201427f35e3dd09ba8dcf265f293eaee3fb70f460136f7e05c0594f514055b3`  
		Last Modified: Tue, 12 Nov 2024 15:34:03 GMT  
		Size: 19.2 KB (19179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da12d0b03fdb532b5e50066b24d74381084099a4b1793f57411bb5055059b31a`  
		Last Modified: Wed, 13 Nov 2024 00:04:37 GMT  
		Size: 26.7 MB (26746186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e858d79e4fc6002f0efcbb953ee526e4d18c2db19b1f1941487f88361f3d8c3`  
		Last Modified: Wed, 13 Nov 2024 00:04:36 GMT  
		Size: 2.4 KB (2438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2f1afc2043bd0b73290c132d6a93edac6f6346675f64df527d14e2d7099aa5f`  
		Last Modified: Wed, 13 Nov 2024 00:04:36 GMT  
		Size: 1.7 KB (1729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.7-apache` - unknown; unknown

```console
$ docker pull wordpress@sha256:d39b4cb95e6fb9f0244f414722ad1d706f5170b9b6c8d0e7007ad36b5773684e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8168068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e457932f6e598322f3e5470360d19610531efd15dd9c69a55f9f5e79f3553dae`

```dockerfile
```

-	Layers:
	-	`sha256:f523652b7e02811b539b7822da7897d1c9417dd3309b75715796ac1181f89192`  
		Last Modified: Wed, 13 Nov 2024 00:04:36 GMT  
		Size: 8.1 MB (8104641 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68dec49472b6feae1d1a96cd145ee16fc471372be08570e0a61e524366a1e72c`  
		Last Modified: Wed, 13 Nov 2024 00:04:35 GMT  
		Size: 63.4 KB (63427 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6.7-apache` - linux; s390x

```console
$ docker pull wordpress@sha256:597fe1f56d1fddfd468a3953d7105c1c1ca071a3d74716d68891870c35a94e08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.2 MB (217238865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c258d3152e1806684e96f145dfa0b47edb4bb27a790f6a2dc21c7ce5e0a1939`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 24 Oct 2024 13:43:42 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
CMD ["bash"]
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 24 Oct 2024 13:43:42 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 24 Oct 2024 13:43:42 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_VERSION=8.2.25
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.25.tar.xz.asc
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_SHA256=330b54876ea1d05ade12ee9726167332058bccd58dffa1d4e12117f6b4f616b9
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 24 Oct 2024 13:43:42 GMT
STOPSIGNAL SIGWINCH
# Thu, 24 Oct 2024 13:43:42 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
WORKDIR /var/www/html
# Thu, 24 Oct 2024 13:43:42 GMT
EXPOSE map[80/tcp:{}]
# Thu, 24 Oct 2024 13:43:42 GMT
CMD ["apache2-foreground"]
# Mon, 11 Nov 2024 20:03:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 Nov 2024 20:03:11 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Mon, 11 Nov 2024 20:03:11 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Mon, 11 Nov 2024 20:03:11 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Mon, 11 Nov 2024 20:03:11 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Mon, 11 Nov 2024 20:03:11 GMT
RUN set -eux; 	version='6.7-RC5'; 	sha1='f3103a0adc6bd356ce743b6f0ad12d0be6f6ac36'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Mon, 11 Nov 2024 20:03:11 GMT
VOLUME [/var/www/html]
# Mon, 11 Nov 2024 20:03:11 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Mon, 11 Nov 2024 20:03:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 11 Nov 2024 20:03:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 11 Nov 2024 20:03:11 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:fa8cb447c1a4d7decc9cbf4223b78597699fc7980d77431c085cd6cf32c5b3ed`  
		Last Modified: Tue, 12 Nov 2024 00:59:17 GMT  
		Size: 27.5 MB (27491628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:557ec8c9288f91e0e914bc88a84e7f99c5caf8f6d9840288a739773c38a7c07a`  
		Last Modified: Tue, 12 Nov 2024 03:15:05 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c26af4e0d7a3fb552ad3968a1cee38ccd36f353e2162832fca3623342e7ab8a`  
		Last Modified: Tue, 12 Nov 2024 03:15:07 GMT  
		Size: 80.8 MB (80817024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36392fa6e835e08d294727ebd2c1c3a2bb6f80d6dc6273a5056d2f6ed2c1ffed`  
		Last Modified: Tue, 12 Nov 2024 03:15:05 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e54e67acbced0cb69e2dc640f712d45dcfa623c348b09bd75ae63c1818f0129f`  
		Last Modified: Tue, 12 Nov 2024 03:20:14 GMT  
		Size: 19.9 MB (19895214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5427c8084a617f516431588d36205b585b6e003a7c6f3326454cc9e4e520946`  
		Last Modified: Tue, 12 Nov 2024 03:20:13 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abd0bc1eddda7a2174cecf32a39f30306b749d6521c2b41823a1b05b41eef6f9`  
		Last Modified: Tue, 12 Nov 2024 03:20:13 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3045792d7daeaa7d40702a0f202dd4f51e513c1910095051fa218af2b912703`  
		Last Modified: Tue, 12 Nov 2024 06:22:13 GMT  
		Size: 12.3 MB (12253536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03580c8e2e52a438759c088b169dddf5c4f5dfe03921ab767b930b5fd13527c5`  
		Last Modified: Tue, 12 Nov 2024 06:22:13 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf8a0d82e5993a8a7e949ce2fba4f13a19cb4d33696f21c8501dfc31055478bc`  
		Last Modified: Tue, 12 Nov 2024 06:22:14 GMT  
		Size: 10.6 MB (10644710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c9953170bd68c9a1d28d8cff26ed13b1e023d89398d3b23d4c34d4965bcad2`  
		Last Modified: Tue, 12 Nov 2024 06:22:13 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82b5ca5b3fb692d59f13a93a6c0f3198b164d597816fcde527bd1538ad39a9a2`  
		Last Modified: Tue, 12 Nov 2024 06:22:14 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3142c1f502be74edfb0f59194ffd1be8da1f810c954117cba27367a3cd9a5329`  
		Last Modified: Tue, 12 Nov 2024 06:22:14 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a20e9ee065b71f367fe3d38a28f5322cf8259cf927af9bb0d02c199ee15c288`  
		Last Modified: Tue, 12 Nov 2024 23:00:11 GMT  
		Size: 25.9 MB (25898985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1315168ca762460398ddc1edf56d9239c1a871d3c958b5faf726c0bd53279641`  
		Last Modified: Tue, 12 Nov 2024 23:00:12 GMT  
		Size: 13.5 MB (13462013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8245ab70d2d6fbedae14f3762234c1de36b7cf74898ebccabf223e917813f2e7`  
		Last Modified: Tue, 12 Nov 2024 23:00:11 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:133eb1afdcea6451fd49f0b716930dee4842d23d7222d463d1bf395cf1cd2788`  
		Last Modified: Tue, 12 Nov 2024 23:00:11 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4f48a990c8aadd7db80f45f7bb931e324b641193ccc2a47b503579b4641bf31`  
		Last Modified: Tue, 12 Nov 2024 23:00:12 GMT  
		Size: 19.2 KB (19162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17eef68ca6a7dbd41af2e7ca82729e274d71ebb1f150fd94f405dcab68ac9f29`  
		Last Modified: Tue, 12 Nov 2024 23:21:36 GMT  
		Size: 26.7 MB (26746183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd0ddb969987322a9fd951739a5455c7f55a807959b4945c7c9d4103d5991606`  
		Last Modified: Tue, 12 Nov 2024 23:21:35 GMT  
		Size: 2.4 KB (2437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:145c96a723b0fde9ce18d8d176caecb474996e4f042324834097dc6246ea54e4`  
		Last Modified: Tue, 12 Nov 2024 23:21:35 GMT  
		Size: 1.7 KB (1730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.7-apache` - unknown; unknown

```console
$ docker pull wordpress@sha256:693cb46e35a9d30c259fbb3bcf99c7ce086c1a86df37d49a85e78cdc054116e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (8018921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d3dc5a58f971fdbcec84098284cdfac5d00a89e1bdf53491fe3e68c51a2f8e5`

```dockerfile
```

-	Layers:
	-	`sha256:1b9237964a4f9c46a3bef3b8f365b4609564065299c3457db2d0476bb2ae7f42`  
		Last Modified: Tue, 12 Nov 2024 23:21:35 GMT  
		Size: 8.0 MB (7955629 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05c843c7417cb5ffed8862e4cb50ca065caee306cf19930a08052e4f5d421d2d`  
		Last Modified: Tue, 12 Nov 2024 23:21:34 GMT  
		Size: 63.3 KB (63292 bytes)  
		MIME: application/vnd.in-toto+json
