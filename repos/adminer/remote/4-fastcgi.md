## `adminer:4-fastcgi`

```console
$ docker pull adminer@sha256:17a57b649aca6899d2486fe797d13f9c92dc77d20eb38b189b1bf944dff758b6
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

### `adminer:4-fastcgi` - linux; amd64

```console
$ docker pull adminer@sha256:d28113abed8c078df894e4896fd5f893b059915bb14d9a1b30470a8877b353e7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.0 MB (95963610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9c81ff724cfc6975d1e2eb0f1eec88407c1ac7adbe9c36237a5e7f5b8886570`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:32 GMT
ADD file:1bf1a123da85382e70ea251091b98fd8b4a1972e4c4e84d392443a4e20b7a135 in / 
# Tue, 13 Feb 2024 00:37:32 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:41:55 GMT
STOPSIGNAL SIGINT
# Tue, 13 Feb 2024 01:42:15 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 01:42:16 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 13 Feb 2024 01:42:37 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Tue, 13 Feb 2024 01:42:37 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 13 Feb 2024 01:42:37 GMT
WORKDIR /var/www/html
# Tue, 13 Feb 2024 01:42:37 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 13 Feb 2024 01:42:37 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 13 Feb 2024 01:42:38 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 13 Feb 2024 01:42:38 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 13 Feb 2024 01:42:48 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 13 Feb 2024 01:42:48 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 13 Feb 2024 01:42:48 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 13 Feb 2024 01:42:48 GMT
USER adminer
# Tue, 13 Feb 2024 01:42:49 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:09e2bc8a597c33b54cccaf52f2e21798e2e0df79ab6cb33d3b1dfd4b33a57512`  
		Last Modified: Tue, 13 Feb 2024 00:42:21 GMT  
		Size: 55.1 MB (55084838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:092a59d5d6497166f3dbba32aa205aaa78ddfd080243695a000fc05b7988d184`  
		Last Modified: Tue, 13 Feb 2024 01:43:08 GMT  
		Size: 39.5 MB (39486506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4dca1b56763151283fbe5bc268620ccb9bca392661422e8628f497c3b6863dc`  
		Last Modified: Tue, 13 Feb 2024 01:43:01 GMT  
		Size: 385.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d4d7fd85b75db139e89404e6e2708b299ec3e93c580cb5d42fa86bf3d3e8162`  
		Last Modified: Tue, 13 Feb 2024 01:43:25 GMT  
		Size: 2.7 KB (2704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23113510534223fbf69e7de3334db9652a1692b84f625da69791cbe19b03d4ff`  
		Last Modified: Tue, 13 Feb 2024 01:43:25 GMT  
		Size: 1.9 KB (1875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea25210f26a47784c1ca191c5b8b5c616e5354c46e70ab6512199353b8f99328`  
		Last Modified: Tue, 13 Feb 2024 01:43:24 GMT  
		Size: 1.5 KB (1476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08d0134361a716638c099177b20ecb0ccd4ce918335138861225f90a626e9475`  
		Last Modified: Tue, 13 Feb 2024 01:43:25 GMT  
		Size: 1.4 MB (1385337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aad5456ea85af8d929b8c9d0508f459b22f47414329a6b931b476da1ef933d5d`  
		Last Modified: Tue, 13 Feb 2024 01:43:24 GMT  
		Size: 489.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-fastcgi` - linux; arm variant v5

```console
$ docker pull adminer@sha256:c17762f6e86926f2da1191afe8f17828009a3eb7dc656e858997c634c91e4bed
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91226474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d154ab9bacf27a2754912a3ca1a6e2bb16611ec332250ac2a69ee9196cd3542`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Tue, 12 Mar 2024 00:48:38 GMT
ADD file:e13a63ed3af4c4dcb74dfa2a2b12a285563b8c905dbac41b538492e1e100f93e in / 
# Tue, 12 Mar 2024 00:48:39 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 07:59:47 GMT
STOPSIGNAL SIGINT
# Tue, 12 Mar 2024 08:00:28 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 08:00:29 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 12 Mar 2024 08:00:56 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Tue, 12 Mar 2024 08:00:57 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 12 Mar 2024 08:00:58 GMT
WORKDIR /var/www/html
# Tue, 12 Mar 2024 08:00:58 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 12 Mar 2024 08:00:58 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 12 Mar 2024 08:00:58 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 12 Mar 2024 08:00:58 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 12 Mar 2024 08:01:13 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 12 Mar 2024 08:01:13 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 12 Mar 2024 08:01:13 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 12 Mar 2024 08:01:13 GMT
USER adminer
# Tue, 12 Mar 2024 08:01:13 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:57e872a0ca7dbab84f7804705a96154de6b3cffcdb4f8946d4387764bfc1e307`  
		Last Modified: Tue, 12 Mar 2024 00:52:01 GMT  
		Size: 52.6 MB (52586778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f46fef05abde7f7546bcf6aa4a5a743326f0406fa97e4cdca50db8a1c65a8ff2`  
		Last Modified: Tue, 12 Mar 2024 08:01:33 GMT  
		Size: 37.2 MB (37247610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c104cb471832f6d326ad627fa96dc2c1e597161ea2e40b7971d631f9ffaf0bb`  
		Last Modified: Tue, 12 Mar 2024 08:01:23 GMT  
		Size: 389.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21fbf64549049afc57d96068f6af3a2304a5daddaf30c4cde8f8260909f3e281`  
		Last Modified: Tue, 12 Mar 2024 08:01:49 GMT  
		Size: 2.7 KB (2704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55abab9cf948fccf6fb7971e8bfd16f05bb265e27e05a36013c076f37fb64f78`  
		Last Modified: Tue, 12 Mar 2024 08:01:49 GMT  
		Size: 1.9 KB (1869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:144bd14e9da7c16ade662df6840f0abd0c8970d19e7697279dd530cc11fe89da`  
		Last Modified: Tue, 12 Mar 2024 08:01:49 GMT  
		Size: 1.5 KB (1479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b44d39f4bb553c0cc5630fdbfeaa2bd4ae4aa39a5d30f0b412244aa2fc7eabf`  
		Last Modified: Tue, 12 Mar 2024 08:01:49 GMT  
		Size: 1.4 MB (1385154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9790629095a1fcb4a80cd8e6f741ec8948c2fda044e91ff3ab712c57aaa65ee`  
		Last Modified: Tue, 12 Mar 2024 08:01:49 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-fastcgi` - linux; arm variant v7

```console
$ docker pull adminer@sha256:f6b508b9bfdff34b2bd3447e4305aa412b4909d8018301fe07d5b538c28f9f37
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.8 MB (87821972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b35e05077810d15d73e29531e8fcf8328b3f51e87ed6ccc3f7c551a29b6c1ce`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Tue, 12 Mar 2024 00:59:25 GMT
ADD file:477c339ed6ec658bb1d0025e1568290c3cbbc98d9f973379f3133b83c2de9128 in / 
# Tue, 12 Mar 2024 00:59:28 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:31:44 GMT
STOPSIGNAL SIGINT
# Tue, 12 Mar 2024 02:32:09 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:32:10 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 12 Mar 2024 02:32:32 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Tue, 12 Mar 2024 02:32:33 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 12 Mar 2024 02:32:33 GMT
WORKDIR /var/www/html
# Tue, 12 Mar 2024 02:32:33 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 12 Mar 2024 02:32:33 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 12 Mar 2024 02:32:33 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 12 Mar 2024 02:32:33 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 12 Mar 2024 02:32:44 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 12 Mar 2024 02:32:44 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 12 Mar 2024 02:32:45 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 12 Mar 2024 02:32:45 GMT
USER adminer
# Tue, 12 Mar 2024 02:32:45 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:ab40cb80ac5229a1c48dfbfe9aaa04da29109444982d90d4bca2c7b6842beceb`  
		Last Modified: Tue, 12 Mar 2024 01:03:56 GMT  
		Size: 50.2 MB (50241442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7327478c4231aa77cf7cab36cd2f0c3c0f9a6db93dfbf55e5c90cde6524bbe9`  
		Last Modified: Tue, 12 Mar 2024 02:33:03 GMT  
		Size: 36.2 MB (36188441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e35d66055a894a3e6c6467b18c4eebfaae710cf56b2c0aa6de4cc2ecd1e0f31e`  
		Last Modified: Tue, 12 Mar 2024 02:32:55 GMT  
		Size: 390.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bee49a2db0d3c135ef774852c3476c0117046cece39866928abccfbb6d89516`  
		Last Modified: Tue, 12 Mar 2024 02:33:19 GMT  
		Size: 2.7 KB (2705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2a68753fd1a5b95981a8e725e07594817149860234cf08a6c72982309f5dfaa`  
		Last Modified: Tue, 12 Mar 2024 02:33:19 GMT  
		Size: 1.9 KB (1865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae1d24282261b1c527abba2546a90f56c72673631fc468aa8808caaf29f8deb4`  
		Last Modified: Tue, 12 Mar 2024 02:33:19 GMT  
		Size: 1.5 KB (1477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba4327ab62557159df86a4df635237bb44d72aa72a89e3d1e34e13fbb09d3b6a`  
		Last Modified: Tue, 12 Mar 2024 02:33:19 GMT  
		Size: 1.4 MB (1385161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a678196d0acfc041a18aaf167b01d4aebc34ed3f32a684da110f54cacb51161`  
		Last Modified: Tue, 12 Mar 2024 02:33:19 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-fastcgi` - linux; arm64 variant v8

```console
$ docker pull adminer@sha256:2d0406dfc294b569c429cdafeffed87e5a14f88261afa83d557725ae05ca6cc6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94356071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f93bc82986c16e335325ac6b099535e2e7597fc6b5ea037e04d908ca499fe20`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:43 GMT
ADD file:7cb312b5f676a37f5c3172be6eb95e30986e5da0dcf21985d2176f8a9a037012 in / 
# Tue, 12 Mar 2024 00:45:44 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:22:42 GMT
STOPSIGNAL SIGINT
# Tue, 12 Mar 2024 01:23:03 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:23:04 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 12 Mar 2024 01:23:23 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Tue, 12 Mar 2024 01:23:24 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 12 Mar 2024 01:23:24 GMT
WORKDIR /var/www/html
# Tue, 12 Mar 2024 01:23:24 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 12 Mar 2024 01:23:24 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 12 Mar 2024 01:23:24 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 12 Mar 2024 01:23:24 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 12 Mar 2024 01:23:34 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 12 Mar 2024 01:23:34 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 12 Mar 2024 01:23:34 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 12 Mar 2024 01:23:34 GMT
USER adminer
# Tue, 12 Mar 2024 01:23:34 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:f53ee134f2f58aa9d86f682cbedb185619a5b857474f430e6dc3384fafdec81c`  
		Last Modified: Tue, 12 Mar 2024 00:49:12 GMT  
		Size: 53.7 MB (53722099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:736b482dff10e5ae34b256f9ed0b77b11b5035086d16b5d83dd547493a421e25`  
		Last Modified: Tue, 12 Mar 2024 01:23:50 GMT  
		Size: 39.2 MB (39241856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fbc285c8fa7ada768fea15139bd3696c7a85037ad5509364ca3cc8edd38e1ed`  
		Last Modified: Tue, 12 Mar 2024 01:23:44 GMT  
		Size: 393.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c065ab672aedcf271867add807cd754a9c3479702c1422596e28ce96e3101cd`  
		Last Modified: Tue, 12 Mar 2024 01:24:10 GMT  
		Size: 2.7 KB (2712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:166ee9a9591ad6275a9a62c82ea0533803d94a4b2e1d3d301a42a528b1d782cf`  
		Last Modified: Tue, 12 Mar 2024 01:24:11 GMT  
		Size: 1.9 KB (1880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:961400d283e2e480a569750eef0c9e91343bfa839aa3a52184e76618a4c13f9d`  
		Last Modified: Tue, 12 Mar 2024 01:24:10 GMT  
		Size: 1.5 KB (1476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceb6f10f5bdc90a7e6105f37b0d1fe2b40fc2c36a13659e8df1ce80d57e18fc6`  
		Last Modified: Tue, 12 Mar 2024 01:24:11 GMT  
		Size: 1.4 MB (1385164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a26fec7a41f602aaa9dc121d12f62dd388eed56ccb7a8061a471cc9dddc40548`  
		Last Modified: Tue, 12 Mar 2024 01:24:11 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-fastcgi` - linux; 386

```console
$ docker pull adminer@sha256:58b6b828b589bcc3fa5db8e9f29ab014dbbe3625e7f88409ad45256882ac662d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.0 MB (97007574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8a04dc3fdec32b0ce90dff040a1cce3c6fec24c01e2b1012548fd4cebaa7139`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Tue, 12 Mar 2024 00:58:12 GMT
ADD file:e7e92b37650e4d33c3374ca47bc378c2b4e15f7c7e0a7c7fc659a29c5b3fc583 in / 
# Tue, 12 Mar 2024 00:58:12 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 07:37:48 GMT
STOPSIGNAL SIGINT
# Tue, 12 Mar 2024 07:38:20 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 07:38:21 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 12 Mar 2024 07:38:47 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Tue, 12 Mar 2024 07:38:47 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 12 Mar 2024 07:38:48 GMT
WORKDIR /var/www/html
# Tue, 12 Mar 2024 07:38:48 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 12 Mar 2024 07:38:48 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 12 Mar 2024 07:38:48 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 12 Mar 2024 07:38:48 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 12 Mar 2024 07:39:01 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 12 Mar 2024 07:39:01 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 12 Mar 2024 07:39:01 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 12 Mar 2024 07:39:01 GMT
USER adminer
# Tue, 12 Mar 2024 07:39:01 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:ec2ed44737cc768246d63628c6de48f2d223cdb3a6c218bddd11786679e34647`  
		Last Modified: Tue, 12 Mar 2024 01:03:04 GMT  
		Size: 56.1 MB (56057973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b5b8a89beb8d9af3fd72c598548b86fb747e74608c80010d9da412be22ad3f1`  
		Last Modified: Tue, 12 Mar 2024 07:39:25 GMT  
		Size: 39.6 MB (39557502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0deeb7243b1ff117bee9da35536cde769f37e39536a2bc1403cc939fcaa09deb`  
		Last Modified: Tue, 12 Mar 2024 07:39:15 GMT  
		Size: 391.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dafc0ba62aab0544a852057ed00a36411255a0d21b0696a36f8db99876a8196c`  
		Last Modified: Tue, 12 Mar 2024 07:39:41 GMT  
		Size: 2.7 KB (2706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a14b1d7c777a17a8ecc5cae84f5e195c8ca006849a350bee4ee1d6740770a04b`  
		Last Modified: Tue, 12 Mar 2024 07:39:41 GMT  
		Size: 1.9 KB (1870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebc948737c030d56e4d134f0f42f7c91334f11fe8ed2f937af45578c7b1d9c3e`  
		Last Modified: Tue, 12 Mar 2024 07:39:41 GMT  
		Size: 1.5 KB (1481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99f6e1786737954182a2c7dbc86b47207398bceb2e56f8607b7b9ba7dbd09784`  
		Last Modified: Tue, 12 Mar 2024 07:39:42 GMT  
		Size: 1.4 MB (1385161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:373790c68066b4a0aebd1b1690282b06d190d3193535ab6977159e22a890ee95`  
		Last Modified: Tue, 12 Mar 2024 07:39:41 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-fastcgi` - linux; mips64le

```console
$ docker pull adminer@sha256:3f5166c64b93eac34fa57225abd35ba78c4dab69304cce9cc7faeeddc7636eb6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.6 MB (92649513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87d398abc6f15784ae84fb73a4ec7cb27028088f0ce0dfef563c958698baa4b9`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Tue, 12 Mar 2024 01:06:53 GMT
ADD file:ceaac889009e9d867969b5a568939eb0f6e136303e3438d9747193d6ef4755ab in / 
# Tue, 12 Mar 2024 01:06:58 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:57:07 GMT
STOPSIGNAL SIGINT
# Tue, 12 Mar 2024 01:59:04 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:59:10 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 12 Mar 2024 02:00:54 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Tue, 12 Mar 2024 02:01:00 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 12 Mar 2024 02:01:04 GMT
WORKDIR /var/www/html
# Tue, 12 Mar 2024 02:01:07 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 12 Mar 2024 02:01:10 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 12 Mar 2024 02:01:13 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 12 Mar 2024 02:01:17 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 12 Mar 2024 02:02:06 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 12 Mar 2024 02:02:09 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 12 Mar 2024 02:02:12 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 12 Mar 2024 02:02:15 GMT
USER adminer
# Tue, 12 Mar 2024 02:02:19 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:3856c0b5cf8a29fd86ef6fe0c2a36a38020518c2e120457769b9044974ec1ca8`  
		Last Modified: Tue, 12 Mar 2024 01:17:56 GMT  
		Size: 53.3 MB (53303519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10cec6da94bd0c183de93bb08aac547c356f09e634431834b4dfd1df66fd16c7`  
		Last Modified: Tue, 12 Mar 2024 02:03:08 GMT  
		Size: 38.0 MB (37952997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5c8e5180951d1e6bd7af5bdc785b54eea4aa18aee55ac41064a79a214bd0fdb`  
		Last Modified: Tue, 12 Mar 2024 02:02:41 GMT  
		Size: 393.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6917c74f4d5a02cf99c55e45a598935f287cf0a8e3e5e4621f2658090bf02ff3`  
		Last Modified: Tue, 12 Mar 2024 02:03:29 GMT  
		Size: 2.7 KB (2714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9259c7e32ec0610a362cb19b3627732aeb10af656efde1a15d1601e25e98714a`  
		Last Modified: Tue, 12 Mar 2024 02:03:28 GMT  
		Size: 1.7 KB (1729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99a77f80a795b470a3891f03deba5cdf5863422cdc5fc6fe9f70fd5533539c0d`  
		Last Modified: Tue, 12 Mar 2024 02:03:28 GMT  
		Size: 1.5 KB (1481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0960bf25611bef45f61bad1fefa78f8ce34efe28ec1c4a20645f55e56b0ed9f`  
		Last Modified: Tue, 12 Mar 2024 02:03:29 GMT  
		Size: 1.4 MB (1386188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:044fddadfc3de083c87ec7ec5e4a7273f251a9c16726902e5a0c94719a4f9d6d`  
		Last Modified: Tue, 12 Mar 2024 02:03:28 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-fastcgi` - linux; ppc64le

```console
$ docker pull adminer@sha256:75cb6723066bc445a093230f3a83fb22cec22d4e29d7330f06a4cc9f5eb6fe27
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.3 MB (101290249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84aba149a57f559e96e7ec7060e927ce4f21e3f035021929590dbf3e155a7157`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Tue, 13 Feb 2024 00:39:15 GMT
ADD file:de34873811ec1071766dcf77b8d1180714c8e5b4373bed3aaf9a9e742ade2fee in / 
# Tue, 13 Feb 2024 00:39:19 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:24:00 GMT
STOPSIGNAL SIGINT
# Tue, 13 Feb 2024 01:24:58 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 01:25:01 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 13 Feb 2024 01:25:41 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Tue, 13 Feb 2024 01:25:43 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 13 Feb 2024 01:25:43 GMT
WORKDIR /var/www/html
# Tue, 13 Feb 2024 01:25:43 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 13 Feb 2024 01:25:44 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 13 Feb 2024 01:25:44 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 13 Feb 2024 01:25:45 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 13 Feb 2024 01:26:13 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 13 Feb 2024 01:26:14 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 13 Feb 2024 01:26:14 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 13 Feb 2024 01:26:15 GMT
USER adminer
# Tue, 13 Feb 2024 01:26:15 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:5b3ca2d45f6b2df666b88854e431316a856c6ecacdd29894dd599694e415a1eb`  
		Last Modified: Tue, 13 Feb 2024 00:44:22 GMT  
		Size: 59.0 MB (58954488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e029c5ea562dd6d357c1bed2443ac90c451b2253527daa6b56663826d249ad4e`  
		Last Modified: Tue, 13 Feb 2024 01:26:39 GMT  
		Size: 40.9 MB (40943323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e511f8603016ae4f5e261cad68ea477938c886b5b18dfc125a8e3bb6bce7c957`  
		Last Modified: Tue, 13 Feb 2024 01:26:30 GMT  
		Size: 394.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f54d0a62eae31c4f851c40064233ea2c6fa2083cf333c1f24c2373d7d6bde0c`  
		Last Modified: Tue, 13 Feb 2024 01:26:58 GMT  
		Size: 2.7 KB (2711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b807d644533a1fcdb998c6cde83baee0987405fc18ce0d0b0530821f827a2a32`  
		Last Modified: Tue, 13 Feb 2024 01:26:59 GMT  
		Size: 1.9 KB (1876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d145477c056c49656d4d8d43c44c4d23e789824f4556a660086d2fd74663bf14`  
		Last Modified: Tue, 13 Feb 2024 01:26:59 GMT  
		Size: 1.5 KB (1481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25bc73e2f6682fe4e9e4a1d02776c429ab8762b6166af224085b917061eb575c`  
		Last Modified: Tue, 13 Feb 2024 01:26:59 GMT  
		Size: 1.4 MB (1385486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcdc434056eba16c2adda5ec5b456b26100a38e758d86390888e3590df705494`  
		Last Modified: Tue, 13 Feb 2024 01:26:59 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-fastcgi` - linux; s390x

```console
$ docker pull adminer@sha256:19bfecedaf3b31ac4beec0dfeca9edc9673e00db5a0c2c30dbdcd172745951a3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.7 MB (93736780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1afcb9e8ba854d9f228d398aaa8a9f0e7519e8ef2d09c6b76cbb9502f0ba698`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Tue, 13 Feb 2024 01:03:43 GMT
ADD file:baaec0dbf612f7bd9d783527a940d73b2148b2ceb1e6770a7be62a51d3bc72e8 in / 
# Tue, 13 Feb 2024 01:03:46 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 04:16:26 GMT
STOPSIGNAL SIGINT
# Tue, 13 Feb 2024 04:16:54 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 04:17:03 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 13 Feb 2024 04:18:32 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Tue, 13 Feb 2024 04:18:33 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 13 Feb 2024 04:18:34 GMT
WORKDIR /var/www/html
# Tue, 13 Feb 2024 04:18:34 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 13 Feb 2024 04:18:34 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 13 Feb 2024 04:18:34 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 13 Feb 2024 04:18:35 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 13 Feb 2024 04:18:43 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 13 Feb 2024 04:18:43 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 13 Feb 2024 04:18:43 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 13 Feb 2024 04:18:44 GMT
USER adminer
# Tue, 13 Feb 2024 04:18:44 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:75a00755bfcec7b096a7f2fdb8374002f3bbc7076571213a985c40116dbabb6a`  
		Last Modified: Tue, 13 Feb 2024 01:30:37 GMT  
		Size: 53.3 MB (53319325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:112506421ca98b25ac74bb82254c5406cab8eea61fb8d62db39073657f432759`  
		Last Modified: Tue, 13 Feb 2024 04:20:04 GMT  
		Size: 39.0 MB (39025245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c10724d9fbf328dd1ef3e8442af2f41eb0a3c6b7026b365af89ae6404d73c7cf`  
		Last Modified: Tue, 13 Feb 2024 04:19:56 GMT  
		Size: 389.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbb230daa063110f35c8ae0c02aa217c5fcf75310c373172517e9bb4331ea4ce`  
		Last Modified: Tue, 13 Feb 2024 04:20:16 GMT  
		Size: 2.7 KB (2711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e735a1f84dd0780fe284ed8c9afcd03f85822338ccb1338f50c485a1f28fb975`  
		Last Modified: Tue, 13 Feb 2024 04:20:15 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:432fde1b36db23cf33dca2e72a21f8b29a37e619e4db9ecc851b43ffb1bd9527`  
		Last Modified: Tue, 13 Feb 2024 04:20:16 GMT  
		Size: 1.5 KB (1481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a79f04f1649950e2fa3c7995f15cb64086b2694b421a4b73e3c569d3b8c24160`  
		Last Modified: Tue, 13 Feb 2024 04:20:16 GMT  
		Size: 1.4 MB (1385260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c345bc0deb437375d968de8d5a66579a13343c4d36c2500b2f91b1f5007de74`  
		Last Modified: Tue, 13 Feb 2024 04:20:15 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
