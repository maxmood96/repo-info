## `adminer:4-fastcgi`

```console
$ docker pull adminer@sha256:090619aa58c1739ec0f38ee5b5389d54b930e6a9fe10444ffba850aaedd3c7b9
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
$ docker pull adminer@sha256:a9df20e7d9358082caee7a84655e5f724f8f86ad68af0c279f84dae1a00a6485
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91226590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cca97e195509abd9d549c4402f99e69eea7651af15ba03ebcfb3ba73b4cbee4e`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Tue, 13 Feb 2024 01:08:36 GMT
ADD file:e60f5be11728cbf36bc5b1ee8a186ec55fb8e6bbc13d939c76ff03e91e934e90 in / 
# Tue, 13 Feb 2024 01:08:37 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:59:44 GMT
STOPSIGNAL SIGINT
# Tue, 13 Feb 2024 02:00:54 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 02:00:55 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 13 Feb 2024 02:01:40 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Tue, 13 Feb 2024 02:01:42 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 13 Feb 2024 02:01:42 GMT
WORKDIR /var/www/html
# Tue, 13 Feb 2024 02:01:42 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 13 Feb 2024 02:01:43 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 13 Feb 2024 02:01:43 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 13 Feb 2024 02:01:44 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 13 Feb 2024 02:02:08 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 13 Feb 2024 02:02:09 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 13 Feb 2024 02:02:09 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 13 Feb 2024 02:02:09 GMT
USER adminer
# Tue, 13 Feb 2024 02:02:10 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:bbf2c22df990ef0a734a6681b9078a2b5c2ea21e9fee5c8e62c2171859d433d8`  
		Last Modified: Tue, 13 Feb 2024 01:13:53 GMT  
		Size: 52.6 MB (52586881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03ddd64715bfc7a52ee47ef33638aa50b6ddc9a1e9f7bf68b142adf6d33cf3d6`  
		Last Modified: Tue, 13 Feb 2024 02:02:41 GMT  
		Size: 37.2 MB (37247477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:804bae3b0b7a6e38bf57f209d3381cca9d6b31c79e63ef481710d5c6b1241eb8`  
		Last Modified: Tue, 13 Feb 2024 02:02:30 GMT  
		Size: 396.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba72ef4891afa65033f077583125f2a567b7d303b0d47144b0cd508c232149af`  
		Last Modified: Tue, 13 Feb 2024 02:03:00 GMT  
		Size: 2.7 KB (2715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd187af8c4c73db2ed7fc9d61e819efb94037b0b2b4a9e1e3f9ebd4c126bf0a7`  
		Last Modified: Tue, 13 Feb 2024 02:03:01 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9a654901e8777f826a23c9bf1130f37432964a1f4f5fd56ba34b85fe4e1bbd8`  
		Last Modified: Tue, 13 Feb 2024 02:03:00 GMT  
		Size: 1.5 KB (1479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:057057fe29b09937c0488965edbfeb8be5a95cc731d3b5081a5778a199eb7e23`  
		Last Modified: Tue, 13 Feb 2024 02:03:01 GMT  
		Size: 1.4 MB (1385287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ce762ae8f2845834472698a4acb11f4791e559353adbb9f5f76b61751eb3694`  
		Last Modified: Tue, 13 Feb 2024 02:03:00 GMT  
		Size: 489.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-fastcgi` - linux; arm variant v7

```console
$ docker pull adminer@sha256:ab64a2f7442fd1008aa4dc8736baad63a4aabf0ef6f6b15b3bf6db2af1c52e83
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.8 MB (87822422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02a69aa1611a0d605b9c42ea1ca3a966781d73dfe1abff127737a624a09c9e2f`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Tue, 13 Feb 2024 01:20:21 GMT
ADD file:a6e150be02b0758f7cb3863651ae586c1592e19949e91c78e3771ceaad602a2a in / 
# Tue, 13 Feb 2024 01:20:22 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 03:57:55 GMT
STOPSIGNAL SIGINT
# Tue, 13 Feb 2024 03:59:05 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 03:59:07 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 13 Feb 2024 03:59:49 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Tue, 13 Feb 2024 03:59:50 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 13 Feb 2024 03:59:50 GMT
WORKDIR /var/www/html
# Tue, 13 Feb 2024 03:59:50 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 13 Feb 2024 03:59:50 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 13 Feb 2024 03:59:50 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 13 Feb 2024 03:59:50 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 13 Feb 2024 04:00:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 13 Feb 2024 04:00:02 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 13 Feb 2024 04:00:02 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 13 Feb 2024 04:00:02 GMT
USER adminer
# Tue, 13 Feb 2024 04:00:02 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:623a3ffac68434a8d471ef584bdb1dcbfafd4648778c484c1566ff7910d04b0e`  
		Last Modified: Tue, 13 Feb 2024 01:27:15 GMT  
		Size: 50.2 MB (50241706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caa4795efe3f8d59559a0046cc77b82f7e71074c886e2aa723558b36deaa89d6`  
		Last Modified: Tue, 13 Feb 2024 04:00:20 GMT  
		Size: 36.2 MB (36188417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb1b104e4728c4b3530100b8b681827fe0996521e8670ebae14bf1cc76633510`  
		Last Modified: Tue, 13 Feb 2024 04:00:13 GMT  
		Size: 392.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4def487651e6716b6f448c95b4ee574f485192618dbccf0eab501501370b0cc7`  
		Last Modified: Tue, 13 Feb 2024 04:00:38 GMT  
		Size: 2.7 KB (2709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e7ce4b4c42eaa72b03706128c5f38290c8d4cdc462f6f16935926c27f105a98`  
		Last Modified: Tue, 13 Feb 2024 04:00:38 GMT  
		Size: 1.9 KB (1870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1e96a14d6f4edae4eb2827c4392371c3597929d5b501e26dadf7e3eb33ae85a`  
		Last Modified: Tue, 13 Feb 2024 04:00:38 GMT  
		Size: 1.5 KB (1479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:452c2994e06c027cdb36a87f3508fa251002a9e6deafe485e8f75b7191caa9fd`  
		Last Modified: Tue, 13 Feb 2024 04:00:38 GMT  
		Size: 1.4 MB (1385357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dff41865b9cabd61248ee99bae59548d6d1a4088d6218dd725ef81111ec5ede`  
		Last Modified: Tue, 13 Feb 2024 04:00:38 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-fastcgi` - linux; arm64 variant v8

```console
$ docker pull adminer@sha256:527b885bf6ac684927a8b0fa36e754b3ab01322ae5c526b8ddb60db034d438e8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94355137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48175a25f2a0cbaf02c93ea5f566c0be569a5a0817d5e6a9dfe0a6b185cfd47e`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:27 GMT
ADD file:46791e28a2eef97a17393ff5cf2928d2e721f9380340a34c7d2e85053edec7c1 in / 
# Tue, 13 Feb 2024 00:41:27 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:35:35 GMT
STOPSIGNAL SIGINT
# Tue, 13 Feb 2024 01:35:53 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 01:35:54 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 13 Feb 2024 01:36:09 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Tue, 13 Feb 2024 01:36:09 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 13 Feb 2024 01:36:09 GMT
WORKDIR /var/www/html
# Tue, 13 Feb 2024 01:36:09 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 13 Feb 2024 01:36:10 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 13 Feb 2024 01:36:10 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 13 Feb 2024 01:36:10 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 13 Feb 2024 01:36:19 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 13 Feb 2024 01:36:19 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 13 Feb 2024 01:36:19 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 13 Feb 2024 01:36:19 GMT
USER adminer
# Tue, 13 Feb 2024 01:36:20 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:4245faf914201feff648b048cbaf6c46414d24a56e29e4cff1f82ac1b151d326`  
		Last Modified: Tue, 13 Feb 2024 00:45:14 GMT  
		Size: 53.7 MB (53721486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:253942c235484cc0a80af52e0bf1671cb46515d3975f82904e8cfb31b04dd86c`  
		Last Modified: Tue, 13 Feb 2024 01:36:35 GMT  
		Size: 39.2 MB (39241479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eef721d8b12382974bb7949ddfb312189924381e469ca9ed214c03a67f99c309`  
		Last Modified: Tue, 13 Feb 2024 01:36:29 GMT  
		Size: 386.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71f137755fa69eaca43e36817e8fc44c5896bdeeb7f3f911e375bf1f0fe83819`  
		Last Modified: Tue, 13 Feb 2024 01:36:52 GMT  
		Size: 2.7 KB (2708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf9264452ec4399b6e96f1d39369c354701d3290cb9013d310e47ddd4553d2da`  
		Last Modified: Tue, 13 Feb 2024 01:36:52 GMT  
		Size: 1.9 KB (1877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:201a9caec17e5042a166b47044dc0355ead5bac7504707e15b18bd6bfa349f87`  
		Last Modified: Tue, 13 Feb 2024 01:36:52 GMT  
		Size: 1.5 KB (1476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7081d1fa70947bf33375e16827cf1f231cff333f3ed0419edc482295355eee2`  
		Last Modified: Tue, 13 Feb 2024 01:36:53 GMT  
		Size: 1.4 MB (1385236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b121138db1d271107012be94d956c509e64f76dd328f1adb3b00831bac1281`  
		Last Modified: Tue, 13 Feb 2024 01:36:52 GMT  
		Size: 489.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-fastcgi` - linux; 386

```console
$ docker pull adminer@sha256:54a211a9a76464230ad0926f6f60bcb5d6b2c3e88b748cfcd0dba5ebeefca3c0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.0 MB (97007238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:717775d38a06836bb34a6e7532f3bcd35e1291d5827d8e8653cb24d7320b2836`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Tue, 13 Feb 2024 00:39:08 GMT
ADD file:357a898c0f7038f486b4958deafdca917cd52fe835643c888f731e981b2862dc in / 
# Tue, 13 Feb 2024 00:39:08 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:14:54 GMT
STOPSIGNAL SIGINT
# Tue, 13 Feb 2024 01:15:24 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 01:15:25 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 13 Feb 2024 01:15:52 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Tue, 13 Feb 2024 01:15:53 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 13 Feb 2024 01:15:53 GMT
WORKDIR /var/www/html
# Tue, 13 Feb 2024 01:15:53 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 13 Feb 2024 01:15:53 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 13 Feb 2024 01:15:53 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 13 Feb 2024 01:15:53 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 13 Feb 2024 01:16:07 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 13 Feb 2024 01:16:07 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 13 Feb 2024 01:16:07 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 13 Feb 2024 01:16:07 GMT
USER adminer
# Tue, 13 Feb 2024 01:16:07 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:dfd8f591553599fb1e7856eb5c0c822bdff33905eff3003ef95a2281f1003454`  
		Last Modified: Tue, 13 Feb 2024 00:44:10 GMT  
		Size: 56.1 MB (56057784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96d19401fa8382bd461439880f08a01ddd17b92fcbb3203cd8a9e0e75e9c2014`  
		Last Modified: Tue, 13 Feb 2024 01:16:30 GMT  
		Size: 39.6 MB (39557399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9974308b672f6b2b4009c5c4dd560915083c0c3a2d7458b3f80ba49ca8d7d3ed`  
		Last Modified: Tue, 13 Feb 2024 01:16:19 GMT  
		Size: 389.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c72255dc51a498800a868d016f70c9bd2ef1b7fee88272f6e1b858458028aab`  
		Last Modified: Tue, 13 Feb 2024 01:16:46 GMT  
		Size: 2.7 KB (2707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be67536246f3ce6f87355dce18b5d06af1fa5e9352e526483d319a72ad335b90`  
		Last Modified: Tue, 13 Feb 2024 01:16:47 GMT  
		Size: 1.9 KB (1869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d481d9d7eca190ac4d5fed2a46b1aff6e88f0eb5246037371a1b71a5e10aa20`  
		Last Modified: Tue, 13 Feb 2024 01:16:47 GMT  
		Size: 1.5 KB (1477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:814f3b649fca368dddca0d66a64415c695b7c8afeb216398fbb2391cb31e75c8`  
		Last Modified: Tue, 13 Feb 2024 01:16:47 GMT  
		Size: 1.4 MB (1385125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a955042792d45a6b957d74890002c24ae1b6148b78414ca35af4d9ecb44739c`  
		Last Modified: Tue, 13 Feb 2024 01:16:47 GMT  
		Size: 488.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-fastcgi` - linux; mips64le

```console
$ docker pull adminer@sha256:271344c6abea014443789df995af878c6dae466283abb757da590a6d5d00b0d7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.6 MB (92649081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55350330c3ec4edc7b5b89815f50d67ad17a47c17e0bffeeb390e5d2672b53cf`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Tue, 13 Feb 2024 02:04:48 GMT
ADD file:f0c2e3e71ce8133518aba22664b25c63fbd8c964a5c5ce64025477e120c8e59c in / 
# Tue, 13 Feb 2024 02:04:54 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 03:36:31 GMT
STOPSIGNAL SIGINT
# Tue, 13 Feb 2024 03:38:28 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 03:38:35 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 13 Feb 2024 03:40:18 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Tue, 13 Feb 2024 03:40:24 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 13 Feb 2024 03:40:28 GMT
WORKDIR /var/www/html
# Tue, 13 Feb 2024 03:40:31 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 13 Feb 2024 03:40:34 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 13 Feb 2024 03:40:38 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 13 Feb 2024 03:40:41 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 13 Feb 2024 03:41:28 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 13 Feb 2024 03:41:31 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 13 Feb 2024 03:41:34 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 13 Feb 2024 03:41:38 GMT
USER adminer
# Tue, 13 Feb 2024 03:41:41 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:8fd455dd9aba699cef01f8ec9dcd521cc60e9d65f6f4a8b4682b184d6d9f01cb`  
		Last Modified: Tue, 13 Feb 2024 02:15:55 GMT  
		Size: 53.3 MB (53303273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2b3fab4d5d79b50717411b36a2324cbb3d1d3486791df85de2af712f9d07cd1`  
		Last Modified: Tue, 13 Feb 2024 03:42:33 GMT  
		Size: 38.0 MB (37952800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00851486ec0d1ab007c17701e94d085f0e79217d81ba78ae92e94e103161c844`  
		Last Modified: Tue, 13 Feb 2024 03:42:07 GMT  
		Size: 394.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34db98bb886aae7deb83d145395dbfc5c9027017562cd75d7f9ad9192879f921`  
		Last Modified: Tue, 13 Feb 2024 03:42:53 GMT  
		Size: 2.7 KB (2716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1f0fb88da86c398662baf7a9585f32fa41d7cf988b8201d5297fb06e7f989f9`  
		Last Modified: Tue, 13 Feb 2024 03:42:53 GMT  
		Size: 1.7 KB (1728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a1422194ad74e892e7a642bc707ccd5296599fc19f51708d67e3ef6ab46808d`  
		Last Modified: Tue, 13 Feb 2024 03:42:54 GMT  
		Size: 1.5 KB (1481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4dfac8d1ca00c730f67d1035f62c7c9aa4f8c084a523ce459c8fbb4454d147b`  
		Last Modified: Tue, 13 Feb 2024 03:42:54 GMT  
		Size: 1.4 MB (1386198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44560a50da44e971f10145b5cf6dba44f4f6a85ee5f5d50081db2f6780fca820`  
		Last Modified: Tue, 13 Feb 2024 03:42:53 GMT  
		Size: 491.0 B  
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
